---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Função IntAsBoolArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: f89cb3d7ca29d7deaaf49573b2670534166caded
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224336"
---
# <a name="intasboolarray-function"></a>Função IntAsBoolArray

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Produz uma representação binária de um inteiro positivo, usando a representação little-endian para a matriz retornada.

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a>Entrada

### <a name="number--int"></a>número: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro positivo a ser convertido em uma matriz de valores Boolianos.


### <a name="bits--int"></a>bits: [int](xref:microsoft.quantum.lang-ref.int)

O número de bits na representação binária de `number` .



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Uma matriz de valores Boolianos que representa `number` .

## <a name="remarks"></a>Comentários

A entrada `bits` deve estar entre 0 e 63.
A entrada `number` deve estar entre 0 e $2 ^ {\texttt{bits}}-$1.