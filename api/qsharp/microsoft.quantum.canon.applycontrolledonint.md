---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Operação ApplyControlledOnInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3dd17e6bc913e84941a6b81f134e60536a4c4122
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218998"
---
# <a name="applycontrolledonint-operation"></a>Operação ApplyControlledOnInt

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação unitário no registro de destino se o estado de registro de controle corresponder a um número inteiro positivo especificado.

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="numberstate--int"></a>número de série: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro não negativo no qual a operação `oracle` deve ser controlada.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

Uma operação unitário a ser controlada.


### <a name="controlregister--qubit"></a>controlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro do Quantum que controla a aplicação do `oracle` .


### <a name="targetregister--t"></a>targetRegister: ' t

Um registro no qual aplicar `oracle` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

O valor de `numberState` é interpretado usando uma codificação little-endian.

`numberState` deve ser no máximo $2 ^ \texttt{Length (controlRegister)}-$1.
Por exemplo, `numberState = 537` significa que `oracle` será aplicado se e somente se `controlRegister` estiver no estado $ \ket {537} $.