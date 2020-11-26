---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Tipo definido pelo usuário LabeledSample
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: a7c7dae5cd9e82d66bb98313f4200838006ca291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196320"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="d1eb5-102">Tipo definido pelo usuário LabeledSample</span><span class="sxs-lookup"><span data-stu-id="d1eb5-102">LabeledSample user defined type</span></span>

<span data-ttu-id="d1eb5-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d1eb5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d1eb5-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d1eb5-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="d1eb5-105">Um exemplo, rotulado com uma classe à qual o exemplo pertence.</span><span class="sxs-lookup"><span data-stu-id="d1eb5-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="d1eb5-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="d1eb5-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="d1eb5-107">Recursos: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d1eb5-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d1eb5-108">Um vetor de recursos para o exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1eb5-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="d1eb5-109">Rótulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d1eb5-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d1eb5-110">Um rótulo de número inteiro para a classe à qual este exemplo pertence.</span><span class="sxs-lookup"><span data-stu-id="d1eb5-110">An integer label for the class to which this sample belongs.</span></span>