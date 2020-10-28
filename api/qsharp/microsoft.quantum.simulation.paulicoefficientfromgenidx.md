---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: Função PauliCoefficientFromGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 5bbc8d6113fb36bfd4050b98538bb61bbac02185
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694633"
---
# <a name="paulicoefficientfromgenidx-function"></a><span data-ttu-id="d80a8-102">Função PauliCoefficientFromGenIdx</span><span class="sxs-lookup"><span data-stu-id="d80a8-102">PauliCoefficientFromGenIdx function</span></span>

<span data-ttu-id="d80a8-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d80a8-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d80a8-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d80a8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d80a8-105">Extrai o coeficiente de um termo Pauli descrito por um `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="d80a8-105">Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a><span data-ttu-id="d80a8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d80a8-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="d80a8-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d80a8-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="d80a8-108">`GeneratorIndex` tipo que codifica um termo de Pauli.</span><span class="sxs-lookup"><span data-stu-id="d80a8-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--double"></a><span data-ttu-id="d80a8-109">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d80a8-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d80a8-110">O coeficiente do termo descrito por um `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="d80a8-110">The coefficient of the term described by a `GeneratorIndex`.</span></span>