---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Operação EstimateEnergy
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: 52e527a68818c80f93bc177d3563064fd0f2aea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693662"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="60152-102">Operação EstimateEnergy</span><span class="sxs-lookup"><span data-stu-id="60152-102">EstimateEnergy operation</span></span>

<span data-ttu-id="60152-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="60152-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="60152-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="60152-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="60152-105">Estima a energia do molécula somando a energia contribuída pelos termos individuais de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="60152-105">Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.</span></span>

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="60152-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="60152-106">Description</span></span>

<span data-ttu-id="60152-107">Essa operação depende implicitamente da Convenção de indexação da rotação para cima.</span><span class="sxs-lookup"><span data-stu-id="60152-107">This operation implicitly relies on the spin up-down indexing convention.</span></span>

## <a name="input"></a><span data-ttu-id="60152-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="60152-108">Input</span></span>

### <a name="jwhamiltonian--jordanwignerencodingdata"></a><span data-ttu-id="60152-109">jwHamiltonian: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="60152-109">jwHamiltonian : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="60152-110">O Jordan-Wigner Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="60152-110">The Jordan-Wigner Hamiltonian.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="60152-111">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="60152-111">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="60152-112">O número de amostras a serem usadas para a estimativa das expectativas do termo.</span><span class="sxs-lookup"><span data-stu-id="60152-112">The number of samples to use for the estimation of the term expectations.</span></span>



## <a name="output--double"></a><span data-ttu-id="60152-113">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="60152-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="60152-114">A energia estimada do molécula</span><span class="sxs-lookup"><span data-stu-id="60152-114">The estimated energy of the molecule</span></span>