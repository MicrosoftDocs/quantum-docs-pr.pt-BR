---
uid: Microsoft.Quantum.Simulation._AddGeneratorSystems
title: Função _AddGeneratorSystems
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: e51addb38da99e508a71dffa757cd7fb19c89dcd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858001"
---
# <a name="_addgeneratorsystems-function"></a><span data-ttu-id="649ec-102">Função _AddGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="649ec-102">_AddGeneratorSystems function</span></span>

<span data-ttu-id="649ec-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="649ec-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="649ec-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="649ec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="649ec-105">Adiciona dois `GeneratorSystem` s para criar um novo `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="649ec-105">Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.</span></span>

```qsharp
function _AddGeneratorSystems (idxTerm : Int, nTermsA : Int, nTermsB : Int, generatorIndexFunctionA : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), generatorIndexFunctionB : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="649ec-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="649ec-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="649ec-107">idxTerm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="649ec-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ntermsa--int"></a><span data-ttu-id="649ec-108">nTermsA: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="649ec-108">nTermsA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ntermsb--int"></a><span data-ttu-id="649ec-109">nTermsB: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="649ec-109">nTermsB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="generatorindexfunctiona--int---generatorindex"></a><span data-ttu-id="649ec-110">generatorIndexFunctionA: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="649ec-110">generatorIndexFunctionA : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>




### <a name="generatorindexfunctionb--int---generatorindex"></a><span data-ttu-id="649ec-111">generatorIndexFunctionB: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="649ec-111">generatorIndexFunctionB : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>





## <a name="output--generatorindex"></a><span data-ttu-id="649ec-112">Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="649ec-112">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>



## <a name="remarks"></a><span data-ttu-id="649ec-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="649ec-113">Remarks</span></span>

<span data-ttu-id="649ec-114">Esta é uma etapa intermediária e não deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="649ec-114">This is an intermediate step and should not be called.</span></span>