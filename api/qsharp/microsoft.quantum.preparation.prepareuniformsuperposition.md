---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Operação PrepareUniformSuperposition
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 8b57a7a02e9f704cf9677574824dfdc93fff25b0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693049"
---
# <a name="prepareuniformsuperposition-operation"></a><span data-ttu-id="5211b-102">Operação PrepareUniformSuperposition</span><span class="sxs-lookup"><span data-stu-id="5211b-102">PrepareUniformSuperposition operation</span></span>

<span data-ttu-id="5211b-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="5211b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="5211b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5211b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5211b-105">Cria uma superposição uniforme em Estados que codificam 0 a `nIndices - 1` .</span><span class="sxs-lookup"><span data-stu-id="5211b-105">Creates a uniform superposition over states that encode 0 through `nIndices - 1`.</span></span>

<span data-ttu-id="5211b-106">Ou seja, esse unitário $U $ cria uma superposição uniforme em todos os Estados de número $0 $ para $M-$1, dado um estado de entrada $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="5211b-106">That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$.</span></span> <span data-ttu-id="5211b-107">Em outras palavras, $ $ \begin{align} U\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.</span><span class="sxs-lookup"><span data-stu-id="5211b-107">In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}.</span></span>
<span data-ttu-id="5211b-108">\end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="5211b-108">\end{align} $$.</span></span>

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="5211b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="5211b-109">Input</span></span>

### <a name="nindices--int"></a><span data-ttu-id="5211b-110">nIndices: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5211b-110">nIndices : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5211b-111">O número desejado de Estados $M $ na superposição uniforme.</span><span class="sxs-lookup"><span data-stu-id="5211b-111">The desired number of states $M$ in the uniform superposition.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="5211b-112">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5211b-112">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5211b-113">O registro qubit que armazena os Estados de número no `LittleEndian` formato.</span><span class="sxs-lookup"><span data-stu-id="5211b-113">The qubit register that stores the number states in `LittleEndian` format.</span></span>
<span data-ttu-id="5211b-114">Esse registro deve ser capaz de armazenar o número $M-$1 e presume-se que seja inicializado no estado $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="5211b-114">This register must be able to store the number $M-1$, and is assumed to be initialized in the state $\ket{0\cdots 0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5211b-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5211b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5211b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5211b-116">Remarks</span></span>

<span data-ttu-id="5211b-117">A operação é adjointable, mas requer que `indexRegister` esteja em uma superposição uniforme nos Estados da primeira `nIndices` base nesse caso.</span><span class="sxs-lookup"><span data-stu-id="5211b-117">The operation is adjointable, but requires that `indexRegister` is in a uniform superposition over the first `nIndices` basis states in that case.</span></span>