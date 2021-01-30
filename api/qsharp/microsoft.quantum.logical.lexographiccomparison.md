---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Função LexographicComparison
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: de8179ab6e835d08e7f41287f31a876b7ecc91c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814393"
---
# <a name="lexographiccomparison-function"></a>Função LexographicComparison

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma função de comparação, retorna uma nova função que lexographically compara duas matrizes.

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a>Entrada

### <a name="elementcomparison--tt---bool"></a>elementComparison: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Uma função que compara dois elementos `x` e `y` retorna se `x` é menor ou igual a `y` .



## <a name="output--tt---bool"></a>Saída: (t [], t [])-> [bool](xref:microsoft.quantum.lang-ref.bool)

Uma função que compara duas matrizes `xs` e `ys` retorna se `xs` ocorre antes ou igual a `ys` na ordenação de lexographical.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos das matrizes que estão sendo comparados.

## <a name="remarks"></a>Comentários

A comparação de lexographic entre duas matrizes `xs` e `ys` é definida pelo procedimento a seguir. Dizemos que dois elementos `x` e `y` são equivalentes se `elementComparison(x, y)` e `elementComparison(y, x)` são ambos verdadeiros.

- Ambas as matrizes são comparadas elemento por elemento até o primeiro par de elementos que não são equivalentes. A matriz que contém o elemento que ocorre primeiro de acordo com o `elementComparison` é mencionada primeiro na ordenação lexographical.
- Se nenhum elemento inequivalente for encontrado e uma matriz for maior do que a outra, a matriz mais curta será mencionada primeiro.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. arrays. Classificed](xref:Microsoft.Quantum.Arrays.Sorted)