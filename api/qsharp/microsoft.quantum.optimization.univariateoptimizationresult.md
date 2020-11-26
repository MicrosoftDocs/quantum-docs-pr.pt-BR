---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Tipo definido pelo usuário UnivariateOptimizationResult
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194025"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="86b49-102">Tipo definido pelo usuário UnivariateOptimizationResult</span><span class="sxs-lookup"><span data-stu-id="86b49-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="86b49-103">Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="86b49-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="86b49-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="86b49-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="86b49-105">Representa o resultado da otimização de uma função monovariável.</span><span class="sxs-lookup"><span data-stu-id="86b49-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="86b49-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="86b49-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="86b49-107">Coordenada: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86b49-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86b49-108">Entrada na qual foi encontrado um ideal.</span><span class="sxs-lookup"><span data-stu-id="86b49-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="86b49-109">Valor: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86b49-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86b49-110">Valor retornado pela função em seu ideal.</span><span class="sxs-lookup"><span data-stu-id="86b49-110">Value returned by the function at its optimum.</span></span>