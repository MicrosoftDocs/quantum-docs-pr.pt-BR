---
title: Medições de Pauli
description: Saiba como trabalhar com operações de medição de Pauli de qubit única e múltipla.
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: 7f10c4ad5eb325da97552d60ff47ea89a699f08d
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269466"
---
# <a name="pauli-measurements"></a><span data-ttu-id="06952-103">Medições de Pauli</span><span class="sxs-lookup"><span data-stu-id="06952-103">Pauli Measurements</span></span>

<span data-ttu-id="06952-104">Nas discussões anteriores, concentramos-se em medidas de base computacional.</span><span class="sxs-lookup"><span data-stu-id="06952-104">In the previous discussions, we have focused on computational basis measurements.</span></span>
<span data-ttu-id="06952-105">Na verdade, há outras medidas comuns que ocorrem na computação Quantum que, de uma perspectiva de notação, são convenientes para expressar em termos de medidas de base computacional.</span><span class="sxs-lookup"><span data-stu-id="06952-105">In fact, there are other common measurements that occur in quantum computing that, from a notational perspective, are convenient to express in terms of computational basis measurements.</span></span>
<span data-ttu-id="06952-106">À medida que você trabalha com o Q #, o tipo mais comum de medidas que você encontrará provavelmente será *Pauli medições*, que generalizam as medidas de base computacional para incluir medidas em outras bases e de paridade entre diferentes qubits.</span><span class="sxs-lookup"><span data-stu-id="06952-106">As you work with Q#, the most common kind of measurements that you'll run into will likely be *Pauli measurements*, which generalize computational basis measurements to include measurements in other bases, and of parity between different qubits.</span></span>
<span data-ttu-id="06952-107">Nesses casos, é comum discutir a medição de um operador Pauli, em geral, um operador como $X, Y, Z $ ou $Z \otimes Z, x \otimes x x \otimes Y $ e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="06952-107">In such cases, it is common to discuss measuring a Pauli operator, in general an operator such as $X,Y,Z$ or $Z\otimes Z, X\otimes X, X\otimes Y$, and so forth.</span></span>

> [!TIP]
> <span data-ttu-id="06952-108">Em Q #, os operadores qubit Pauli geralmente são representados por matrizes do tipo `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="06952-108">In Q#, multi-qubit Pauli operators are generally represented by arrays of type `Pauli[]`.</span></span>
> <span data-ttu-id="06952-109">Por exemplo, para representar $X \otimes Z \otimes Y $ , você pode usar a matriz `[PauliX, PauliZ, PauliY]` .</span><span class="sxs-lookup"><span data-stu-id="06952-109">For example, to represent $X \otimes Z \otimes Y$, you can use the array `[PauliX, PauliZ, PauliY]`.</span></span>

<span data-ttu-id="06952-110">Discutir a medição em termos de operadores Pauli é especialmente comum no subcampo de correção de erro Quantum.</span><span class="sxs-lookup"><span data-stu-id="06952-110">Discussing measurement in terms of Pauli operators is especially common in the subfield of quantum error correction.</span></span>
<span data-ttu-id="06952-111">Em Q #, seguimos uma convenção semelhante; Agora, explicamos essa exibição alternativa de medidas.</span><span class="sxs-lookup"><span data-stu-id="06952-111">In Q#, we follow a similar convention; we now explain this alternative view of measurements.</span></span>

<span data-ttu-id="06952-112">Antes de se aprofundar nos detalhes de como pensar em uma medida Pauli, é útil pensar em que a medição de um único qubit dentro de um computador Quantum faz o estado Quantum.</span><span class="sxs-lookup"><span data-stu-id="06952-112">Before delving into the details of how to think of a Pauli measurement, it is useful to think about what measuring a single qubit inside a quantum computer does to the quantum state.</span></span>
<span data-ttu-id="06952-113">Imagine que tenhamos um estado de $ quantum $n-qubit; em seguida, medindo uma qubit imediatamente as regras de metade das possibilidades de $2 ^ n $ que o estado pode estar.</span><span class="sxs-lookup"><span data-stu-id="06952-113">Imagine that we have an $n$-qubit quantum state; then measuring one qubit immediately rules out half of the $2^n$ possibilities that state could be in.</span></span>
<span data-ttu-id="06952-114">Em outras palavras, a medida projeta o estado da Quantum em um dos dois espaços.</span><span class="sxs-lookup"><span data-stu-id="06952-114">In other words, the measurement projects the quantum state onto one of two half-spaces.</span></span>
<span data-ttu-id="06952-115">Podemos generalizar a maneira como pensamos na medição para refletir essa intuição.</span><span class="sxs-lookup"><span data-stu-id="06952-115">We can generalize the way we think about measurement to reflect this intuition.</span></span>

<span data-ttu-id="06952-116">Para identificar esses subespaços de forma concisa, precisamos de uma linguagem para descreve-los.</span><span class="sxs-lookup"><span data-stu-id="06952-116">In order to concisely identify these subspaces, we need a language for describing them.</span></span>
<span data-ttu-id="06952-117">Uma maneira de descrever os dois subespaços é especificando-os por meio de uma matriz que tem apenas duas eigenvalues exclusivas, tomadas pela Convenção para ser $ \pm 1 $ .</span><span class="sxs-lookup"><span data-stu-id="06952-117">One way to describe the two subspaces is by specifying them through a matrix that just has two unique eigenvalues, taken by convention to be $\pm 1$.</span></span>
<span data-ttu-id="06952-118">Para obter um exemplo simples de descrição de subespaços dessa forma, considere $Z $ :</span><span class="sxs-lookup"><span data-stu-id="06952-118">For a simple example of describing subspaces in this way, consider $Z$:</span></span>

