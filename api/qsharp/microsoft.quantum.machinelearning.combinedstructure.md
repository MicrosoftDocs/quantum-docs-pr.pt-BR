---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: Função CombinedStructure
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: fbfd87761a40abe350e5f955fb53d8024eeb614e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694684"
---
# <a name="combinedstructure-function"></a>Função CombinedStructure

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Dada uma ou mais camadas de rotações controladas, retorna uma única camada com o índice de parâmetro de modelo deslocado de modo que as camadas distintas são parametrizadas por parâmetros de modelo distintos.

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Entrada

### <a name="layers--controlledrotation"></a>camadas: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []

As camadas a serem combinadas.



## <a name="output--controlledrotation"></a>Saída: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Uma única camada de rotações controladas, representando a concatenação de todas as outras camadas.