---
uid: Microsoft.Quantum.Math.BitSizeI
title: Função BitSizeI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7cfe03908a8a394fc8ceb1c9facbf02f3db2d48
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696765"
---
# <a name="bitsizei-function"></a>Função BitSizeI

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Agrupa [](https://nuget.org/packages/)


Para um inteiro não negativo `a` , retorna o número de bits necessários para representar `a` .

Ou seja, retorna o menor $n $, que $a < 2 ^ n $.

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

O inteiro cujo tamanho de bit deve ser calculado.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O tamanho de bit de `a` .