<span data-ttu-id="06952-119">US $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="06952-119">$$ \begin{align}</span></span>
  <span data-ttu-id="06952-120">Z & = \begin{ bmatrix } 1 & 0 \\ \\ 0 &-1 \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="06952-120">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="06952-121">\end{align}</span><span class="sxs-lookup"><span data-stu-id="06952-121">\end{align}</span></span>
$$

<span data-ttu-id="06952-122">Lendo os elementos diagonais da matriz Pauli-$Z $ , podemos ver que $Z $ tem dois eigenvectors, $ \ket{0 } $ e $ \ket{1 } $, com eigenvalues $ \pm 1 correspondente $ .</span><span class="sxs-lookup"><span data-stu-id="06952-122">By reading the diagonal elements of the Pauli-$Z$ matrix, we can see that $Z$ has two eigenvectors, $\ket{0}$ and $\ket{1}$, with corresponding eigenvalues $\pm 1$.</span></span>
<span data-ttu-id="06952-123">Portanto, se medirmos o qubit e obtivermos `Zero` (correspondente ao estado $ \ket{0 } $), sabemos que o estado de nosso qubit é uma eigenstate $ + 1 $ do $ operador $Z.</span><span class="sxs-lookup"><span data-stu-id="06952-123">Thus, if we measure the qubit and obtain `Zero` (corresponding to the state $\ket{0}$), we know that the state of our qubit is a $+1$ eigenstate of the $Z$ operator.</span></span>
<span data-ttu-id="06952-124">Da mesma forma, se obtivermos `One` , sabemos que o estado de nosso qubit é um eigenstate $-1 $ de $Z $ .</span><span class="sxs-lookup"><span data-stu-id="06952-124">Similarly, if we obtain `One`, we know that the state of our qubit is a $-1$ eigenstate of $Z$.</span></span>
<span data-ttu-id="06952-125">Esse processo é mencionado na linguagem de medidas Pauli como "medindo Pauli $Z $ " e é totalmente equivalente a executar uma medição de base computacional.</span><span class="sxs-lookup"><span data-stu-id="06952-125">This process is referred to in the language of Pauli measurements as "measuring Pauli $Z$," and is entirely equivalent to performing a computational basis measurement.</span></span>

<span data-ttu-id="06952-126">Qualquer \times matriz $2 2 $ que é uma transformação unitário de $Z $ também satisfaz a esses critérios.</span><span class="sxs-lookup"><span data-stu-id="06952-126">Any $2\times 2$ matrix that is a unitary transformation of $Z$ also satisfies this criteria.</span></span>
<span data-ttu-id="06952-127">Ou seja, também poderíamos usar uma matriz $A = U ^ \dagger Z U $ , em que $U $ é qualquer outra matriz de unitário, para fornecer uma matriz que define os dois resultados de uma medição em seu $ \pm 1 $ eigenvectors.</span><span class="sxs-lookup"><span data-stu-id="06952-127">That is, we could also use a matrix $A=U^\dagger Z U$, where $U$ is any other unitary matrix, to give a matrix that defines the two outcomes of a measurement in its $\pm 1$ eigenvectors.</span></span>
<span data-ttu-id="06952-128">A notação de medidas Pauli faz referência a essa equivalência unitário identificando as medidas $X, Y, Z $ como medidas equivalentes que um pode fazer para obter informações de um qubit.</span><span class="sxs-lookup"><span data-stu-id="06952-128">The notation of Pauli measurements references this unitary equivalence by identifying $X,Y,Z$ measurements as equivalent measurements that one could do to gain information from a qubit.</span></span>
<span data-ttu-id="06952-129">Essas medidas são fornecidas abaixo para sua conveniência.</span><span class="sxs-lookup"><span data-stu-id="06952-129">These measurements are given below for convenience.</span></span>


|<span data-ttu-id="06952-130">Medição de Pauli</span><span class="sxs-lookup"><span data-stu-id="06952-130">Pauli Measurement</span></span>  |<span data-ttu-id="06952-131">Transformação unitário</span><span class="sxs-lookup"><span data-stu-id="06952-131">Unitary transformation</span></span>  |
|-------------------|------------------------|
| <span data-ttu-id="06952-132">$Z$</span><span class="sxs-lookup"><span data-stu-id="06952-132">$Z$</span></span>               | <span data-ttu-id="06952-133">US $ \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-133">$\boldone$</span></span>             |
| <span data-ttu-id="06952-134">$X$</span><span class="sxs-lookup"><span data-stu-id="06952-134">$X$</span></span>               | <span data-ttu-id="06952-135">$H$</span><span class="sxs-lookup"><span data-stu-id="06952-135">$H$</span></span>                    |
| <span data-ttu-id="06952-136">$Y$</span><span class="sxs-lookup"><span data-stu-id="06952-136">$Y$</span></span>               | <span data-ttu-id="06952-137">$HS ^ {\dagger}$</span><span class="sxs-lookup"><span data-stu-id="06952-137">$HS^{\dagger}$</span></span>         |

<span data-ttu-id="06952-138">Ou seja, usar essa linguagem, "Measure $Y $ " é equivalente a aplicar $HS ^ \dagger $ e, em seguida, medir na base computacional, em que [`S`](xref:microsoft.quantum.intrinsic.s) é uma operação de Quantum intrínseca às vezes chamada de "portão de fase" e pode ser simulada pela matriz unitário</span><span class="sxs-lookup"><span data-stu-id="06952-138">That is, using this language, "measure $Y$" is equivalent to applying $HS^\dagger$ and then measuring in the computational basis, where [`S`](xref:microsoft.quantum.intrinsic.s) is an intrinsic quantum operation sometimes called the "phase gate," and can be simulated by the unitary matrix</span></span>

