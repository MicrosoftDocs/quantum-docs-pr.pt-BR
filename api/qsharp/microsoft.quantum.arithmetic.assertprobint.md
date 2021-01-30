---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Operação AssertProbInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843399"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="73bfa-102">Operação AssertProbInt</span><span class="sxs-lookup"><span data-stu-id="73bfa-102">AssertProbInt operation</span></span>

<span data-ttu-id="73bfa-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="73bfa-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="73bfa-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="73bfa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="73bfa-105">Declara que a probabilidade de um estado específico de um registro Quantum tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="73bfa-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="73bfa-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="73bfa-106">Description</span></span>

<span data-ttu-id="73bfa-107">Dado um estado $n $-qubit Quantum $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $, declara que a probabilidade $ | \ alpha_j | ^ 2 $ do estado $ \ket{j} $ indexado por $j $ tem o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="73bfa-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="73bfa-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="73bfa-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="73bfa-109">stateIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="73bfa-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="73bfa-110">O índice $j $ do estado $ \ket{j} $ representado por um `LittleEndian` registro.</span><span class="sxs-lookup"><span data-stu-id="73bfa-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="73bfa-111">esperado: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="73bfa-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="73bfa-112">O valor esperado de $ | \ alpha_j | ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="73bfa-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="73bfa-113">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="73bfa-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="73bfa-114">O registro qubit que armazena $ \ket{\psi} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="73bfa-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="73bfa-115">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="73bfa-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="73bfa-116">Tolerância absoluta na diferença entre real e esperado.</span><span class="sxs-lookup"><span data-stu-id="73bfa-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="73bfa-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="73bfa-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="73bfa-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="73bfa-118">Example</span></span>

<span data-ttu-id="73bfa-119">Suponha que o `qubits` registro codifica um estado de Quantum de 3 qubit $ \ket{\psi} = \ sqrt {1/8} \ ket {0} + \ sqrt {7/8} \ ket {6} $ no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="73bfa-119">Suppose that the `qubits` register encodes a 3-qubit quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{6}$ in little-endian format.</span></span>
<span data-ttu-id="73bfa-120">Isso significa que o número afirma $ \ket {0} \equiv\ket {0} \ket {0} \ket {0} $ e $ \ket {6} \equiv\ket \ket \ket {0} {1} {1} $.</span><span class="sxs-lookup"><span data-stu-id="73bfa-120">This means that the number states $\ket{0}\equiv\ket{0}\ket{0}\ket{0}$ and $\ket{6}\equiv\ket{0}\ket{1}\ket{1}$.</span></span> <span data-ttu-id="73bfa-121">Em seguida, as seguintes declarações serão realizadas com sucesso:</span><span class="sxs-lookup"><span data-stu-id="73bfa-121">Then the following asserts succeed:</span></span>

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```