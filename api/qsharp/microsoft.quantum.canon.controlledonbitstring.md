---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: Função ControlledOnBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 9435406506fc99fe211f5dce628b21c18ee4f9fe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216652"
---
# <a name="controlledonbitstring-function"></a>Função ControlledOnBitString

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna uma operação unitário que aplica um Oracle no registro de destino se o estado de registro de controle corresponder a uma máscara de bits especificada.

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a>Descrição

A saída dessa função é uma operação que pode ser representada por uma transformação unitário $U $ de modo que \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} em que $V $ é uma transformação unitário que representa a ação da `oracle` operação.

## <a name="input"></a>Entrada

### <a name="bits--bool"></a>bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

A cadeia de caracteres de bits para controlar a operação unitário especificada.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

A operação unitário a ser aplicada no registro de destino.



## <a name="output--qubitt--unit--is-adj--ctl"></a>Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[], t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Uma operação unitário que se aplica ao `oracle` registro de destino se o estado de registro de controle corresponder à máscara de bits `bits` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

O padrão fornecido por `bits` pode ser menor que `controlRegister` , nesse caso, qubits de controle adicional são ignorados (ou seja, nenhum controlado em $ \ket {0} $ nem $ \ket {1} $).
Se `bits` for maior que `controlRegister` , um erro será gerado.

Dada uma matriz booliana `bits` e uma operação unitário `oracle` , a saída dessa função é uma operação que executa as seguintes etapas:

* Aplique uma `X` operação a cada qubit do registro de controle que corresponda ao `false` elemento de `bits` ;
* aplicar `Controlled oracle` aos registros de destino e controle;
* Aplique uma `X` operação a cada qubit do registro de controle que corresponde ao `false` elemento de `bits` novamente para retornar o registro de controle para o estado original.

A saída de `Controlled` functor é um caso especial de `ControlledOnBitString` onde `bits` é igual a `[true, ..., true]` .