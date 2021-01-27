---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorIndex
title: Função MultiplyGeneratorIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorIndex
qsharp.summary: Multiplies the coefficient in a `GeneratorIndex`.
ms.openlocfilehash: b53a483a0c2b8c99b733c9c87289fb212b5ffc89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848024"
---
# <a name="multiplygeneratorindex-function"></a><span data-ttu-id="92e6b-102">Função MultiplyGeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="92e6b-102">MultiplyGeneratorIndex function</span></span>

<span data-ttu-id="92e6b-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="92e6b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="92e6b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92e6b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="92e6b-105">Multiplica o coeficiente em um `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="92e6b-105">Multiplies the coefficient in a `GeneratorIndex`.</span></span>

```qsharp
function MultiplyGeneratorIndex (multiplier : Double, generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="92e6b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="92e6b-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="92e6b-107">multiplicador: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="92e6b-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="92e6b-108">O multiplicador no coeficiente.</span><span class="sxs-lookup"><span data-stu-id="92e6b-108">The multiplier on the coefficient.</span></span>


### <a name="generatorindex--generatorindex"></a><span data-ttu-id="92e6b-109">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="92e6b-109">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="92e6b-110">O `GeneratorIndex` a ser multiplicado.</span><span class="sxs-lookup"><span data-stu-id="92e6b-110">The `GeneratorIndex` to be multiplied.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="92e6b-111">Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="92e6b-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="92e6b-112">Um `GeneratorIndex` que representa um termo com o coeficiente um fator `multiplier` maior.</span><span class="sxs-lookup"><span data-stu-id="92e6b-112">A `GeneratorIndex` representing a term with coefficient a factor `multiplier` larger.</span></span>

## <a name="example"></a><span data-ttu-id="92e6b-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="92e6b-113">Example</span></span>

```qsharp
let gen = GeneratorIndex(([1,2,3],[coeff]),[1,2,3]);
let ((idxPaulis, idxDoubles), idxQubits) = MultiplyGeneratorIndex(multiplier, gen);
// idxDoubles[0] == multiplier * coeff;
```

## <a name="see-also"></a><span data-ttu-id="92e6b-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="92e6b-114">See Also</span></span>

- [<span data-ttu-id="92e6b-115">Microsoft. Quantum. Simulation. GeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="92e6b-115">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)