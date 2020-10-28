---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Função sequencel
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694411"
---
# <a name="sequencel-function"></a>Função sequencel

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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