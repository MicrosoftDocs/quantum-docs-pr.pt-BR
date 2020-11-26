---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Função sequencei
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 5f03e5f2baff8077c1fa3fb5f1f079528ef0e215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220290"
---
# <a name="sequencei-function"></a>Função sequencei

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Obter uma matriz de inteiros em um determinado intervalo.

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a>Entrada

### <a name="from--int"></a>de: [int](xref:microsoft.quantum.lang-ref.int)

Um índice inicial inclusivo do intervalo.


### <a name="to--int"></a>para: [int](xref:microsoft.quantum.lang-ref.int)

Um índice final inclusivo do intervalo que não é menor que `from` .



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz que contém a sequência de números `from` , `from + 1` ,..., `to` .