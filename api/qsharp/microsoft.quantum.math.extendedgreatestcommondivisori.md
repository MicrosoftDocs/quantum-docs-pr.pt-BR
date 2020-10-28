---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: Função ExtendedGreatestCommonDivisorI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 8cb21ae5052ae6c5a8aed8be71d6bd3d32034272
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696840"
---
# <a name="extendedgreatestcommondivisori-function"></a>Função ExtendedGreatestCommonDivisorI

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Agrupa [](https://nuget.org/packages/)


Computa uma tupla $ (u, v) $ de forma que $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, em que $ \operatorname{GCD} $ é $a $ maior divisor comum de $a $ e $b $. O GCD é sempre positivo.

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

o primeiro número do qual o maior divisor comum estendido está sendo computado


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

o segundo número do qual o maior divisor comum estendido está sendo computado



## <a name="output--intint"></a>Saída: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

Tupla $ (u, v) $ com a propriedade $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.

## <a name="references"></a>Referências

- Essa implementação é de acordo com https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm