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
# <a name="combinedstructure-function"></a><span data-ttu-id="c2719-102">Função CombinedStructure</span><span class="sxs-lookup"><span data-stu-id="c2719-102">CombinedStructure function</span></span>

<span data-ttu-id="c2719-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c2719-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="c2719-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2719-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2719-105">Dada uma ou mais camadas de rotações controladas, retorna uma única camada com o índice de parâmetro de modelo deslocado de modo que as camadas distintas são parametrizadas por parâmetros de modelo distintos.</span><span class="sxs-lookup"><span data-stu-id="c2719-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="c2719-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2719-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="c2719-107">camadas: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="c2719-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="c2719-108">As camadas a serem combinadas.</span><span class="sxs-lookup"><span data-stu-id="c2719-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="c2719-109">Saída: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="c2719-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="c2719-110">Uma única camada de rotações controladas, representando a concatenação de todas as outras camadas.</span><span class="sxs-lookup"><span data-stu-id="c2719-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>