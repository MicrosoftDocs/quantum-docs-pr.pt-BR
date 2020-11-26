---
uid: Microsoft.Quantum.Canon.DelayCA
title: Operação DelayCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: a32a4f4a3f5d0f253a4c4eaf28c67db8da978b0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207081"
---
# <a name="delayca-operation"></a>Operação DelayCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma determinada operação com um atraso.

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Dada uma operação e uma entrada para essa operação, o aplica a operação quando uma entrada adicional é fornecida.
Em particular, a expressão `Delay(op, arg, _)` é uma operação que se aplica ao `op` `arg` quando chamado.
A expressão `Delay(op,arg,_)` permite atrasar a aplicação do `op` .

## <a name="input"></a>Entrada

### <a name="op--t--unit--is-adj--ctl"></a>op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

Uma operação a ser aplicada.


### <a name="arg--t"></a>ARG: ' t

A entrada à qual a operação é aplicada.


### <a name="aux--unit"></a>AUX: [unidade](xref:microsoft.quantum.lang-ref.unit)

Argumento usado para atrasar a aplicação de operação usando o aplicativo parcial.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser atrasada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)
- [Microsoft. Quantum. Canon. atrasado](xref:Microsoft.Quantum.Canon.Delayed)