---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: Função PurifiedMixedStateWithData
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: c89ee8f5df58e5d6b154b67d2b39db208bc8a215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229946"
---
# <a name="purifiedmixedstatewithdata-function"></a><span data-ttu-id="e0229-102">Função PurifiedMixedStateWithData</span><span class="sxs-lookup"><span data-stu-id="e0229-102">PurifiedMixedStateWithData function</span></span>

<span data-ttu-id="e0229-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="e0229-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="e0229-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0229-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0229-105">Retorna uma operação que prepara um Purification de um determinado estado misto, confusas com um registro que representa uma determinada coleção de dados.</span><span class="sxs-lookup"><span data-stu-id="e0229-105">Returns an operation that prepares a a purification of a given mixed state, entangled with a register representing a given collection of data.</span></span>
<span data-ttu-id="e0229-106">Um "estado misto de purified com dados" refere-se a um estado do formulário σi √ Pi | i ⟩ | XI ⟩ | lixoi ⟩, em que cada XI é um bitstring de dados adicionais de codificação associados ao registro | i ⟩.</span><span class="sxs-lookup"><span data-stu-id="e0229-106">A "purified mixed state with data" refers to a state of the form Σᵢ √𝑝ᵢ |𝑖⟩ |𝑥ᵢ⟩ |garbageᵢ⟩, where each 𝑥ᵢ is a bitstring encoding additional data associated with the register |𝑖⟩.</span></span>

<span data-ttu-id="e0229-107">Consulte https://arxiv.org/pdf/1805.03662.pdf?page=15 para mais discussões.</span><span class="sxs-lookup"><span data-stu-id="e0229-107">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="e0229-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0229-108">Description</span></span>

<span data-ttu-id="e0229-109">Usa a técnica de ROM Quantum para representar uma determinada matriz de densidade, retornando essa representação como uma operação de preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="e0229-109">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="e0229-110">Em particular, dada uma lista de $N $ coeficientes $ \ alpha_j $ e um bitstring $ \vec{x}_j $ associado a cada coeficiente, essa função retorna uma operação que usa a técnica de ROM Quantum para preparar uma aproximação $ $ \begin{align} \tilde\rho = \sum_{j = 0} ^ {N-1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x} _J} \bra{\vec{x}_j} \end{align} $ $ do estado misto $ $ \begin{align} \rho = \sum_{j = 0} ^ {N-1} \ frac {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j} \otimes \ket{\vec{x} _j} \bra{\vec{x} _j}, \end{Align} $ $, em que cada $p _j $ é uma aproximação para o coeficiente determinado $ \ alpha_j $ de que $ $ \begin{align} \left | p_j-\frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ para cada $j $.</span><span class="sxs-lookup"><span data-stu-id="e0229-110">In particular, given a list of $N$ coefficients $\alpha_j$, and a bitstring $\vec{x}_j$ associated with each coefficient, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x}_j}\bra{\vec{x}_j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j} \otimes \ket{\vec{x}_j}\bra{\vec{x}_j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="e0229-111">Quando passou um registro de índice e um registro de qubits de lixo, inicialmente no estado $ \ket {0} \ket{00\cdots 0}, a operação retornada prepara os registros para o Purification de $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j} \ket{\vec{x} _J} \ket{\text{garbage} _J}, \end{align} $ $ para que a redefinição e desalocação do registro de lixo atue na preparação desejada para dentro do erro de destino $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="e0229-111">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j} \ket{\vec{x}_j} \ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="e0229-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0229-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="e0229-113">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e0229-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e0229-114">O erro de destino $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="e0229-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--doublebool"></a><span data-ttu-id="e0229-115">coeficientes: ([duplo](xref:microsoft.quantum.lang-ref.double),[bool](xref:microsoft.quantum.lang-ref.bool)[]) []</span><span class="sxs-lookup"><span data-stu-id="e0229-115">coefficients : ([Double](xref:microsoft.quantum.lang-ref.double),[Bool](xref:microsoft.quantum.lang-ref.bool)[])[]</span></span>

<span data-ttu-id="e0229-116">Matriz de $N $ coeficientes especificando a probabilidade de Estados de base, juntamente com o bitstring $ \vec{x} _j $ associado a cada coeficiente.</span><span class="sxs-lookup"><span data-stu-id="e0229-116">Array of $N$ coefficients specifying the probability of basis states, along with the bitstring $\vec{x}_j$ associated with each coefficient.</span></span>
<span data-ttu-id="e0229-117">Números negativos $-\ alpha_j $ serão tratados como $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="e0229-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="e0229-118">Saída: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="e0229-118">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="e0229-119">Uma operação que prepara $ \tilde \rho $ como um Purification para um índice conjunta e registro de lixo.</span><span class="sxs-lookup"><span data-stu-id="e0229-119">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0229-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0229-120">Remarks</span></span>

<span data-ttu-id="e0229-121">Os coeficientes fornecidos a essa operação são normalizados seguindo a norma 1, de modo que os coeficientes são sempre considerados para descrever uma distribuição de probabilidade categórica válida.</span><span class="sxs-lookup"><span data-stu-id="e0229-121">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="e0229-122">Referências</span><span class="sxs-lookup"><span data-stu-id="e0229-122">References</span></span>

- <span data-ttu-id="e0229-123">Codificação eletrônica de Spectra em circuitos Quantum com complexidade T linear Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru fosco, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="e0229-123">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="e0229-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e0229-124">See Also</span></span>

- [<span data-ttu-id="e0229-125">Microsoft. Quantum. Preparation. PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="e0229-125">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)