---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Função FeatureRegisterSize
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 8f7c47c7547e7a0ac1672f308de445c1b46461e1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696778"
---
# <a name="featureregistersize-function"></a>Função FeatureRegisterSize

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Retorna o número de qubits necessário para codificar um vetor de recurso específico.

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a>Entrada

### <a name="sample--double"></a>exemplo: [Double](xref:microsoft.quantum.lang-ref.double)[]

Um vetor de recurso de exemplo a ser codificado em um registro qubit.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O tamanho necessário para codificar `sample` em um registro qubit, expresso como um número de qubits.