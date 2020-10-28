---
uid: Microsoft.Quantum.Arrays.Zipped
title: Função compactada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 67170fa005675f0e5d788c9c3b350fb9a961a597
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694383"
---
# <a name="zipped-function"></a>Função compactada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


Dadas duas matrizes, retorna uma nova matriz de pares, de modo que cada par contém um elemento de cada matriz original.

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a>Entrada

### <a name="left--t"></a>esquerda: ' t []

Uma matriz que contém valores para o primeiro elemento de cada tupla.


### <a name="right--u"></a>direita: ' U []

Uma matriz que contém valores para o segundo elemento de cada tupla.



## <a name="output--tu"></a>Saída: (t, ' U) []

Uma matriz que contém pares do formulário `(left[idx], right[idx])` para cada `idx` . Se as duas matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos da matriz esquerda.
### <a name="u"></a>' U

O tipo dos elementos da matriz direita.

## <a name="see-also"></a>Consulte Também

- [Microsoft.Quantum.Arrays.Zipped3](xref:Microsoft.Quantum.Arrays.Zipped3)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)
- [Microsoft. Quantum. arrays. descompactado](xref:Microsoft.Quantum.Arrays.Unzipped)