<span data-ttu-id="06952-139">US $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="06952-139">$$ \begin{align}</span></span>
    <span data-ttu-id="06952-140">S = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="06952-140">S = \begin{bmatrix}</span></span>
        <span data-ttu-id="06952-141">1 & 0 \\ \\ 0 & \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="06952-141">1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="06952-142">\end{align}</span><span class="sxs-lookup"><span data-stu-id="06952-142">\end{align}</span></span>
$$

<span data-ttu-id="06952-143">Também é equivalente a aplicar $HS ^ \dagger $ ao vetor de estado Quantum e, em seguida, medir $Z $ , de modo que a seguinte operação seja equivalente a `Measure([PauliY], [q])` :</span><span class="sxs-lookup"><span data-stu-id="06952-143">It is also equivalent to applying $HS^\dagger$ to the quantum state vector and then measuring $Z$, such that the following operation is equivalent to `Measure([PauliY], [q])`:</span></span>

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

<span data-ttu-id="06952-144">O estado correto seria então encontrado transformando de volta para a base computacional, que valores para aplicar $SH $ ao vetor de estado Quantum; no trecho acima, a transformação de volta para a base computacional é manipulada automaticamente pelo uso do `within … apply` bloco.</span><span class="sxs-lookup"><span data-stu-id="06952-144">The correct state would then be found by transforming back to the computational basis, which amounts to applying $SH$ to the quantum state vector; in the above snippet, the transformation back to the computational basis is handled automatically by the use of the `within … apply` block.</span></span>

<span data-ttu-id="06952-145">Em Q #, dizemos que o resultado---ou seja, as informações clássicas extraídas da interação com o estado---são dadas por um `Result` valor $j na \\ {\Texttt{zero } , \texttt{One } \\ } $ indicando se o resultado está na eigenspace de $ (-1) ^ j $ do operador Pauli medido.</span><span class="sxs-lookup"><span data-stu-id="06952-145">In Q#, we say the outcome---that is, the classical information extracted from interacting with the state---is given by a `Result` value $j \in \\{\texttt{Zero}, \texttt{One}\\}$ indicating if the result is in the $(-1)^j$ eigenspace of the Pauli operator measured.</span></span>


## <a name="multiple-qubit-measurements"></a><span data-ttu-id="06952-146">Medições de várias qubit</span><span class="sxs-lookup"><span data-stu-id="06952-146">Multiple-qubit measurements</span></span>

<span data-ttu-id="06952-147">As medições de operadores qubit Pauli são definidas da mesma forma, como visto em:</span><span class="sxs-lookup"><span data-stu-id="06952-147">Measurements of multi-qubit Pauli operators are defined similarly, as seen from:</span></span>

<span data-ttu-id="06952-148">$ $ Z \otimes z = \begin{ bmatrix } 1 &0 &0&0 \\\\ 0 & -1&0&0 \\\\ 0&0 & -1&0 \\\\ 0&0&0&1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="06952-148">$$ Z\otimes Z = \begin{bmatrix}1 &0 &0&0\\\\  0&-1&0&0\\\\ 0&0&-1&0\\\\ 0&0&0&1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="06952-149">Assim, os produtos tensor de dois operadores Pauli-$Z $ formam uma matriz composta de dois espaços consistindo em $ + 1 $ e $-1 $ eigenvalues.</span><span class="sxs-lookup"><span data-stu-id="06952-149">Thus the tensor products of two Pauli-$Z$ operators forms a matrix composed of two spaces consisting of $+1$ and $-1$ eigenvalues.</span></span>
<span data-ttu-id="06952-150">Assim como no caso de qubit único, ambos constituem um meio-espaço que significa que metade do espaço de vetor acessível pertence ao $ + 1 $ eigenspace e à metade restante para o $-1 $ eigenspace.</span><span class="sxs-lookup"><span data-stu-id="06952-150">As with the single-qubit case, both constitute a half-space meaning that half of the accessible vector space belongs to the $+1$ eigenspace and the remaining half to the $-1$ eigenspace.</span></span>
<span data-ttu-id="06952-151">Em geral, é fácil ver a definição do produto tensor que qualquer produto tensor de operadores de $Z de Pauli $ e a identidade também obedece a isso.</span><span class="sxs-lookup"><span data-stu-id="06952-151">In general, it is easy to see from the definition of the tensor product that any tensor product of Pauli-$Z$ operators and the identity also obeys this.</span></span>
<span data-ttu-id="06952-152">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="06952-152">For example,</span></span>

<span data-ttu-id="06952-153">US $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="06952-153">$$ \begin{align}</span></span>
    <span data-ttu-id="06952-154">Z \otimes \boldone = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="06952-154">Z \otimes \boldone = \begin{bmatrix}</span></span>
        <span data-ttu-id="06952-155">1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 &-1 & 0 \\ \\ 0 & 0 & 0 &-1 \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="06952-155">1 &  0 &  0 &  0 \\\\ 0 &  1 &  0 &  0 \\\\ 0 &  0 & -1 &  0 \\\\ 0 &  0 &  0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="06952-156">\end{align}</span><span class="sxs-lookup"><span data-stu-id="06952-156">\end{align}</span></span>
$$

