---
uid: Microsoft.Quantum.Canon.CControlledC
title: Função CControlledC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 25ac2b35047b1c33a89149eae6d40f6f7ae3b454
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216907"
---
# <a name="ccontrolledc-function"></a>Função CControlledC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação op, retorna uma nova operação que aplica a op se um bit de controle clássico for true. Se `false` nada acontecer.
O modificador `C` indica que a operação é controlável.

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="op--t--unit--is-ctl"></a>op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

Uma operação a ser aplicada condicionalmente.



## <a name="output--boolt--unit--is-ctl"></a>Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), não) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é CTL

Uma nova operação que será op se o bit de controle clássico for true.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser aplicada condicionalmente.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. CControlled](xref:Microsoft.Quantum.Canon.CControlled)