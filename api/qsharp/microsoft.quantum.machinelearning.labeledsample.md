---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Tipo definido pelo usuário LabeledSample
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: 8b4afa1eaf7ca69938b2606163cd1ec17a1ad80f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693317"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="d81bd-102">Tipo definido pelo usuário LabeledSample</span><span class="sxs-lookup"><span data-stu-id="d81bd-102">LabeledSample user defined type</span></span>

<span data-ttu-id="d81bd-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d81bd-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d81bd-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d81bd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d81bd-105">Um exemplo, rotulado com uma classe à qual o exemplo pertence.</span><span class="sxs-lookup"><span data-stu-id="d81bd-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="d81bd-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="d81bd-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="d81bd-107">Recursos: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d81bd-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d81bd-108">Um vetor de recursos para o exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="d81bd-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="d81bd-109">Rótulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d81bd-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d81bd-110">Um rótulo de número inteiro para a classe à qual este exemplo pertence.</span><span class="sxs-lookup"><span data-stu-id="d81bd-110">An integer label for the class to which this sample belongs.</span></span>