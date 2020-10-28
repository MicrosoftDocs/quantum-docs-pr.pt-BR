---
uid: Microsoft.Quantum.Canon.DelayedC
title: Função DelayedC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 7cfd77b0bb2d91c5a1c4bb5bc84e052421d733a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694014"
---
# <a name="delayedc-function"></a>Função DelayedC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Retorna uma operação que aplica a operação especificada com o argumento fornecido.

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="op--t--unit-ctl"></a>op: ' t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma operação a ser aplicada como resultado da aplicação do valor de retorno


### <a name="arg--t"></a>ARG: ' t

A entrada à qual a operação `op` é aplicada.



## <a name="output--unit--unit-ctl"></a>Saída: [Unit](xref:microsoft.quantum.lang-ref.unit) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) de unidade

Uma nova operação que se aplica `op` com a entrada `arg`

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser atrasada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. atrasado](xref:Microsoft.Quantum.Canon.Delayed)
- [Microsoft. Quantum. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)