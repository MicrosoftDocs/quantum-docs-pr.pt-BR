---
uid: Microsoft.Quantum.Core.RangeReverse
title: Função RangeReverse
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: f3b94d3c6fa6350a2c337f8bc8d889d24d87a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853653"
---
# <a name="rangereverse-function"></a>Função RangeReverse

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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