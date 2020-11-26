---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: Função DecomposedIntoTimeStepsCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: aa5f09f2e1fde878b523b4efc20b86c26ac738ff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216533"
---
# <a name="decomposedintotimestepsca-function"></a><span data-ttu-id="1dd85-102">Função DecomposedIntoTimeStepsCA</span><span class="sxs-lookup"><span data-stu-id="1dd85-102">DecomposedIntoTimeStepsCA function</span></span>

<span data-ttu-id="1dd85-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1dd85-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1dd85-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1dd85-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1dd85-105">Retorna uma operação que implementa o integrador Trotter – Suzuki para uma determinada operação.</span><span class="sxs-lookup"><span data-stu-id="1dd85-105">Returns an operation implementing the Trotter–Suzuki integrator for a given operation.</span></span>

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="1dd85-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dd85-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="1dd85-107">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1dd85-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1dd85-108">O número de operações a serem decompostas em etapas de tempo.</span><span class="sxs-lookup"><span data-stu-id="1dd85-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="1dd85-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="1dd85-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1dd85-110">Uma operação que aceita uma entrada de índice (tipo `Int` ) e uma entrada de hora (tipo `Double` ) para decomposição.</span><span class="sxs-lookup"><span data-stu-id="1dd85-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) for decomposition.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="1dd85-111">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1dd85-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1dd85-112">Seleciona a ordem do Trotter – integrador de Suzuki a ser usado.</span><span class="sxs-lookup"><span data-stu-id="1dd85-112">Selects the order of the Trotter–Suzuki integrator to be used.</span></span>
<span data-ttu-id="1dd85-113">Ordem 1 e até mesmo pedidos 2, 4, 6,... atualmente têm suporte.</span><span class="sxs-lookup"><span data-stu-id="1dd85-113">Order 1 and even orders 2, 4, 6,... are currently supported.</span></span>



## <a name="output--doublet--unit--is-adj--ctl"></a><span data-ttu-id="1dd85-114">Saída: ([Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="1dd85-114">Output : ([Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1dd85-115">Retorna um unitário que implementa o integrador Trotter – Suzuki, em que o primeiro parâmetro `Double` é o tamanho da etapa de integração e o segundo parâmetro é o destino.</span><span class="sxs-lookup"><span data-stu-id="1dd85-115">Returns a unitary implementing the Trotter–Suzuki integrator, where the first parameter `Double` is the integration step size, and the second parameter is the target acted upon.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1dd85-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="1dd85-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1dd85-117">T'</span><span class="sxs-lookup"><span data-stu-id="1dd85-117">'T</span></span>

<span data-ttu-id="1dd85-118">O tipo em que cada etapa de tempo deve agir; Normalmente, o `Qubit[]` ou o `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="1dd85-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd85-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dd85-119">Remarks</span></span>

<span data-ttu-id="1dd85-120">Quando chamado com `order` igual a `1` , essa função retorna uma operação que pode ser simulada pelo Trotter de ordem mais baixa – integrador Suzuki $ $ \begin{align} S_1 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_j \lambda}, \end{align} $ $ em que seguimos a notação de [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139) e permitimos que $ \lambda $ seja o tempo de evolução (representado pela primeira entrada da operação retornada), e permitiu que $ \{ H_j \} _ {j = 1} ^ {m} $ seja o conjunto de geradores dinâmicos (distorção-Hermitian), que `op(j, lambda, _)` é simulado pelo operador unitário $e ^ {H_j \lambda} $.</span><span class="sxs-lookup"><span data-stu-id="1dd85-120">When called with `order` equal to `1`, this function returns an operation that can be simulated by the lowest-order Trotter–Suzuki integrator $$ \begin{align} S_1(\lambda) = \prod_{j = 1}^{m} e^{H_j \lambda}, \end{align} $$ where we have followed the notation of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139) and let $\lambda$ be the evolution time (represented by the first input of the returned operation), and have let $\{H_j\}_{j = 1}^{m}$ be the set of (skew-Hermitian) dynamical generators being integrated such that `op(j, lambda, _)` is simulated by the unitary operator $e^{H_j \lambda}$.</span></span>

<span data-ttu-id="1dd85-121">Da mesma forma, um `order` de `2` retorna o Trotter simétrico de segunda ordem – integrador de Suzuki $ $ \begin{align} S_2 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_k \lambda/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \lambda/2}.</span><span class="sxs-lookup"><span data-stu-id="1dd85-121">Similarly, an `order` of `2` returns the second-order symmetric Trotter–Suzuki integrator $$ \begin{align} S_2(\lambda) = \prod_{j = 1}^{m} e^{H_k \lambda / 2} \prod_{j' = m}^{1} e^{H_{j'} \lambda / 2}.</span></span>
<span data-ttu-id="1dd85-122">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="1dd85-122">\end{align} $$</span></span>

<span data-ttu-id="1dd85-123">Valores maiores iguais de `order` são implementados usando a construção recursiva de [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="1dd85-123">Higher even values of `order` are implemented using the recursive construction of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span>

## <a name="references"></a><span data-ttu-id="1dd85-124">Referências</span><span class="sxs-lookup"><span data-stu-id="1dd85-124">References</span></span>

- [<span data-ttu-id="1dd85-125">*D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders*</span><span class="sxs-lookup"><span data-stu-id="1dd85-125"> *D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders* </span></span>](https://arxiv.org/abs/quant-ph/0508139)