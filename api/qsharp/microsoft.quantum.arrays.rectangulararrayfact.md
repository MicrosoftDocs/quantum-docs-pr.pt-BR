---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Função RectangularArrayFact
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: f0d3f4d6bfa9e86f1c7a91792c09e16fe86433a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694418"
---
# <a name="rectangulararrayfact-function"></a>Função RectangularArrayFact

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


Representa uma condição de que uma matriz bidimensional tem uma forma retangular

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>Descrição

Essa função declara que cada linha em uma matriz tem o mesmo comprimento.

## <a name="input"></a>Entrada

### <a name="array--t"></a>matriz: t [] []

Uma matriz bidimensional de elementos


### <a name="message--string"></a>mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Uma mensagem a ser impressa se a matriz não for uma matriz retangular



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de cada elemento de `array` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. arrays. SquareArrayFact](xref:Microsoft.Quantum.Arrays.SquareArrayFact)