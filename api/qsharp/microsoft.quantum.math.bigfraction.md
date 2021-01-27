---
uid: Microsoft.Quantum.Math.BigFraction
title: Tipo definido pelo usuário BigFraction
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: bfbf49e7a3d060417e506a1977c20adc08b81f0e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846911"
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