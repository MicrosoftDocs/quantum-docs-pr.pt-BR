---
uid: Microsoft.Quantum.Math.PNormalized
title: Função PNormalized
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 196bdab67528aa8672a010ac3830459e27276ce9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227515"
---
# <a name="pnormalized-function"></a>Função PNormalized

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Normaliza um vetor de `Double` s na `L(p)` norma.

Ou seja, dada uma matriz $x $ do tipo `Double[]` , isso retorna uma matriz onde todos os elementos são divididos pelo $p $-norma $ \| x \| _p $.

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a>Entrada

### <a name="p--double"></a>p: [Double](xref:microsoft.quantum.lang-ref.double)

O expoente $p $ no $p $-normal.


### <a name="array--double"></a>matriz: [Double](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]

A matriz $x $ normalizada pelo $p $-normal $ \| x \| _p $.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Math. PNorm](xref:Microsoft.Quantum.Math.PNorm)