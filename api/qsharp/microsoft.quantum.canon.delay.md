---
uid: Microsoft.Quantum.Canon.Delay
title: Operação de atraso
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: f9f0e5c3120eb69bd7431d52d6cde5e846ffbe4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694029"
---
# <a name="delay-operation"></a>Operação de atraso

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Aplica uma determinada operação com um atraso.

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a>Descrição

Dada uma operação e uma entrada para essa operação, o aplica a operação quando uma entrada adicional é fornecida.
Em particular, a expressão `Delay(op, arg, _)` é uma operação que se aplica ao `op` `arg` quando chamado.
A expressão `Delay(op,arg,_)` permite atrasar a aplicação do `op` .

## <a name="input"></a>Entrada

### <a name="op--t--u"></a>op: ' T' => ' U 

Uma operação a ser aplicada.


### <a name="arg--t"></a>ARG: ' t

A entrada à qual a operação é aplicada.


### <a name="aux--unit"></a>AUX: [unidade](xref:microsoft.quantum.lang-ref.unit)

Argumento usado para atrasar a aplicação de operação usando o aplicativo parcial.



## <a name="output--u"></a>Saída: ' U



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser atrasada.
### <a name="u"></a>' U

O tipo de retorno da operação a ser atrasada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. DelayC](xref:Microsoft.Quantum.Canon.DelayC)
- [Microsoft. Quantum. Canon. Delaya](xref:Microsoft.Quantum.Canon.DelayA)
- [Microsoft. Quantum. Canon. DelayCA](xref:Microsoft.Quantum.Canon.DelayCA)
- [Microsoft. Quantum. Canon. atrasado](xref:Microsoft.Quantum.Canon.Delayed)