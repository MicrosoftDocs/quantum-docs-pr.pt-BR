---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Função ismutation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 361bb21bedc725c25a1f3dfc811e9cfda4cb45ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694449"
---
# <a name="ispermutation-function"></a>Função ismutation

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


Gera true se e somente se uma determinada matriz representar uma permutação.

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a>Descrição

Dada uma matriz `array` de comprimento `n` , retorna true se e somente se cada inteiro de `0` para `n - 1` aparecer exatamente uma vez em `array` , de modo que `array` possa ser interpretado como uma permutação nos `n` elementos.

## <a name="input"></a>Entrada

### <a name="permuation--int"></a>permuation: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz que pode ou não representar uma permutação.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)



## <a name="remarks"></a>Comentários

Uma matriz de comprimento zero é uma simples permuta.