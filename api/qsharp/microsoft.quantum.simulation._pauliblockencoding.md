---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: Função _PauliBlockEncoding
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: ba30a7e87bd970961dc87f048aa586ff5c512e2a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693221"
---
# <a name="_pauliblockencoding-function"></a><span data-ttu-id="4dad1-102">Função _PauliBlockEncoding</span><span class="sxs-lookup"><span data-stu-id="4dad1-102">_PauliBlockEncoding function</span></span>

<span data-ttu-id="4dad1-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4dad1-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4dad1-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4dad1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4dad1-105">Cria um unitário de codificação de bloco para um Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="4dad1-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="4dad1-106">O Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ é descrito por uma soma dos termos de Pauli $P _j $, cada um com o coeficiente real $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="4dad1-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="4dad1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4dad1-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="4dad1-108">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="4dad1-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="4dad1-109">Um `GeneratorSystem` que descreve $H $ como uma soma dos termos do Pauli</span><span class="sxs-lookup"><span data-stu-id="4dad1-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>


### <a name="stateprepunitary--double---littleendian--unit-adj--ctl"></a><span data-ttu-id="4dad1-110">statePrepUnitary: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) de LittleEndian do ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="4dad1-110">statePrepUnitary : [Double](xref:microsoft.quantum.lang-ref.double)[] -> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="4dad1-111">Uma operação unitário $V $ que aplica o $V unitário _j $ controlado no índice $ \ket{j} $, dada uma função $f: j\rightarrow V_j $.</span><span class="sxs-lookup"><span data-stu-id="4dad1-111">A unitary operation $V$ that applies the unitary $V_j$ controlled on index $\ket{j}$, given a function $f: j\rightarrow V_j$.</span></span>


### <a name="multiplexer--intint---qubit--unit-adj--ctl---littleendianqubit--unit-adj--ctl"></a><span data-ttu-id="4dad1-112">Multiplexador: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) adj + CTL)-> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL</span><span class="sxs-lookup"><span data-stu-id="4dad1-112">multiplexer : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl) -> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>





## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="4dad1-113">Saída: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="4dad1-113">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="4dad1-114">Primeiro parâmetro</span><span class="sxs-lookup"><span data-stu-id="4dad1-114">First parameter</span></span>

<span data-ttu-id="4dad1-115">A uma norma de coeficientes $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="4dad1-115">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="4dad1-116">Segundo parâmetro</span><span class="sxs-lookup"><span data-stu-id="4dad1-116">Second parameter</span></span>

<span data-ttu-id="4dad1-117">Um `BlockEncodingReflection` unitário $U $ do Hamiltonian $U $.</span><span class="sxs-lookup"><span data-stu-id="4dad1-117">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $U$.</span></span> <span data-ttu-id="4dad1-118">Como esse unitário satisfaz $U ^ 2 = I $, também é uma reflexão.</span><span class="sxs-lookup"><span data-stu-id="4dad1-118">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dad1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dad1-119">Remarks</span></span>

<span data-ttu-id="4dad1-120">Operações de exemplo a preparação e despreparação do estado $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ e a construção de um unitário controlado por multiplicação são <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> e <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="4dad1-120">Example operations the prepare and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and construct a multiply-controlled unitary are <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>