---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Função decompostay
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697054"
---
# <a name="decomposedon-function"></a>Função decompostay

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Agrupa [](https://nuget.org/packages/)


Redação de uma permutação em uma variável

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>Descrição

Dada uma permutação $ \pi $ ( `perm` ) e um índice $i $ ( `index` ), esse método retorna três permutas $ ((\ pi_l, \ pi_r), \pi ') $ de forma que as imagens de $ \ pi_l $ e $ \ pi_r $ não alterem bits em seus elementos em índices diferentes de $i $ e imagens de $ \pi ' $ não altere o bit $i $ em seus elementos.

## <a name="input"></a>Entrada

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>índice: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Saída: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])

