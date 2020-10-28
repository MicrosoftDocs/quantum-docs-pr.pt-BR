---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Função de classificações incorretas
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 500c2910f7c5616c88ff6c70ab3cc16680e199fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696820"
---
# <a name="misclassifications-function"></a>Função de classificações incorretas

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Dado um conjunto de rótulos deduzidos e um conjunto de rótulos corretos, retorna índices para onde cada conjunto de rótulos difere.

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a>Entrada

### <a name="inferredlabels--int"></a>inferredLabels: [int](xref:microsoft.quantum.lang-ref.int)[]

Os rótulos inferidos para um determinado treinamento ou conjunto de validação.


### <a name="actuallabels--int"></a>actualLabels: [int](xref:microsoft.quantum.lang-ref.int)[]

Os rótulos verdadeiros para um determinado treinamento ou conjunto de validação.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz de índices `idx` como essa `inferredLabels[idx] != actualLabels[idx]` .