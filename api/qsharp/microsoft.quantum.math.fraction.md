---
uid: Microsoft.Quantum.Math.Fraction
title: Tipo de fração definido pelo usuário
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1838bb2b605b109742948ec0633b08ca01baea98
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210668"
---
# <a name="fraction-user-defined-type"></a>Tipo de fração definido pelo usuário

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa um número racional do formulário `p/q` . Integer `p` é o primeiro elemento da tupla e `q` é o segundo elemento da tupla.

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a>Itens nomeados

### <a name="numerator--int"></a>Numerador: [int](xref:microsoft.quantum.lang-ref.int)

Numerador da fração.
### <a name="denominator--int"></a>Denominador: [int](xref:microsoft.quantum.lang-ref.int)

Denominador da fração/