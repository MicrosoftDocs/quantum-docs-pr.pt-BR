---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Função decompostay
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855523"
---
# <a name="decomposedon-function"></a><span data-ttu-id="6a3c8-102">Função decompostay</span><span class="sxs-lookup"><span data-stu-id="6a3c8-102">DecomposedOn function</span></span>

<span data-ttu-id="6a3c8-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6a3c8-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6a3c8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a3c8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a3c8-105">Redação de uma permutação em uma variável</span><span class="sxs-lookup"><span data-stu-id="6a3c8-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="6a3c8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a3c8-106">Description</span></span>

<span data-ttu-id="6a3c8-107">Dada uma permutação $ \pi $ ( `perm` ) e um índice $i $ ( `index` ), esse método retorna três permutas $ ((\ pi_l, \ pi_r), \pi ') $ de forma que as imagens de $ \ pi_l $ e $ \ pi_r $ não alterem bits em seus elementos em índices diferentes de $i $ e imagens de $ \pi ' $ não altere o bit $i $ em seus elementos.</span><span class="sxs-lookup"><span data-stu-id="6a3c8-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="6a3c8-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a3c8-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="6a3c8-109">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6a3c8-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="6a3c8-110">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6a3c8-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="6a3c8-111">Saída: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="6a3c8-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>



## <a name="example"></a><span data-ttu-id="6a3c8-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6a3c8-112">Example</span></span>

<span data-ttu-id="6a3c8-113">Suponha que a entrada seja Perm = [0, 2, 3, 5, 7, 1, 4, 6] e índice = 0. em seguida, essa função computa três permutações com base na tabela a seguir, que lista a permutação `perm` em notação binária com elementos no grupo A e imagens no grupo D.  As colunas listam os índices de bits.</span><span class="sxs-lookup"><span data-stu-id="6a3c8-113">Assume that the input is perm = [0, 2, 3, 5, 7, 1, 4, 6] and index = 0, then this function computes three permutations based on the following table, which lists the permutation `perm` in binary notation with elements in group A and images in group D.  The columns list the bit indices.</span></span>

<span data-ttu-id="6a3c8-114">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="6a3c8-114">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="6a3c8-115">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-115">2 1 0</span></span> | <span data-ttu-id="6a3c8-116">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-116">2 1 0</span></span> | <span data-ttu-id="6a3c8-117">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-117">2 1 0</span></span> | <span data-ttu-id="6a3c8-118">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-118">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="6a3c8-119">0 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-119">0 0 0</span></span> |       |       | <span data-ttu-id="6a3c8-120">0 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-120">0 0 0</span></span> | <span data-ttu-id="6a3c8-121">0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-121">0</span></span>
| <span data-ttu-id="6a3c8-122">0 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-122">0 0 1</span></span> |       |       | <span data-ttu-id="6a3c8-123">0 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-123">0 1 0</span></span> | <span data-ttu-id="6a3c8-124">2</span><span class="sxs-lookup"><span data-stu-id="6a3c8-124">2</span></span>
| <span data-ttu-id="6a3c8-125">0 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-125">0 1 0</span></span> |       |       | <span data-ttu-id="6a3c8-126">0 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-126">0 1 1</span></span> | <span data-ttu-id="6a3c8-127">3</span><span class="sxs-lookup"><span data-stu-id="6a3c8-127">3</span></span>
| <span data-ttu-id="6a3c8-128">0 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-128">0 1 1</span></span> |       |       | <span data-ttu-id="6a3c8-129">1 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-129">1 0 1</span></span> | <span data-ttu-id="6a3c8-130">5</span><span class="sxs-lookup"><span data-stu-id="6a3c8-130">5</span></span>
| <span data-ttu-id="6a3c8-131">1 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-131">1 0 0</span></span> |       |       | <span data-ttu-id="6a3c8-132">1 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-132">1 1 1</span></span> | <span data-ttu-id="6a3c8-133">7</span><span class="sxs-lookup"><span data-stu-id="6a3c8-133">7</span></span>
| <span data-ttu-id="6a3c8-134">1 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-134">1 0 1</span></span> |       |       | <span data-ttu-id="6a3c8-135">0 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-135">0 0 1</span></span> | <span data-ttu-id="6a3c8-136">1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-136">1</span></span>
| <span data-ttu-id="6a3c8-137">1 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-137">1 1 0</span></span> |       |       | <span data-ttu-id="6a3c8-138">1 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-138">1 0 0</span></span> | <span data-ttu-id="6a3c8-139">4</span><span class="sxs-lookup"><span data-stu-id="6a3c8-139">4</span></span>
| <span data-ttu-id="6a3c8-140">1 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-140">1 1 1</span></span> |       |       | <span data-ttu-id="6a3c8-141">1 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-141">1 1 0</span></span> | <span data-ttu-id="6a3c8-142">6</span><span class="sxs-lookup"><span data-stu-id="6a3c8-142">6</span></span>

<span data-ttu-id="6a3c8-143">Todos os valores de índices diferentes de 0 (= índice) são copiados de a para B e de D para C.</span><span class="sxs-lookup"><span data-stu-id="6a3c8-143">All values for indices not equal to 0 (= index) are copied from A to B and from D to C.</span></span>

<span data-ttu-id="6a3c8-144">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="6a3c8-144">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="6a3c8-145">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-145">2 1 0</span></span> | <span data-ttu-id="6a3c8-146">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-146">2 1 0</span></span> | <span data-ttu-id="6a3c8-147">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-147">2 1 0</span></span> | <span data-ttu-id="6a3c8-148">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-148">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="6a3c8-149">0 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-149">0 0 0</span></span> | <span data-ttu-id="6a3c8-150">0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-150">0 0</span></span>   | <span data-ttu-id="6a3c8-151">0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-151">0 0</span></span>   | <span data-ttu-id="6a3c8-152">0 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-152">0 0 0</span></span> |
| <span data-ttu-id="6a3c8-153">0 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-153">0 0 1</span></span> | <span data-ttu-id="6a3c8-154">0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-154">0 0</span></span>   | <span data-ttu-id="6a3c8-155">0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-155">0 1</span></span>   | <span data-ttu-id="6a3c8-156">0 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-156">0 1 0</span></span> |
| <span data-ttu-id="6a3c8-157">0 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-157">0 1 0</span></span> | <span data-ttu-id="6a3c8-158">0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-158">0 1</span></span>   | <span data-ttu-id="6a3c8-159">0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-159">0 1</span></span>   | <span data-ttu-id="6a3c8-160">0 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-160">0 1 1</span></span> |
| <span data-ttu-id="6a3c8-161">0 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-161">0 1 1</span></span> | <span data-ttu-id="6a3c8-162">0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-162">0 1</span></span>   | <span data-ttu-id="6a3c8-163">1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-163">1 0</span></span>   | <span data-ttu-id="6a3c8-164">1 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-164">1 0 1</span></span> |
| <span data-ttu-id="6a3c8-165">1 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-165">1 0 0</span></span> | <span data-ttu-id="6a3c8-166">1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-166">1 0</span></span>   | <span data-ttu-id="6a3c8-167">1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-167">1 1</span></span>   | <span data-ttu-id="6a3c8-168">1 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-168">1 1 1</span></span> |
| <span data-ttu-id="6a3c8-169">1 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-169">1 0 1</span></span> | <span data-ttu-id="6a3c8-170">1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-170">1 0</span></span>   | <span data-ttu-id="6a3c8-171">0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-171">0 0</span></span>   | <span data-ttu-id="6a3c8-172">0 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-172">0 0 1</span></span> |
| <span data-ttu-id="6a3c8-173">1 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-173">1 1 0</span></span> | <span data-ttu-id="6a3c8-174">1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-174">1 1</span></span>   | <span data-ttu-id="6a3c8-175">1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-175">1 0</span></span>   | <span data-ttu-id="6a3c8-176">1 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-176">1 0 0</span></span> |
| <span data-ttu-id="6a3c8-177">1 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-177">1 1 1</span></span> | <span data-ttu-id="6a3c8-178">1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-178">1 1</span></span>   | <span data-ttu-id="6a3c8-179">1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-179">1 1</span></span>   | <span data-ttu-id="6a3c8-180">1 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-180">1 1 0</span></span> |

<span data-ttu-id="6a3c8-181">Em seguida, 0 é colocado para o primeiro elemento com um índice vazio na coluna 0 no bloco B e, em seguida, um 1 é colocado em B, onde o prefixo corresponde (no primeiro caso, a outra linha com os índices 0 0).</span><span class="sxs-lookup"><span data-stu-id="6a3c8-181">Next a 0 is placed for the first element with an empty index at column 0 in block B and then a 1 is placed in B where the prefix matches (in the first case the other row with indices 0 0).</span></span>
<span data-ttu-id="6a3c8-182">Depois, um 1 é adicionado na mesma linha no bloco C e, em seguida, um 0 para o prefixo correspondente no bloco C.  Esse processo é repetido, até que todos os índices tenham sido colocados na coluna 0 nos blocos B e C.</span><span class="sxs-lookup"><span data-stu-id="6a3c8-182">Afterwards, a 1 is added in the same row in block C, and then a 0 for the corresponding prefix in block C.  This process is repeated, until all indices have been placed in column 0 in blocks B and C.</span></span>

<span data-ttu-id="6a3c8-183">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="6a3c8-183">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="6a3c8-184">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-184">2 1 0</span></span> | <span data-ttu-id="6a3c8-185">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-185">2 1 0</span></span> | <span data-ttu-id="6a3c8-186">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-186">2 1 0</span></span> | <span data-ttu-id="6a3c8-187">2 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-187">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="6a3c8-188">0 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-188">0 0 0</span></span> | <span data-ttu-id="6a3c8-189">0 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-189">0 0 0</span></span> | <span data-ttu-id="6a3c8-190">0 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-190">0 0 0</span></span> | <span data-ttu-id="6a3c8-191">0 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-191">0 0 0</span></span> |
| <span data-ttu-id="6a3c8-192">0 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-192">0 0 1</span></span> | <span data-ttu-id="6a3c8-193">0 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-193">0 0 1</span></span> | <span data-ttu-id="6a3c8-194">0 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-194">0 1 1</span></span> | <span data-ttu-id="6a3c8-195">0 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-195">0 1 0</span></span> |
| <span data-ttu-id="6a3c8-196">0 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-196">0 1 0</span></span> | <span data-ttu-id="6a3c8-197">0 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-197">0 1 0</span></span> | <span data-ttu-id="6a3c8-198">0 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-198">0 1 0</span></span> | <span data-ttu-id="6a3c8-199">0 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-199">0 1 1</span></span> |
| <span data-ttu-id="6a3c8-200">0 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-200">0 1 1</span></span> | <span data-ttu-id="6a3c8-201">0 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-201">0 1 1</span></span> | <span data-ttu-id="6a3c8-202">1 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-202">1 0 1</span></span> | <span data-ttu-id="6a3c8-203">1 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-203">1 0 1</span></span> |
| <span data-ttu-id="6a3c8-204">1 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-204">1 0 0</span></span> | <span data-ttu-id="6a3c8-205">1 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-205">1 0 0</span></span> | <span data-ttu-id="6a3c8-206">1 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-206">1 1 0</span></span> | <span data-ttu-id="6a3c8-207">1 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-207">1 1 1</span></span> |
| <span data-ttu-id="6a3c8-208">1 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-208">1 0 1</span></span> | <span data-ttu-id="6a3c8-209">1 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-209">1 0 1</span></span> | <span data-ttu-id="6a3c8-210">0 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-210">0 0 1</span></span> | <span data-ttu-id="6a3c8-211">0 0 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-211">0 0 1</span></span> |
| <span data-ttu-id="6a3c8-212">1 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-212">1 1 0</span></span> | <span data-ttu-id="6a3c8-213">1 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-213">1 1 0</span></span> | <span data-ttu-id="6a3c8-214">1 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-214">1 0 0</span></span> | <span data-ttu-id="6a3c8-215">1 0 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-215">1 0 0</span></span> |
| <span data-ttu-id="6a3c8-216">1 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-216">1 1 1</span></span> | <span data-ttu-id="6a3c8-217">1 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-217">1 1 1</span></span> | <span data-ttu-id="6a3c8-218">1 1 1</span><span class="sxs-lookup"><span data-stu-id="6a3c8-218">1 1 1</span></span> | <span data-ttu-id="6a3c8-219">1 1 0</span><span class="sxs-lookup"><span data-stu-id="6a3c8-219">1 1 0</span></span> |

<span data-ttu-id="6a3c8-220">Podemos ler três novas permutações da tabela:</span><span class="sxs-lookup"><span data-stu-id="6a3c8-220">We can read three new permutations from the table:</span></span>

- <span data-ttu-id="6a3c8-221">$ \ pi_l $ com elementos em A, imagens em B (esquerda)</span><span class="sxs-lookup"><span data-stu-id="6a3c8-221">$\pi_l$ with elements in A, images in B (left)</span></span>
- <span data-ttu-id="6a3c8-222">$ \ pi_r $ com elementos em D, imagens em C (direita)</span><span class="sxs-lookup"><span data-stu-id="6a3c8-222">$\pi_r$ with elements in D, images in C (right)</span></span>
- <span data-ttu-id="6a3c8-223">$ \pi ' $ com elementos em B, imagens em C (restante)</span><span class="sxs-lookup"><span data-stu-id="6a3c8-223">$\pi'$  with elements in B, images in C (remainder)</span></span>

<span data-ttu-id="6a3c8-224">Observe que os valores de bit de design não mudam em $ \ pi_l $ e $ \ pi_r $ para os índices 1 e 2, e os valores de bits não são alterados em $ \ pi_ ' $ para o índice 0.</span><span class="sxs-lookup"><span data-stu-id="6a3c8-224">Note that by design bit values do not change in $\pi_l$ and $\pi_r$ for indices 1 and 2, and bit values do not change for in $\pi_'$ for index 0.</span></span>  <span data-ttu-id="6a3c8-225">Observe também que $ \ pi_l $ e $ \ pi_r $ devem ser inversos.</span><span class="sxs-lookup"><span data-stu-id="6a3c8-225">Also note that $\pi_l$ and $\pi_r$ must be self-inverse.</span></span>

<span data-ttu-id="6a3c8-226">As permutações derivadas e retornadas são: esquerda = [0, 1, 2, 3, 4, 5, 6, 7] Right = [0, 1, 3, 2, 4, 5, 7, 6] resto = [0, 3, 2, 5, 6, 1, 4, 7]</span><span class="sxs-lookup"><span data-stu-id="6a3c8-226">The derived and returned permutations are: left      = [0, 1, 2, 3, 4, 5, 6, 7] right     = [0, 1, 3, 2, 4, 5, 7, 6] remainder = [0, 3, 2, 5, 6, 1, 4, 7]</span></span>