---
uid: Microsoft.Quantum.Canon.CControlledC
title: Função CControlledC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e5975455385e182236d7e2864e26ca00795a40c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694066"
---
# <a name="ccontrolledc-function"></a>Função CControlledC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Dada uma operação op, retorna uma nova operação que aplica a op se um bit de controle clássico for true. Se `false` nada acontecer.
O modificador `C` indica que a operação é controlável.

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="op--t--unit-ctl"></a>op: ' t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma operação a ser aplicada condicionalmente.



## <a name="output--boolt--unit-ctl"></a>Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), não) => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma nova operação que será op se o bit de controle clássico for true.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser aplicada condicionalmente.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. CControlled](xref:Microsoft.Quantum.Canon.CControlled)