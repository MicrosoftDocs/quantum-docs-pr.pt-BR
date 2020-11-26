---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: Função ExtendedGreatestCommonDivisorL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: abbbd367859952180f181a245ca0754646529b18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210702"
---
# <a name="extendedgreatestcommondivisorl-function"></a>Função ExtendedGreatestCommonDivisorL

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Computa uma tupla $ (u, v) $ de forma que $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, em que $ \operatorname{GCD} $ é $a $ maior divisor comum de $a $ e $b $. O GCD é sempre positivo.

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a>Entrada

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

o primeiro número do qual o maior divisor comum estendido está sendo computado


### <a name="b--bigint"></a>b: [bigint](xref:microsoft.quantum.lang-ref.bigint)

o segundo número do qual o maior divisor comum estendido está sendo computado



## <a name="output--bigintbigint"></a>Saída: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))

Tupla $ (u, v) $ com a propriedade $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.

## <a name="references"></a>Referências

- Essa implementação é de acordo com https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm