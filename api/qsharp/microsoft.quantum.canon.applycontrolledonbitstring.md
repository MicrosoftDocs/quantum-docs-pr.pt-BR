---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Operação ApplyControlledOnBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 6947d2dbdec4cfbb592143024a7c8ccd53a32029
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219066"
---
# <a name="applycontrolledonbitstring-operation"></a>Operação ApplyControlledOnBitString

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação unitário no registro de destino, controlada em um estado especificado por uma determinada máscara de bits.

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="bits--bool"></a>bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

A cadeia de caracteres de bits para controlar a operação unitário especificada.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

A operação unitário a ser aplicada no registro de destino.


### <a name="controlregister--qubit"></a>controlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro do Quantum que controla a aplicação do `oracle` .


### <a name="targetregister--t"></a>targetRegister: ' t

O registro de destino a ser passado `oracle` como uma entrada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

O padrão fornecido por `bits` pode ser menor que `controlRegister` , nesse caso, qubits de controle adicional são ignorados (ou seja, nenhum controlado em $ \ket {0} $ nem $ \ket {1} $).
Se `bits` for maior que `controlRegister` , um erro será gerado.

Por exemplo, `bits = [0,1,0,0,1]` significa que `oracle` será aplicado se e somente se `controlRegister` estiver no estado $ \ket {0} \ket {1} \ket {0} \ket {0} \ket {1} $.