<span data-ttu-id="06952-157">Como antes, qualquer transformação unitário dessas matrizes também descreve dois espaços de meio rotulados por $ \pm 1 $ eigenvalues.</span><span class="sxs-lookup"><span data-stu-id="06952-157">As before, any unitary transformation of such matrices also describes two half-spaces labeled by $\pm 1$ eigenvalues.</span></span>
<span data-ttu-id="06952-158">Por exemplo, $X \otimes X = h \otimes h (z \otimes z) h \otimes h $ da identidade que $Z = HxH $ .</span><span class="sxs-lookup"><span data-stu-id="06952-158">For example, $X\otimes X = H\otimes H(Z\otimes Z)H\otimes H$  from the identity that $Z=HXH$.</span></span>
<span data-ttu-id="06952-159">Semelhante ao caso One-qubit, todas as medidas de Pauli qubit podem ser escritas como $U ^ \dagger (Z \otimes \id) U para as $ \times matrizes de $4 4 $ $U $ .</span><span class="sxs-lookup"><span data-stu-id="06952-159">Similar to the one-qubit case, all two-qubit Pauli-measurements can be written as $U^\dagger (Z\otimes \id) U$ for $4\times 4$ unitary matrices $U$.</span></span> <span data-ttu-id="06952-160">Enumeramos as transformações na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="06952-160">We enumerate the transformations in the following table.</span></span>

> [!NOTE]
> <span data-ttu-id="06952-161">Na tabela a seguir, usamos $ \operatorname{SWAP } $ para indicar a matriz $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="06952-161">In the table below, we use $\operatorname{SWAP}$ to indicate the matrix $$ \begin{align}</span></span>
>     <span data-ttu-id="06952-162">\operatorname{SWAP } & = \left (\begin{Matrix}</span><span class="sxs-lookup"><span data-stu-id="06952-162">\operatorname{SWAP} & = \left(\begin{matrix}</span></span>
>         <span data-ttu-id="06952-163">1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{Matrix } \right) \end{align}</span><span class="sxs-lookup"><span data-stu-id="06952-163">1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{matrix}\right) \end{align}</span></span>
> <span data-ttu-id="06952-164">$ $ usado para simular a operação intrínseca [`SWAP`](xref:microsoft.quantum.intrinsic) .</span><span class="sxs-lookup"><span data-stu-id="06952-164">$$ used to simulate the intrinsic operation [`SWAP`](xref:microsoft.quantum.intrinsic).</span></span>

