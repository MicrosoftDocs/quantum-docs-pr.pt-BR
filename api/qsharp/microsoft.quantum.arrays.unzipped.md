---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Função não compactada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 7eea7982721dc596b8660be5f3634df71b1ddf95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845375"
---
# <a name="unzipped-function"></a>Função não compactada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz de 2 tuplas, retorna uma tupla de duas matrizes, cada uma contendo os elementos das tuplas da matriz de entrada.

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a>Entrada

### <a name="arr--tu"></a>arr: (t, ' U) []

Uma matriz que contém 2 tuplas



## <a name="output--tu"></a>Saída: (t [], ' U [])

Duas matrizes, a primeira que contém todos os primeiros elementos das tuplas de entrada, a segunda que contém todos os elementos de cada segundo das tuplas de entrada.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo do primeiro elemento em cada tupla
### <a name="u"></a>' U

O tipo do segundo elemento em cada tupla

## <a name="example"></a>Exemplo

```qsharp
// split is same as ([6, 5, 5, 3, 2, 1], [true, false, false, false, true, false])
let split = Unzipped([(6, true), (5, false), (5, false), (3, false), (2, true), (1, false)]);
```

## <a name="see-also"></a>Consulte Também

- [Microsoft.Quantum.Arrays.ZipPED](xref:Microsoft.Quantum.Arrays.Zipped)