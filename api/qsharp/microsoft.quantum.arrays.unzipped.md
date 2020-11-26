---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Função não compactada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: aee1d48c9e0a1f104040bc56c78fdbb8bc4d34ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219950"
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

## <a name="see-also"></a>Consulte Também

- [Microsoft.Quantum.Arrays.ZipPED](xref:Microsoft.Quantum.Arrays.Zipped)