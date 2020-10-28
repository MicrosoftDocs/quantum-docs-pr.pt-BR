---
uid: Microsoft.Quantum.Core.RangeEnd
title: Função RangeEnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 4dbcf517c4dc17775040444c77deb0e449082390
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693590"
---
# <a name="rangeend-function"></a>Função RangeEnd

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Agrupa [](https://nuget.org/packages/)


Retorna o valor final definido do intervalo especificado, que não é necessariamente o último elemento na sequência.

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a>Entrada

### <a name="range--range"></a>intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O valor final definido do intervalo especificado.

## <a name="remarks"></a>Comentários

O primeiro elemento de uma expressão de intervalo é `start` , o segundo elemento é `start+step` , o terceiro elemento é `start+step+step` , etc., até que `end` seja passado.

Observe que o valor final definido de um intervalo pode ser diferente do último elemento na sequência especificada pelo intervalo; por exemplo, em um intervalo de 0.. 2.. 5 o último elemento é 4, mas o valor final é 5.