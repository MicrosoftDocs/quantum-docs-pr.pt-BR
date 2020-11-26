---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Tipo definido pelo usuário SequentialModel
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: 3afdb8dafe0179535fe5d8c3dff668f1f3de2f7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196167"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="958c1-102">Tipo definido pelo usuário SequentialModel</span><span class="sxs-lookup"><span data-stu-id="958c1-102">SequentialModel user defined type</span></span>

<span data-ttu-id="958c1-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="958c1-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="958c1-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="958c1-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="958c1-105">Descreve um modelo de classificador Quantum composto por uma sequência de rotações parametrizadas e controladas, uma atribuição de ângulos de rotação e uma tendência entre as duas classes reconhecidas pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="958c1-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="958c1-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="958c1-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="958c1-107">Estrutura: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="958c1-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="958c1-108">A sequência de rotações controladas usadas para classificar entradas.</span><span class="sxs-lookup"><span data-stu-id="958c1-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="958c1-109">Parâmetros: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="958c1-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="958c1-110">Uma atribuição de ângulos de rotação para a estrutura de classificação fornecida.</span><span class="sxs-lookup"><span data-stu-id="958c1-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="958c1-111">Tendência: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="958c1-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="958c1-112">A tendência entre as duas classes reconhecidas por este classificador.</span><span class="sxs-lookup"><span data-stu-id="958c1-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="958c1-113">Referências</span><span class="sxs-lookup"><span data-stu-id="958c1-113">References</span></span>

- [<span data-ttu-id="958c1-114">arXiv:1804.00633</span><span class="sxs-lookup"><span data-stu-id="958c1-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)