|<span data-ttu-id="06952-165">Medição de Pauli</span><span class="sxs-lookup"><span data-stu-id="06952-165">Pauli Measurement</span></span>     |<span data-ttu-id="06952-166">Transformação unitário</span><span class="sxs-lookup"><span data-stu-id="06952-166">Unitary transformation</span></span>  |
|----------------------|------------------------|
| <span data-ttu-id="06952-167">$Z \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-167">$Z \otimes \boldone$</span></span> | <span data-ttu-id="06952-168">US $ \boldone \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-168">$\boldone \otimes \boldone$</span></span> |
| <span data-ttu-id="06952-169">$Z \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-169">$Z\otimes \boldone$</span></span> | <span data-ttu-id="06952-170">US $ \boldone \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-170">$\boldone\otimes \boldone$</span></span> |
| <span data-ttu-id="06952-171">$X \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-171">$X\otimes \boldone$</span></span> | <span data-ttu-id="06952-172">$H \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-172">$H\otimes \boldone$</span></span> |
| <span data-ttu-id="06952-173">$Y \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-173">$Y\otimes \boldone$</span></span> | <span data-ttu-id="06952-174">$HS ^ \dagger \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="06952-174">$HS^\dagger\otimes \boldone$</span></span> |
| <span data-ttu-id="06952-175">US $ \boldone \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="06952-175">$\boldone \otimes Z$</span></span> | <span data-ttu-id="06952-176">US $ \operatorname{SWAP}$</span><span class="sxs-lookup"><span data-stu-id="06952-176">$\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="06952-177">US $ \boldone \otimes X$</span><span class="sxs-lookup"><span data-stu-id="06952-177">$\boldone \otimes X$</span></span> | <span data-ttu-id="06952-178">US $ (H \otimes \boldone) \operatorname{swap}$</span><span class="sxs-lookup"><span data-stu-id="06952-178">$(H\otimes \boldone)\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="06952-179">US $ \boldone \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="06952-179">$\boldone \otimes Y$</span></span> | <span data-ttu-id="06952-180">US $ (HS ^ \dagger \otimes \boldone) \operatorname{swap}$</span><span class="sxs-lookup"><span data-stu-id="06952-180">$(HS^\dagger\otimes \boldone)\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="06952-181">\otimesZ $Z$</span><span class="sxs-lookup"><span data-stu-id="06952-181">$Z\otimes Z$</span></span> | <span data-ttu-id="06952-182">US $ \operatorname{CNOT } \_ {10}$</span><span class="sxs-lookup"><span data-stu-id="06952-182">$\operatorname{CNOT}\_{10}$</span></span> |
| <span data-ttu-id="06952-183">\otimesZ $X$</span><span class="sxs-lookup"><span data-stu-id="06952-183">$X\otimes Z$</span></span> | <span data-ttu-id="06952-184">$ \operatorname{CNOT } \_ {10 } (H \otimes \boldone) $</span><span class="sxs-lookup"><span data-stu-id="06952-184">$\operatorname{CNOT}\_{10}(H\otimes \boldone)$</span></span> |
| <span data-ttu-id="06952-185">\otimesZ $Y$</span><span class="sxs-lookup"><span data-stu-id="06952-185">$Y\otimes Z$</span></span> | <span data-ttu-id="06952-186">$ \operatorname{CNOT } \_ {10 } (HS ^ \dagger \otimes \boldone) $</span><span class="sxs-lookup"><span data-stu-id="06952-186">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes \boldone)$</span></span> |
| <span data-ttu-id="06952-187">$Z \otimes X$</span><span class="sxs-lookup"><span data-stu-id="06952-187">$Z\otimes X$</span></span> | <span data-ttu-id="06952-188">$ \operatorname{CNOT } \_ {10 } (\boldone \otimes H) $</span><span class="sxs-lookup"><span data-stu-id="06952-188">$\operatorname{CNOT}\_{10}(\boldone\otimes H)$</span></span> |
| <span data-ttu-id="06952-189">$X \otimes X$</span><span class="sxs-lookup"><span data-stu-id="06952-189">$X\otimes X$</span></span> | <span data-ttu-id="06952-190">$ \operatorname{CNOT } \_ {10 } (h \otimes h) $</span><span class="sxs-lookup"><span data-stu-id="06952-190">$\operatorname{CNOT}\_{10}(H\otimes H)$</span></span> |
| <span data-ttu-id="06952-191">$Y \otimes X$</span><span class="sxs-lookup"><span data-stu-id="06952-191">$Y\otimes X$</span></span> | <span data-ttu-id="06952-192">$ \operatorname{CNOT } \_ {10 } (HS ^ \dagger \otimes H) $</span><span class="sxs-lookup"><span data-stu-id="06952-192">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes H)$</span></span> |
| <span data-ttu-id="06952-193">$Z \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="06952-193">$Z\otimes Y$</span></span> | <span data-ttu-id="06952-194">$ \operatorname{CNOT } \_ {10 } (\boldone \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="06952-194">$\operatorname{CNOT}\_{10}(\boldone \otimes HS^\dagger)$</span></span> |
| <span data-ttu-id="06952-195">$X \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="06952-195">$X\otimes Y$</span></span> | <span data-ttu-id="06952-196">$ \operatorname{CNOT } \_ {10 } (H \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="06952-196">$\operatorname{CNOT}\_{10}(H\otimes HS^\dagger)$</span></span> |
| <span data-ttu-id="06952-197">$Y \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="06952-197">$Y\otimes Y$</span></span> | <span data-ttu-id="06952-198">$ \operatorname{CNOT } \_ {10 } (HS ^ \dagger \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="06952-198">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes HS^\dagger)$</span></span> |

<span data-ttu-id="06952-199">Aqui, a [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) operação é exibida pelo seguinte motivo.</span><span class="sxs-lookup"><span data-stu-id="06952-199">Here, the [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) operation appears for the following reason.</span></span>
<span data-ttu-id="06952-200">Cada medida de Pauli que não inclui a matriz $ \boldone $ é equivalente a um unitário para $Z \otimes Z $ pelo raciocínio acima.</span><span class="sxs-lookup"><span data-stu-id="06952-200">Each Pauli measurement that does not include the $\boldone$ matrix is equivalent up to a unitary to $Z\otimes Z$ by the above reasoning.</span></span>
<span data-ttu-id="06952-201">O eigenvalues da $Z \otimes Z $ só depende da paridade do qubits que compõe cada vetor base computacional, e as operações controladas não servem para computar essa paridade e armazená-las no primeiro bit.</span><span class="sxs-lookup"><span data-stu-id="06952-201">The eigenvalues of $Z\otimes Z$ only depend on the parity of the qubits that comprise each computational basis vector, and the controlled-not operations serve to compute this parity and store it in the first bit.</span></span>
<span data-ttu-id="06952-202">Depois que o primeiro bit é medido, podemos recuperar a identidade do espaço resultante, que é equivalente a medir o operador Pauli.</span><span class="sxs-lookup"><span data-stu-id="06952-202">Then once the first bit is measured, we can recover the identity of the resultant half-space, which is equivalent to measuring the Pauli operator.</span></span>

<span data-ttu-id="06952-203">Uma observação adicional: embora possa ser tentador pressupor que medir $Z \otimes Z $ é o mesmo que medir sequencialmente $Z \otimes \mathbb{1 } $ e, em seguida, $ \mathbb{1 } \otimes Z $ , essa suposição seria falsa.</span><span class="sxs-lookup"><span data-stu-id="06952-203">One additional note: while it may be tempting to assume that measuring $Z\otimes Z$ is the same as sequentially measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$, this assumption would be false.</span></span>
<span data-ttu-id="06952-204">O motivo é que medir $Z \otimes $ projetos Z o estado da Quantum na eigenstate de $ + 1 $ ou $-1 $ desses operadores.</span><span class="sxs-lookup"><span data-stu-id="06952-204">The reason is that measuring $Z\otimes Z$ projects the quantum state into either the $+1$ or $-1$ eigenstate of these operators.</span></span>
<span data-ttu-id="06952-205">Medindo $Z \otimes \mathbb{1 } $ e, em seguida, $ \Mathbb{1 } \otimes Z $ projeta o vetor de estado Quantum primeiro em um semestre de $Z \otimes \mathbb{1 } $ e, em seguida, em um semestre de $ \mathbb{1 } \otimes Z $ . Como há quatro vetores de base computacional, a execução de ambas as medidas reduz o estado para um quarto de espaço e, portanto, reduz-a para um único vetor de computação.</span><span class="sxs-lookup"><span data-stu-id="06952-205">Measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$ projects the quantum state vector first onto a half space of $Z\otimes \mathbb{1}$ and then onto a half space of $\mathbb{1} \otimes Z$. As there are four computational basis vectors, performing both measurements reduces the state to a quarter-space and hence reduces it to a single computational basis vector.</span></span>

## <a name="correlations-between-qubits"></a><span data-ttu-id="06952-206">Correlações entre qubits</span><span class="sxs-lookup"><span data-stu-id="06952-206">Correlations between qubits</span></span>
<span data-ttu-id="06952-207">Outra maneira de observar a medição de produtos tensor de matrizes Pauli, como $X \otimes X $ ou $Z \otimes Z, $ é que essas medidas permitem que você examine as informações armazenadas nas correlações entre os dois qubits.</span><span class="sxs-lookup"><span data-stu-id="06952-207">Another way of looking at measuring tensor products of Pauli matrices such as $X\otimes X$ or $Z\otimes Z$ is that these measurements let you look at information stored in the correlations between the two qubits.</span></span>
<span data-ttu-id="06952-208">Medir $X \otimes \id $ permite que você examine as informações armazenadas localmente no primeiro qubit.</span><span class="sxs-lookup"><span data-stu-id="06952-208">Measuring $X\otimes \id$ lets you look at information that is locally stored in the first qubit.</span></span>
<span data-ttu-id="06952-209">Embora os dois tipos de medidas sejam igualmente valiosos na computação Quantum, o primeiro ilumina o poder da computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="06952-209">While both types of measurements are equally valuable in quantum computing, the former illuminates the power of quantum computing.</span></span>
<span data-ttu-id="06952-210">Ele revela que, na computação Quantum, geralmente as informações que você deseja aprender não são armazenadas em nenhum único qubit, mas armazenadas não localmente em todas as qubits de uma vez e, portanto, apenas examinando-as por meio de uma medida conjunta (por exemplo, $Z \otimes Z $ ) faz com que essas informações sejam manifestadas.</span><span class="sxs-lookup"><span data-stu-id="06952-210">It reveals that in quantum computing, often the information you wish to learn is not stored in any single qubit but rather stored non-locally in all the qubits at once, and therefore only by looking at it through a joint measurement (e.g. $Z\otimes Z$) does this information become manifest.</span></span>

<span data-ttu-id="06952-211">Por exemplo, na correção de erros, muitas vezes desejamos saber qual erro ocorreu ao aprender nada sobre o estado que estamos tentando proteger.</span><span class="sxs-lookup"><span data-stu-id="06952-211">For example, in error correction, we often wish to learn what error occurred while learning nothing about the state that we're trying to protect.</span></span>
<span data-ttu-id="06952-212">O [exemplo de código de inversão de bits](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) mostra um exemplo de como você pode fazer isso usando medidas como $Z \otimes Z \otimes \id $ e $ \id \Otimes z \otimes z $ .</span><span class="sxs-lookup"><span data-stu-id="06952-212">The [bit-flip code sample](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) shows an example of how you can do that using measurements like $Z \otimes Z \otimes \id$ and $\id \otimes Z \otimes Z$.</span></span>
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

<span data-ttu-id="06952-213">Operadores Pauli arbitrários, como $X \otimes Y \Otimes Z \otimes \boldone, $ também podem ser medidos.</span><span class="sxs-lookup"><span data-stu-id="06952-213">Arbitrary Pauli operators such as $X\otimes Y \otimes Z \otimes \boldone$ can also be measured.</span></span>
<span data-ttu-id="06952-214">Todos esses produtos tensor de operadores Pauli têm apenas duas eigenvalues $ \pm 1 $ e ambas as eigenspaces constituem metade de espaços de todo o espaço de vetor.</span><span class="sxs-lookup"><span data-stu-id="06952-214">All such tensor products of Pauli operators have only two eigenvalues $\pm 1$ and both eigenspaces constitute half-spaces of the entire vector space.</span></span>
<span data-ttu-id="06952-215">Portanto, eles coincidem com os requisitos declarados acima.</span><span class="sxs-lookup"><span data-stu-id="06952-215">Thus they coincide with the requirements stated above.</span></span>

<span data-ttu-id="06952-216">Em Q #, essas medidas retornam $j $ se a medida produz um resultado no eigenspace de sinal $ (-1) ^ j $ .</span><span class="sxs-lookup"><span data-stu-id="06952-216">In Q#, such measurements return $j$ if the measurement yields a result in the eigenspace of sign $(-1)^j$.</span></span>
<span data-ttu-id="06952-217">Ter medidas Pauli como um recurso interno em Q # é útil porque a medição desses operadores requer cadeias longas de Gates e transformações de base controladas para descrever a diagonal $U $ portão necessário para expressar a operação como um produto tensor de $Z $ e $ \id $ . Ao ser capaz de especificar que você deseja realizar uma dessas medidas predefinidas, você não precisa se preocupar em como transformar sua base de forma que uma medida de base computacional forneça as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="06952-217">Having Pauli measurements as a built-in feature in Q# is helpful because measuring such operators requires long chains of controlled-NOT gates and basis transformations to describe the diagonalizing $U$ gate needed to express the operation as a tensor product of $Z$ and $\id$. By being able to specify that you wish to do one of these pre-defined measurements, you don't need to worry about how to transform your basis such that a computational basis measurement provides the necessary information.</span></span>
<span data-ttu-id="06952-218">O Q # trata todas as transformações de base necessárias para você automaticamente.</span><span class="sxs-lookup"><span data-stu-id="06952-218">Q# handles all the necessary basis transformations for you automatically.</span></span>
<span data-ttu-id="06952-219">Para obter mais informações, consulte [`Measure`](xref:microsoft.quantum.intrinsic.measure) as [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) operações e.</span><span class="sxs-lookup"><span data-stu-id="06952-219">For more information, see the [`Measure`](xref:microsoft.quantum.intrinsic.measure) and [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) operations.</span></span>

## <a name="the-no-cloning-theorem"></a><span data-ttu-id="06952-220">O teorema no-Cloning</span><span class="sxs-lookup"><span data-stu-id="06952-220">The No-Cloning Theorem</span></span>

<span data-ttu-id="06952-221">As informações da Quantum são poderosas.</span><span class="sxs-lookup"><span data-stu-id="06952-221">Quantum information is powerful.</span></span>
<span data-ttu-id="06952-222">Ele nos permite fazer coisas incríveis, como números de fator exponencialmente mais rápidos do que os melhores algoritmos clássicos conhecidos, ou simular com eficiência sistemas de informações de alta correlação que exigem, de modo clássico, o custo exponencial para simular com precisão.</span><span class="sxs-lookup"><span data-stu-id="06952-222">It enables us to do amazing things such as factor numbers exponentially faster than the best known classical algorithms, or efficiently simulate correlated electron systems that classically require exponential cost to simulate accurately.</span></span>
<span data-ttu-id="06952-223">No entanto, há limitações no poder da computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="06952-223">However, there are limitations to the power of quantum computing.</span></span>
<span data-ttu-id="06952-224">Uma dessas limitações é fornecida pelo *teorema no-Cloning*.</span><span class="sxs-lookup"><span data-stu-id="06952-224">One such limitation is given by the *No-Cloning Theorem*.</span></span>

<span data-ttu-id="06952-225">O teorema no-Cloning é adequadamente nomeado.</span><span class="sxs-lookup"><span data-stu-id="06952-225">The No-Cloning Theorem is aptly named.</span></span>
<span data-ttu-id="06952-226">Ele não permite a clonagem de Estados de Quantum genérico por um computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="06952-226">It disallows cloning of generic quantum states by a quantum computer.</span></span>
<span data-ttu-id="06952-227">A prova do teorema é bastante simples.</span><span class="sxs-lookup"><span data-stu-id="06952-227">The proof of the theorem is remarkably straightforward.</span></span>
<span data-ttu-id="06952-228">Embora uma prova completa do teorema sem clonagem seja um pouco técnica para nossa discussão aqui, a prova no caso de nenhum qubits auxiliar adicional está dentro de nosso escopo (auxiliares qubits são qubits usados para espaço transitório durante uma computação e são facilmente usados e gerenciados em Q #, consulte [qubits emprestados](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span><span class="sxs-lookup"><span data-stu-id="06952-228">While a full proof of the no-cloning theorem is a little too technical for our discussion here, the proof in the case of no additional auxiliary qubits is within our scope (auxiliary qubits are qubits used for scratch space during a computation and are easily used and managed in Q#, see [borrowed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span></span>

<span data-ttu-id="06952-229">Para esse computador Quantum, a operação de clonagem deve ser descrita por uma matriz unitário.</span><span class="sxs-lookup"><span data-stu-id="06952-229">For such a quantum computer, the cloning operation must be described by a unitary matrix.</span></span>
<span data-ttu-id="06952-230">Não permitimos a medição, já que corromperia o estado Quantum que estamos tentando clonar.</span><span class="sxs-lookup"><span data-stu-id="06952-230">We disallow measurement, since it would corrupt the quantum state we are trying to clone.</span></span>
<span data-ttu-id="06952-231">Para simular a operação de clonagem, queremos que a matriz unitário usada tenha a propriedade que $ $ U \ket { \psi } \ket{0 } = \ket { \psi } \ket { \psi}</span><span class="sxs-lookup"><span data-stu-id="06952-231">To simulate the cloning operation, we want the unitary matrix used to have the property that $$ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}</span></span>
<span data-ttu-id="06952-232">$ $ para qualquer estado $ \ket { \psi } $.</span><span class="sxs-lookup"><span data-stu-id="06952-232">$$ for any state $\ket{\psi}$.</span></span>
<span data-ttu-id="06952-233">Em seguida, a propriedade linear da multiplicação de matriz implica que, para qualquer segundo estado Quantum $ \ket { \phi } $,</span><span class="sxs-lookup"><span data-stu-id="06952-233">The linearity property of matrix multiplication then implies that for any second quantum state $\ket{\phi}$,</span></span>

<span data-ttu-id="06952-234">US $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="06952-234">$$ \begin{align}</span></span>
    <span data-ttu-id="06952-235">U \left [\frac{1 } {\sqrt{2 } } \left (\ket { \phi } + \ket { \psi } \right) \right] \ket{0}</span><span class="sxs-lookup"><span data-stu-id="06952-235">U \left[ \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right] \ket{0}</span></span>
    <span data-ttu-id="06952-236">& = \frac{1 } {\sqrt{2 } } U \ket { \phi } \ket{0}</span><span class="sxs-lookup"><span data-stu-id="06952-236">& = \frac{1}{\sqrt{2}} U\ket{\phi}\ket{0}</span></span>
      <span data-ttu-id="06952-237">+ \frac{1 } {\sqrt{2 } } U \ket { \psi } \ket{0 } \\ \\ & = \frac{1 } {\sqrt{2 } } \left (\ket { \phi } \ket { \phi } + \ket { \psi } \ket { \psi}</span><span class="sxs-lookup"><span data-stu-id="06952-237">+ \frac{1}{\sqrt{2}} U\ket{\psi}\ket{0} \\\\ & = \frac{1}{\sqrt{2}} \left( \ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi}</span></span>
        <span data-ttu-id="06952-238">\right) \\ \\ & \ne \left (\frac{1 } {\sqrt{2 } } \left (\ket { \phi } + \ket { \psi } \right) \right) \otimes \left (\frac{1 } {\sqrt{2 } } \left (\ket { \phi } + \ket { \psi } \right) \right).</span><span class="sxs-lookup"><span data-stu-id="06952-238">\right) \\\\ & \ne \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right) \otimes \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right).</span></span>
