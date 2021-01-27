---
uid: Microsoft.Quantum.Simulation.IdxToCoeff
title: Função IdxToCoeff
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdxToCoeff
qsharp.summary: Used in implementation of `PauliBlockEncoding`
ms.openlocfilehash: b6523c0d8f3e6d0ac4ec63234a7de342f8d6c065
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857899"
---
# <a name="idxtocoeff-function"></a><span data-ttu-id="5dc25-102">Função IdxToCoeff</span><span class="sxs-lookup"><span data-stu-id="5dc25-102">IdxToCoeff function</span></span>

<span data-ttu-id="5dc25-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5dc25-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5dc25-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5dc25-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5dc25-105">Usado na implementação de `PauliBlockEncoding`</span><span class="sxs-lookup"><span data-stu-id="5dc25-105">Used in implementation of `PauliBlockEncoding`</span></span>

```qsharp
function IdxToCoeff (idx : Int, genFun : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), genIdxToCoeff : (Microsoft.Quantum.Simulation.GeneratorIndex -> Double)) : Double
```


## <a name="input"></a><span data-ttu-id="5dc25-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dc25-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="5dc25-107">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5dc25-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="genfun--int---generatorindex"></a><span data-ttu-id="5dc25-108">genFun: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="5dc25-108">genFun : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>




### <a name="genidxtocoeff--generatorindex---double"></a><span data-ttu-id="5dc25-109">genIdxToCoeff: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex) -> [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5dc25-109">genIdxToCoeff : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--double"></a><span data-ttu-id="5dc25-110">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5dc25-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="see-also"></a><span data-ttu-id="5dc25-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5dc25-111">See Also</span></span>

- [<span data-ttu-id="5dc25-112">Microsoft. Quantum. Simulation. PauliBlockEncoding</span><span class="sxs-lookup"><span data-stu-id="5dc25-112">Microsoft.Quantum.Simulation.PauliBlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.PauliBlockEncoding)