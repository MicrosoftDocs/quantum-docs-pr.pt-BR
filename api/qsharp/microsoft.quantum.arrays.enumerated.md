---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Função enumerada
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221412"
---
# <a name="enumerated-function"></a>Função enumerada

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz, retorna uma nova matriz contendo os elementos da matriz original junto com os índices de cada elemento.

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a>Entrada

### <a name="array--telement"></a>matriz: ' TElement []

Uma matriz cujos elementos devem ser enumerados.



## <a name="output--inttelement"></a>Saída: ([int](xref:microsoft.quantum.lang-ref.int), ' TElement) []

Uma nova matriz que contém os elementos da matriz original junto com seus índices.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="telement"></a>'TElement

O tipo de elementos da matriz.