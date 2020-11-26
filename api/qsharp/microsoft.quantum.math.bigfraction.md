---
uid: Microsoft.Quantum.Math.BigFraction
title: Tipo definido pelo usuário BigFraction
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1c9b9e350c4fa3664b2c66da05149005b1170ec3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211076"
---
# <a name="bigfraction-user-defined-type"></a>Tipo definido pelo usuário BigFraction

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa um número racional do formulário `p/q` . Integer `p` é o primeiro elemento da tupla e `q` é o segundo elemento da tupla.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>Itens nomeados

### <a name="numerator--bigint"></a>Numerador: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Numerador da fração.
### <a name="denominator--bigint"></a>Denominador: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Denominador da fração/