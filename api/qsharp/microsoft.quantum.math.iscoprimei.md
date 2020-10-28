---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: Função IsCoprimeI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: bdfaecb61f56967e21bf85ba190638b43685214d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696788"
---
# <a name="iscoprimei-function"></a>Função IsCoprimeI

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Agrupa [](https://nuget.org/packages/)


Retornará true se $a $ e $b $ forem coprimos e false caso contrário.

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

o primeiro número de que coprimality está sendo testado


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

o segundo número do qual coprimality está sendo testado



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

True, se $a $ e $b $ forem coprimos (por exemplo, seu maior divisor comum é 1) e false caso contrário