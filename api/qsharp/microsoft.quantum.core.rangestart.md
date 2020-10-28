---
uid: Microsoft.Quantum.Core.RangeStart
title: Função RangeStart
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 3e4b0cebe34b4c98cb1d582a9cd11b46ff778517
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693579"
---
# <a name="rangestart-function"></a>Função RangeStart

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Agrupa [](https://nuget.org/packages/)


Retorna o valor inicial definido do intervalo especificado.

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a>Entrada

### <a name="range--range"></a>intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O valor inicial definido do intervalo especificado.

## <a name="remarks"></a>Comentários

O primeiro elemento de uma expressão de intervalo é `start` , o segundo elemento é `start+step` , o terceiro elemento é `start+step+step` , etc., até que `end` seja passado.

Observe que o valor inicial definido de um intervalo é o mesmo que o primeiro elemento da sequência, a menos que o intervalo especifique uma sequência vazia (por exemplo, 2... 1).