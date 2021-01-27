---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Função NMisclassifications
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: adc7042d6108c7ec72d13340633824d3eaf5e18e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853912"
---
# <a name="nmisclassifications-function"></a>Função NMisclassifications

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Dado um conjunto de rótulos deduzidos e um conjunto de rótulos corretos, retorna o número de índices nos quais cada conjunto de rótulos é diferente.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>Entrada

### <a name="proposed--int"></a>proposta: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>real: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O número de índices `idx` como esse `inferredLabels[idx] != actualLabels[idx]` .

## <a name="example"></a>Exemplo

```qsharp
let nMisclassifications = NMisclassifications([1, 1, 0, 0], [0, 1, 1, 0]);
Message($"{nMisclassifications}"); // Will print 2.
```