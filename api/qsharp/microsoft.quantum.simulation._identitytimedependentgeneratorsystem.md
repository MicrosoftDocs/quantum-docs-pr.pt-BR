---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Função _IdentityTimeDependentGeneratorSystem
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 960842f50353c01362f90eb38d979fb7c4f15d9a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857995"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="6d3fd-102">Função _IdentityTimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="6d3fd-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="6d3fd-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6d3fd-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6d3fd-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6d3fd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6d3fd-105">Retorna um sistema gerador consistente com o Hamiltonian `H(s) = 0` , em que `s` é um parâmetro de agendamento.</span><span class="sxs-lookup"><span data-stu-id="6d3fd-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="6d3fd-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d3fd-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="6d3fd-107">agendamento: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6d3fd-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6d3fd-108">Essa entrada é ignorada e é definida para consistência com o <xref:microsoft.quantum.canon.timedependentgeneratorsystem> tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6d3fd-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="6d3fd-109">Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="6d3fd-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="6d3fd-110">Um sistema gerador que representa a evolução nas $H Hamiltonian = $0 para todos os $s $.</span><span class="sxs-lookup"><span data-stu-id="6d3fd-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>