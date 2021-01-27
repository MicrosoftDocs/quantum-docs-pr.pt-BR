---
uid: Microsoft.Quantum.Core.RangeEnd
title: Função RangeEnd
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 196fab0bd97a441a16976033dc0d660c54cdfd6a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831375"
---
# <a name="rangeend-function"></a>Função RangeEnd

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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