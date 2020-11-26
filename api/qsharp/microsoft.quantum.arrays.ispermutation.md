---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Função ismutation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 144f683818b5d75de5b075328365d3e994de29d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220919"
---
# <a name="ispermutation-function"></a>Função ismutation

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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