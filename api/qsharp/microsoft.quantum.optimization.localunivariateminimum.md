---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: Função LocalUnivariateMinimum
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: 3b09af88bbed20a392768d005e5e9567b3bb7022
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693272"
---
# <a name="localunivariateminimum-function"></a><span data-ttu-id="38882-102">Função LocalUnivariateMinimum</span><span class="sxs-lookup"><span data-stu-id="38882-102">LocalUnivariateMinimum function</span></span>

<span data-ttu-id="38882-103">Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="38882-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="38882-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="38882-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="38882-105">Retorna o mínimo local para uma função monovariável em um intervalo limitado, usando uma pesquisa de intervalo dourado.</span><span class="sxs-lookup"><span data-stu-id="38882-105">Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.</span></span>

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a><span data-ttu-id="38882-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="38882-106">Input</span></span>

### <a name="fn--double---double"></a><span data-ttu-id="38882-107">FN: [duplo](xref:microsoft.quantum.lang-ref.double) -> [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="38882-107">fn : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="38882-108">A função monovariável a ser minimizada.</span><span class="sxs-lookup"><span data-stu-id="38882-108">The univariate function to be minimized.</span></span>


### <a name="bounds--doubledouble"></a><span data-ttu-id="38882-109">limites: ([duplo](xref:microsoft.quantum.lang-ref.double),[duplo](xref:microsoft.quantum.lang-ref.double))</span><span class="sxs-lookup"><span data-stu-id="38882-109">bounds : ([Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span></span>

<span data-ttu-id="38882-110">O intervalo no qual o mínimo local deve ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="38882-110">The interval in which the local minimum is to be found.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="38882-111">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="38882-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="38882-112">A precisão na entrada da função a ser tolerada.</span><span class="sxs-lookup"><span data-stu-id="38882-112">The accuracy in the function input to be tolerated.</span></span>
<span data-ttu-id="38882-113">A pesquisa para optima locais continuará até que o intervalo seja menor na largura que essa tolerância.</span><span class="sxs-lookup"><span data-stu-id="38882-113">The search for local optima will continue until the interval is smaller in width than this tolerance.</span></span>



## <a name="output--univariateoptimizationresult"></a><span data-ttu-id="38882-114">Saída: [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span><span class="sxs-lookup"><span data-stu-id="38882-114">Output : [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span></span>

<span data-ttu-id="38882-115">Um optima local da função fornecida, localizado dentro dos limites fornecidos.</span><span class="sxs-lookup"><span data-stu-id="38882-115">A local optima of the given function, located within the given bounds.</span></span>