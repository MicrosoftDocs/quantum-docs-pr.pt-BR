---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Função IdentityGeneratorIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: b389ca1e0737463e6ccd5ce885b849c6b32d65d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844333"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="ecf04-102">Função IdentityGeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="ecf04-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="ecf04-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ecf04-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ecf04-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ecf04-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ecf04-105">Retorna um índice de gerador consistente com o zero Hamiltonian, `H = 0` , que corresponde à operação de evolução da identidade.</span><span class="sxs-lookup"><span data-stu-id="ecf04-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="ecf04-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ecf04-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="ecf04-107">idxTerm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ecf04-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ecf04-108">Essa entrada é ignorada e é definida para consistência com o <xref:microsoft.quantum.simulation.generatorsystem> tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ecf04-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="ecf04-109">Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ecf04-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ecf04-110">Um índice de gerador que representa a evolução sob o Hamiltonian $H = $0.</span><span class="sxs-lookup"><span data-stu-id="ecf04-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>