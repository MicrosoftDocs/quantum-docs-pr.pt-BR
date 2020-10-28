---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Função sequencei
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694414"
---
# <a name="sequencei-function"></a>Função sequencei

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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