<span data-ttu-id="06952-239">\end{align}</span><span class="sxs-lookup"><span data-stu-id="06952-239">\end{align}</span></span>
$$

<span data-ttu-id="06952-240">Isso fornece a intuição fundamental por trás do teorema sem clonagem: qualquer dispositivo que copia um estado de Quantum desconhecido deve induzir erros em pelo menos alguns dos Estados que ele copia.</span><span class="sxs-lookup"><span data-stu-id="06952-240">This provides the fundamental intuition behind the No-Cloning Theorem: any device that copies an unknown quantum state must induce errors on at least some of the states it copies.</span></span>
<span data-ttu-id="06952-241">Embora a principal suposição de que o Cloner atue linearmente no estado de entrada possa ser violada por meio da adição e da medição do qubits auxiliar, essas interações também vazam informações sobre o sistema por meio de estatísticas de medição e impedem a clonagem exata nesses casos.</span><span class="sxs-lookup"><span data-stu-id="06952-241">While the key assumption that the cloner acts linearly on the input state can be violated through the addition and measurement of auxiliary qubits, such interactions also leak information about the system through the measurement statistics and prevent exact cloning in such cases as well.</span></span>
<span data-ttu-id="06952-242">Para obter uma prova mais completa dos teorema sem clonagem, consulte [para obter mais informações](xref:microsoft.quantum.more-information).</span><span class="sxs-lookup"><span data-stu-id="06952-242">For a more complete proof of the No-Cloning Theorem see [For more information](xref:microsoft.quantum.more-information).</span></span>

