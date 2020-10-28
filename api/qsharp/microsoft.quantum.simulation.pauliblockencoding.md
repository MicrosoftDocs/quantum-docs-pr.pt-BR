---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Função PauliBlockEncoding
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 1426c7cbc257f9263ff45a96738fe798c3679ba1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694634"
---
# <a name="pauliblockencoding-function"></a><span data-ttu-id="b94be-102">Função PauliBlockEncoding</span><span class="sxs-lookup"><span data-stu-id="b94be-102">PauliBlockEncoding function</span></span>

<span data-ttu-id="b94be-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="b94be-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="b94be-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b94be-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b94be-105">Cria um unitário de codificação de bloco para um Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="b94be-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="b94be-106">O Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ é descrito por uma soma dos termos de Pauli $P _j $, cada um com o coeficiente real $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="b94be-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="b94be-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b94be-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="b94be-108">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="b94be-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="b94be-109">Um `GeneratorSystem` que descreve $H $ como uma soma dos termos do Pauli</span><span class="sxs-lookup"><span data-stu-id="b94be-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>



## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="b94be-110">Saída: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="b94be-110">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="b94be-111">Primeiro parâmetro</span><span class="sxs-lookup"><span data-stu-id="b94be-111">First parameter</span></span>

<span data-ttu-id="b94be-112">A uma norma de coeficientes $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="b94be-112">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="b94be-113">Segundo parâmetro</span><span class="sxs-lookup"><span data-stu-id="b94be-113">Second parameter</span></span>

<span data-ttu-id="b94be-114">Um `BlockEncodingReflection` unitário $U $ do Hamiltonian $H $.</span><span class="sxs-lookup"><span data-stu-id="b94be-114">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $H$.</span></span> <span data-ttu-id="b94be-115">Como esse unitário satisfaz $U ^ 2 = I $, também é uma reflexão.</span><span class="sxs-lookup"><span data-stu-id="b94be-115">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="b94be-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b94be-116">Remarks</span></span>

<span data-ttu-id="b94be-117">Isso é obtido preparando e despreparando o estado $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ e construindo um unitário controlado por multiplicação <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> e <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="b94be-117">This is obtained by preparing and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and constructing a multiply-controlled unitary <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>