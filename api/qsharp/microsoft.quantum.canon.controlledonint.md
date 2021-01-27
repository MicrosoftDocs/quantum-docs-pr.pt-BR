---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Função ControlledOnInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 6c7f46c44f2a2427f702e463195f26660cb4fca1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840781"
---
# <a name="controlledonint-function"></a>Função ControlledOnInt

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna um operador unitário que aplica um Oracle no registro de destino se o estado de registro de controle corresponder a um número inteiro positivo especificado.

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="numberstate--int"></a>número de série: [int](xref:microsoft.quantum.lang-ref.int)

Inteiro positivo.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

Operador unitário.



## <a name="output--qubitt--unit--is-adj--ctl"></a>Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[], t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Um operador unitário que se aplica ao `oracle` registro de destino se o estado de registro de controle corresponder ao estado de número `numberState` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

O valor de `numberState` é interpretado usando uma codificação little-endian.