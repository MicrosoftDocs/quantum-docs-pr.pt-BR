---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Função _IdentityTimeDependentGeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 7b93a6674bec974e61496696a3d8403225b16d80
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225594"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="8fb96-102">Função _IdentityTimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="8fb96-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="8fb96-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="8fb96-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="8fb96-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fb96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8fb96-105">Retorna um sistema gerador consistente com o Hamiltonian `H(s) = 0` , em que `s` é um parâmetro de agendamento.</span><span class="sxs-lookup"><span data-stu-id="8fb96-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="8fb96-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fb96-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="8fb96-107">agendamento: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8fb96-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8fb96-108">Essa entrada é ignorada e é definida para consistência com o <xref:microsoft.quantum.canon.timedependentgeneratorsystem> tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8fb96-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="8fb96-109">Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="8fb96-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="8fb96-110">Um sistema gerador que representa a evolução nas $H Hamiltonian = $0 para todos os $s $.</span><span class="sxs-lookup"><span data-stu-id="8fb96-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>