---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Função prefixos
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 3501c11437534b1623bffba272a4517487e5634a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220375"
---
# <a name="prefixes-function"></a>Função prefixos

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz, retorna todos os seus prefixos.

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a>Descrição

Retorna uma matriz de todos os prefixos, começando com uma matriz que só tem o primeiro elemento até a matriz completa.

## <a name="input"></a>Entrada

### <a name="array--t"></a>matriz: ' t []

Uma matriz de elementos.



## <a name="output--t"></a>Saída: ' T' [] []



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de `array` elementos.