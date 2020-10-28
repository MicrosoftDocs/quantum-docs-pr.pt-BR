---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Função ControlledOnInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 4c48f3257f91fc50040d02cae7c2f7bdf87ea7c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694043"
---
# <a name="controlledonint-function"></a>Função ControlledOnInt

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Retorna um operador unitário que aplica um Oracle no registro de destino se o estado de registro de controle corresponder a um número inteiro positivo especificado.

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="numberstate--int"></a>número de série: [int](xref:microsoft.quantum.lang-ref.int)

Inteiro positivo.


### <a name="oracle--t--unit-adj--ctl"></a>Oracle: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL

Operador unitário.



## <a name="output--qubitt--unit-adj--ctl"></a>Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[], t) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL

Um operador unitário que se aplica ao `oracle` registro de destino se o estado de registro de controle corresponder ao estado de número `numberState` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

O valor de `numberState` é interpretado usando uma codificação little-endian.