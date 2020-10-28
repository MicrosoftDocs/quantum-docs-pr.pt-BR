---
uid: Microsoft.Quantum.Canon.ConjugatedByC
title: Função ConjugatedByC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByC
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: c4c381e40c5a941487bcf78ebe5339574aedb45d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694049"
---
# <a name="conjugatedbyc-function"></a>Função ConjugatedByC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Dadas as operações externas e internas, retorna uma nova operação que conjuga a operação interna pela operação externa.

```qsharp
function ConjugatedByC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl)) : ('T => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="outeroperation--t--unit-adj"></a>outerOperation: t => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)

A operação $U $ que deve ser usada para conjugar $V $. Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.


### <a name="inneroperation--t--unit-ctl"></a>innerOperation: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

A operação $V $ sendo conjugada.



## <a name="output--t--unit-ctl"></a>Saída: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

Uma nova operação cuja ação é representada pelo unitário $U ^ {\dagger} V U $.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de destino no qual cada uma das operações internas e externas atuam.

## <a name="remarks"></a>Comentários

A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ConjugatedBy](xref:Microsoft.Quantum.Canon.ConjugatedBy)
- [Microsoft. Quantum. Canon. ConjugatedByA](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [Microsoft. Quantum. Canon. ConjugatedByCA](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [Microsoft. Quantum. Canon. ApplyWith](xref:Microsoft.Quantum.Canon.ApplyWith)