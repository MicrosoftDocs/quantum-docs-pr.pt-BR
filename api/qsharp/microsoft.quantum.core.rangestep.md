---
uid: Microsoft.Quantum.Core.RangeStep
title: Função RangeStep
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 667b579337eec28d6b75de61668bd79de176883e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853609"
---
# <a name="rangestep-function"></a>Função RangeStep

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna o inteiro que especifica como o próximo valor de um intervalo é calculado.

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a>Entrada

### <a name="range--range"></a>intervalo: [intervalo](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O valor de etapa definido do intervalo especificado.

## <a name="remarks"></a>Comentários

O primeiro elemento de uma expressão de intervalo é `start` , o segundo elemento é `start+step` , o terceiro elemento é `start+step+step` , etc., até que `end` seja passado.