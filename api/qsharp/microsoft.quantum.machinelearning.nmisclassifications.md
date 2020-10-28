---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Função NMisclassifications
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 9e356d68233519978e007e5a2999ca1be8cb7f83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693089"
---
# <a name="nmisclassifications-function"></a>Função NMisclassifications

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Dado um conjunto de rótulos deduzidos e um conjunto de rótulos corretos, retorna o número de índices nos quais cada conjunto de rótulos é diferente.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>Entrada

### <a name="proposed--int"></a>proposta: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>real: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O número de índices `idx` como esse `inferredLabels[idx] != actualLabels[idx]` .