<span data-ttu-id="06952-243">O teorema no-Cloning é importante para uma compreensão qualitativa da computação Quantum porque, se você puder clonar os Estados da Quantum de forma incara, terá uma capacidade quase mágico de aprender com os Estados da Quantum.</span><span class="sxs-lookup"><span data-stu-id="06952-243">The No-Cloning Theorem is important for qualitative understanding of quantum computing because if you could clone quantum states inexpensively then you would be granted a near-magical ability to learn from quantum states.</span></span>
<span data-ttu-id="06952-244">Na verdade, você poderia violar o princípio de incerteza de vaunted da Heisenberg.</span><span class="sxs-lookup"><span data-stu-id="06952-244">Indeed, you could violate Heisenberg's vaunted uncertainty principle.</span></span>
<span data-ttu-id="06952-245">Como alternativa, você pode usar um Cloner ideal para pegar um único exemplo de uma distribuição de Quantum complexa e aprender tudo o que poderia ser possível saber sobre essa distribuição de apenas uma amostra.</span><span class="sxs-lookup"><span data-stu-id="06952-245">Alternatively, you could use an optimal cloner to take a single sample from a complex quantum distribution and learn everything you could possibly learn about that distribution from just one sample.</span></span>
<span data-ttu-id="06952-246">Isso seria como você invertendo uma moeda e observando a cabeça e, depois, ao informar a um amigo sobre o resultado que eles respondem "Ah, a distribuição dessa moeda deve ser Bernoulli com $p = 0.512643 \ ldots $ !"</span><span class="sxs-lookup"><span data-stu-id="06952-246">This would be like you flipping a coin and observing heads and then upon telling a friend about the result having them respond "Ah the distribution of that coin must be Bernoulli with $p=0.512643\ldots$!"</span></span>  <span data-ttu-id="06952-247">Essa instrução seria não sensical porque um pouco de informação (o resultado dos cabeçotes) simplesmente não pode fornecer muitas informações necessárias para codificar a distribuição sem informações substanciais anteriores.</span><span class="sxs-lookup"><span data-stu-id="06952-247">Such a statement would be non-sensical because one bit of information (the heads outcome) simply cannot provide the many bits of information needed to encode the distribution without substantial prior information.</span></span>
<span data-ttu-id="06952-248">Da mesma forma, sem informações anteriores, não podemos clonar perfeitamente um estado Quantum da mesma forma que não podemos preparar uma Ensemble dessas moedas sem saber $p $ .</span><span class="sxs-lookup"><span data-stu-id="06952-248">Similarly, without prior information we cannot perfectly clone a quantum state just as we cannot prepare an ensemble of such coins without knowing $p$.</span></span>

<span data-ttu-id="06952-249">As informações não são gratuitas na computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="06952-249">Information is not free in quantum computing.</span></span>
<span data-ttu-id="06952-250">Cada qubit medido fornece uma única informação, e o teorema no-Cloning mostra que não há nenhum backdoor que possa ser explorado para contornar a compensação fundamental entre as informações obtidas sobre o sistema e o distúrbios invocado sobre ele.</span><span class="sxs-lookup"><span data-stu-id="06952-250">Each qubit measured gives a single bit of information, and the No-Cloning Theorem shows that there is no backdoor that can be exploited to get around the fundamental tradeoff between information gained about the system and the disturbance invoked upon it.</span></span>
