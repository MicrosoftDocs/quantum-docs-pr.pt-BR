---
uid: Microsoft.Quantum.Canon.ConjugatedByC
title: Função ConjugatedByC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByC
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 622b1d93dcbd02d000a68de23c66537b24d36c99
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840831"
---
# <a name="conjugatedbyc-function"></a>Função ConjugatedByC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dadas as operações externas e internas, retorna uma nova operação que conjuga a operação interna pela operação externa.

```qsharp
function ConjugatedByC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl)) : ('T => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="outeroperation--t--unit--is-adj"></a>outerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

A operação $U $ que deve ser usada para conjugar $V $. Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.


### <a name="inneroperation--t--unit--is-ctl"></a>innerOperation: T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

A operação $V $ sendo conjugada.



## <a name="output--t--unit--is-ctl"></a>Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

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