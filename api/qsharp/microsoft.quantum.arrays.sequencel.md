---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Função sequencel
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220256"
---
# <a name="sequencel-function"></a>Função sequencel

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Obter uma matriz de inteiros em um determinado intervalo.

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a>Entrada

### <a name="from--bigint"></a>de: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Um índice inicial inclusivo do intervalo.


### <a name="to--bigint"></a>para: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Um índice final inclusivo do intervalo que não é menor que `from` .



## <a name="output--bigint"></a>Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]

Uma matriz que contém a sequência de números `from` , `from + 1` ,..., `to` .

## <a name="remarks"></a>Comentários

A diferença entre `from` e `to` deve se ajustar a um `Int` valor.