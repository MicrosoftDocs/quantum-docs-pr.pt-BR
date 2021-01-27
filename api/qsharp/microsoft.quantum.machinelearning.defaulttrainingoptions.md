---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: Função defaulttrainoptions
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856003"
---
# <a name="defaulttrainingoptions-function"></a>Função defaulttrainoptions

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Retorna um conjunto padrão de opções para classificadores de treinamento.

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a>Saída: [trainoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Um conjunto razoável de opções de treinamento padrão para uso durante o treinamento de classificadores.

## <a name="example"></a>Exemplo

Para usar as opções padrão, mas com medidas adicionais, use o `w/` operador:

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```