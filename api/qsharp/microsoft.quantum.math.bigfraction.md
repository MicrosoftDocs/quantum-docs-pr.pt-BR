---
uid: Microsoft.Quantum.Math.BigFraction
title: Tipo definido pelo usuário BigFraction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a8daa54947097b95040a2dfa7a4d1b90bfaff856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696767"
---
# <a name="bigfraction-user-defined-type"></a>Tipo definido pelo usuário BigFraction

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Agrupa [](https://nuget.org/packages/)


Representa um número racional do formulário `p/q` . Integer `p` é o primeiro elemento da tupla e `q` é o segundo elemento da tupla.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>Itens nomeados

### <a name="numerator--bigint"></a>Numerador: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Numerador da fração.
### <a name="denominator--bigint"></a>Denominador: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Denominador da fração/