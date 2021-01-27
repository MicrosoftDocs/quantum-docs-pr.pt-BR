---
uid: Microsoft.Quantum.Canon.DelayedC
title: Função DelayedC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: a1f2582668131816b774bf4a8b7476d9f1ee8cad
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840572"
---
# <a name="delayedc-function"></a>Função DelayedC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna uma operação que aplica a operação especificada com o argumento fornecido.

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="op--t--unit--is-ctl"></a>op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

Uma operação a ser aplicada como resultado da aplicação do valor de retorno


### <a name="arg--t"></a>ARG: ' t

A entrada à qual a operação `op` é aplicada.



## <a name="output--unit--unit--is-ctl"></a>Saída: unidade de [unidade](xref:microsoft.quantum.lang-ref.unit) => [](xref:microsoft.quantum.lang-ref.unit) é CTL

Uma nova operação que se aplica `op` com a entrada `arg`

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser atrasada.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. atrasado](xref:Microsoft.Quantum.Canon.Delayed)
- [Microsoft. Quantum. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)