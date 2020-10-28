---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Função _IdentityTimeDependentGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 0b440ce9adaab562e16b02da46844c68a7470b11
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693225"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="5ced1-102">Função _IdentityTimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="5ced1-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="5ced1-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5ced1-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5ced1-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5ced1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5ced1-105">Retorna um sistema gerador consistente com o Hamiltonian `H(s) = 0` , em que `s` é um parâmetro de agendamento.</span><span class="sxs-lookup"><span data-stu-id="5ced1-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="5ced1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ced1-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="5ced1-107">agendamento: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5ced1-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5ced1-108">Essa entrada é ignorada e é definida para consistência com o <xref:microsoft.quantum.canon.timedependentgeneratorsystem> tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5ced1-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="5ced1-109">Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="5ced1-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="5ced1-110">Um sistema gerador que representa a evolução nas $H Hamiltonian = $0 para todos os $s $.</span><span class="sxs-lookup"><span data-stu-id="5ced1-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>