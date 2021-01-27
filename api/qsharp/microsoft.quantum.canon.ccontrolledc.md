---
uid: Microsoft.Quantum.Canon.CControlledC
title: Função CControlledC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: a10c8f0f835fe7cbb8f2d89d521a548169613c0a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840972"
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