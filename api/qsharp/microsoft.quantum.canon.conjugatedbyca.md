---
uid: Microsoft.Quantum.Canon.ConjugatedByCA
title: Função ConjugatedByCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByCA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: acd5a9f796f751b9c9c374d841e80de9286fcd24
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207302"
---
# <a name="conjugatedbyca-function"></a>Função ConjugatedByCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dadas as operações externas e internas, retorna uma nova operação que conjuga a operação interna pela operação externa.

```qsharp
function ConjugatedByCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl)) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="outeroperation--t--unit--is-adj"></a>outerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

A operação $U $ que deve ser usada para conjugar $V $. Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.


### <a name="inneroperation--t--unit--is-adj--ctl"></a>innerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

A operação $V $ sendo conjugada.



## <a name="output--t--unit--is-adj--ctl"></a>Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

Uma nova operação cuja ação é representada pelo unitário $U ^ {\dagger} V U $.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de destino no qual cada uma das operações internas e externas atuam.

## <a name="remarks"></a>Comentários

A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ConjugatedByA](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [Microsoft. Quantum. Canon. ConjugatedByC](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [Microsoft. Quantum. Canon. ConjugatedByCA](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [Microsoft. Quantum. Canon. ApplyWith](xref:Microsoft.Quantum.Canon.ApplyWith)