---
uid: Microsoft.Quantum.Core.RangeReverse
title: Função RangeReverse
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: d4e612d2f175015b7193634aeec12f9df12df7d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693588"
---
# <a name="rangereverse-function"></a>Função RangeReverse

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Agrupa [](https://nuget.org/packages/)


Retorna um novo intervalo que é o inverso do intervalo de entrada.

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a>Entrada

### <a name="r--range"></a>r: [intervalo](xref:microsoft.quantum.lang-ref.range)

Intervalo de entrada.



## <a name="output--range"></a>Saída: [intervalo](xref:microsoft.quantum.lang-ref.range)

Um novo intervalo que é o inverso do intervalo especificado.

## <a name="remarks"></a>Comentários

Observe que o inverso de um intervalo não é simplesmente `end` .. `-step` . `start` , porque o último elemento real de um intervalo pode não ser o mesmo que `end` .