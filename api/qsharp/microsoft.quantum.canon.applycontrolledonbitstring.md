---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Operação ApplyControlledOnBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 7a054511bacff574e6f7e889ace048c78886cf91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694324"
---
# <a name="applycontrolledonbitstring-operation"></a>Operação ApplyControlledOnBitString

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Aplica uma operação unitário no registro de destino, controlada em um estado especificado por uma determinada máscara de bits.

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a>Entrada

### <a name="bits--bool"></a>bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

A cadeia de caracteres de bits para controlar a operação unitário especificada.


### <a name="oracle--t--unit-adj--ctl"></a>Oracle: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL

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