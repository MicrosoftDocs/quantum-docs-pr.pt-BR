---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: Função PurifiedMixedState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 73b031f1082d0a12975abad074b07184dcbabdbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230014"
---
# <a name="purifiedmixedstate-function"></a><span data-ttu-id="d5e51-102">Função PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="d5e51-102">PurifiedMixedState function</span></span>

<span data-ttu-id="d5e51-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d5e51-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d5e51-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d5e51-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d5e51-105">Retorna uma operação que prepara um Purification de um determinado estado misto.</span><span class="sxs-lookup"><span data-stu-id="d5e51-105">Returns an operation that prepares a a purification of a given mixed state.</span></span>
<span data-ttu-id="d5e51-106">Um "estado misto de purified" refere-se aos Estados do formulário | ψ ⟩ = σi √ Pi | i ⟩ | lixoi ⟩ especificado por um vetor de coeficientes {PI}.</span><span class="sxs-lookup"><span data-stu-id="d5e51-106">A "purified mixed state" refers to states of the form |ψ⟩ = Σᵢ √𝑝ᵢ |𝑖⟩ |garbageᵢ⟩ specified by a vector of coefficients {𝑝ᵢ}.</span></span> <span data-ttu-id="d5e51-107">Os Estados deste formulário podem ser reduzidos para Estados mistos ρ ≔ Pi | i ⟩ ⟨ i | rastreando o registro de "lixo" (ou seja, um estado misto que é diagonal na base computacional).</span><span class="sxs-lookup"><span data-stu-id="d5e51-107">States of this form can be reduced to mixed states ρ ≔ 𝑝ᵢ |𝑖⟩⟨𝑖| by tracing over the "garbage" register (that is, a mixed state that is diagonal in the computational basis).</span></span>

<span data-ttu-id="d5e51-108">Consulte https://arxiv.org/pdf/1805.03662.pdf?page=15 para mais discussões.</span><span class="sxs-lookup"><span data-stu-id="d5e51-108">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="d5e51-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5e51-109">Description</span></span>

<span data-ttu-id="d5e51-110">Usa a técnica de ROM Quantum para representar uma determinada matriz de densidade, retornando essa representação como uma operação de preparação de estado.</span><span class="sxs-lookup"><span data-stu-id="d5e51-110">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="d5e51-111">Em particular, dada uma lista de $N $ coeficientes $ \ alpha_j $, essa função retorna uma operação que usa a técnica de ROM da Quantum para preparar uma aproximação $ $ \begin{align} \tilde\rho = \ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} \end{align} $ $ do estado misto $ $ \begin{align} \rho = \ sum_ {j = 0} ^ {N-1} \ frac {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j}, \end{Align} $ $, em que cada $p _j $ é uma aproximação para o coeficiente determinado $ \ alpha_j $ de que $ $ \begin{align} \left | p_j-\frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ para cada $j $.</span><span class="sxs-lookup"><span data-stu-id="d5e51-111">In particular, given a list of $N$ coefficients $\alpha_j$, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="d5e51-112">Quando passou um registro de índice e um registro de qubits de lixo, inicialmente no estado $ \ket {0} \ket{00\cdots 0}, a operação retornada prepara ambos os registros para Purification de $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage} _J}, \end{align} $ $ para que a redefinição e desalocação do registro de lixo atue na preparação desejada para dentro do erro de destino $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="d5e51-112">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="d5e51-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5e51-113">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="d5e51-114">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d5e51-114">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d5e51-115">O erro de destino $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="d5e51-115">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="d5e51-116">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d5e51-116">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d5e51-117">Matriz de $N $ coeficientes especificando a probabilidade de Estados de base.</span><span class="sxs-lookup"><span data-stu-id="d5e51-117">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="d5e51-118">Números negativos $-\ alpha_j $ serão tratados como $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="d5e51-118">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="d5e51-119">Saída: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="d5e51-119">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="d5e51-120">Uma operação que prepara $ \tilde \rho $ como um Purification para um índice conjunta e registro de lixo.</span><span class="sxs-lookup"><span data-stu-id="d5e51-120">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e51-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5e51-121">Remarks</span></span>

<span data-ttu-id="d5e51-122">Os coeficientes fornecidos a essa operação são normalizados seguindo a norma 1, de modo que os coeficientes são sempre considerados para descrever uma distribuição de probabilidade categórica válida.</span><span class="sxs-lookup"><span data-stu-id="d5e51-122">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="d5e51-123">Referências</span><span class="sxs-lookup"><span data-stu-id="d5e51-123">References</span></span>

- <span data-ttu-id="d5e51-124">Codificação eletrônica de Spectra em circuitos Quantum com complexidade T linear Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru fosco, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="d5e51-124">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="d5e51-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d5e51-125">See Also</span></span>

- [<span data-ttu-id="d5e51-126">Microsoft. Quantum. Preparation. PurifiedMixedStateWithData</span><span class="sxs-lookup"><span data-stu-id="d5e51-126">Microsoft.Quantum.Preparation.PurifiedMixedStateWithData</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)