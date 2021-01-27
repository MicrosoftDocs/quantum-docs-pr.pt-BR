---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Tipo definido pelo usuário ValidationResults
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 923fd80333b6bf77daeaac2bf205db620e61cfd0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846084"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="63e48-102">Tipo definido pelo usuário ValidationResults</span><span class="sxs-lookup"><span data-stu-id="63e48-102">ValidationResults user defined type</span></span>

<span data-ttu-id="63e48-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="63e48-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="63e48-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="63e48-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="63e48-105">Os resultados de ter validado um classificador em relação a um conjunto de amostras.</span><span class="sxs-lookup"><span data-stu-id="63e48-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="63e48-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="63e48-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="63e48-107">NMisclassifications: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="63e48-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="63e48-108">O número de classificações incorretas observadas durante a validação.</span><span class="sxs-lookup"><span data-stu-id="63e48-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="63e48-109">NValidationSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="63e48-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

