---
title: Oracles Quantum
description: Saiba como trabalhar com e definir os Oracle da Quantum, as operações de caixa preta que são usadas como entrada para outro algoritmo.
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
ms.topic: article
no-loc:
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
ms.openlocfilehash: 31e43940fc0607b15ccefcfae6be7122227b3d64
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630312"
---
# <a name="quantum-oracles"></a><span data-ttu-id="78b3b-103">Oracle Quantum</span><span class="sxs-lookup"><span data-stu-id="78b3b-103">Quantum Oracles</span></span>

<span data-ttu-id="78b3b-104">Um $O da Oracle $ é uma operação de "caixa preta" que é usada como entrada para outro algoritmo.</span><span class="sxs-lookup"><span data-stu-id="78b3b-104">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="78b3b-105">Muitas vezes, essas operações são definidas usando uma função clássica $f: \\ {0, 1 \\ } ^ n \tO \\ {0, 1 \\ } ^ m $ que usa uma $ entrada binária de $n bits e produz uma $ saída binária de $m bits.</span><span class="sxs-lookup"><span data-stu-id="78b3b-105">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="78b3b-106">Para fazer isso, considere uma entrada binária específica $x = (x_ {0 } , x_ {1 } , \dots, x_ {n-1 } ) $.</span><span class="sxs-lookup"><span data-stu-id="78b3b-106">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="78b3b-107">Podemos rotular Estados qubit como $ \ket { \vec{x } } = \ket{x_ {0 } } \otimes \ket{x_ {1 } } \otimes \cdots \otimes \ket{x_ {n-1 } } $.</span><span class="sxs-lookup"><span data-stu-id="78b3b-107">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="78b3b-108">Primeiro, podemos tentar definir $O $ para que $O \ket {x } = \ket{f (x)} $, mas isso tem alguns problemas.</span><span class="sxs-lookup"><span data-stu-id="78b3b-108">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="78b3b-109">Primeiro, $f $ pode ter um tamanho diferente de entrada e saída ($n \ne m $ ), de modo que a aplicação de $O $ alteraria o número de qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="78b3b-109">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="78b3b-110">Em segundo lugar, mesmo se $n = m $ , a função pode não ser invertível: se $f (x) = f (y) $ para alguns $x \ne y $ , $O \ket {x } = o \ket {y } $, mas $O ^ \dagger o \ket {x } \ne o ^ \dagger o \ket {y } $.</span><span class="sxs-lookup"><span data-stu-id="78b3b-110">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="78b3b-111">Isso significa que não será possível construir a operação de adjoin $O ^ \dagger $ e os Oracle precisam ter um adjacente definido para eles.</span><span class="sxs-lookup"><span data-stu-id="78b3b-111">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="78b3b-112">Definindo um Oracle por seu efeito nos Estados de base computacional</span><span class="sxs-lookup"><span data-stu-id="78b3b-112">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="78b3b-113">Podemos lidar com esses dois problemas introduzindo um segundo registro de $m $ qubits para manter nossa resposta.</span><span class="sxs-lookup"><span data-stu-id="78b3b-113">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="78b3b-114">Em seguida, vamos definir o efeito do Oracle em todos os Estados de base computacional: para todos os $x na \\ {0, 1 \\ } ^ n $ e $y na \\ {0, 1 \\ } ^ m $ ,</span><span class="sxs-lookup"><span data-stu-id="78b3b-114">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

<span data-ttu-id="78b3b-115">US $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-115">$$ \begin{align}</span></span>
    <span data-ttu-id="78b3b-116">O (\ket{x } \otimes \ket{y } ) = \ket{x } \otimes \ket{y \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="78b3b-116">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="78b3b-117">\end{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-117">\end{align}</span></span>
$$

<span data-ttu-id="78b3b-118">Agora $O = O ^ \dagger $ por construção, portanto, resolvemos os dois problemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="78b3b-118">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
> <span data-ttu-id="78b3b-119">Para ver que $O = O ^ {\dagger } $, observe que $O ^ 2 = \boldone $ desde $a \oplus b \oplus b = a $ para todos os $a, b na \{ 0, 1 \} $.</span><span class="sxs-lookup"><span data-stu-id="78b3b-119">To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
> <span data-ttu-id="78b3b-120">Como resultado, $O \ket{x } \ket{y \oplus f (x)} = \ket{x } \ket{y \oplus f (x) \oplus f (x)} = \ket{x } \ket{y } $.</span><span class="sxs-lookup"><span data-stu-id="78b3b-120">As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="78b3b-121">De forma importante, definir um Oracle dessa maneira para cada Estado de base computacional $ \ket{x } \ket{y } $ também define como $O $ atua para qualquer outro Estado.</span><span class="sxs-lookup"><span data-stu-id="78b3b-121">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="78b3b-122">Isso é seguido imediatamente do fato de que $O $ , como todas as operações de Quantum, é linear no estado em que atua.</span><span class="sxs-lookup"><span data-stu-id="78b3b-122">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="78b3b-123">Considere a operação Hadamard, por exemplo, que é definida por $H \ket{0 } = \ket { +} $ e $H \ket{1 } = \ket { -} $.</span><span class="sxs-lookup"><span data-stu-id="78b3b-123">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="78b3b-124">Se quisermos saber como $H $ atua em $ \ket { +} $, podemos usar essa $H $ é linear,</span><span class="sxs-lookup"><span data-stu-id="78b3b-124">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

<span data-ttu-id="78b3b-125">US $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-125">$$ \begin{align}</span></span>
<span data-ttu-id="78b3b-126">H \ket { +} & = \frac{1 } {\sqrt{2 } } H (\ket{0 } + \ket{1 } ) = \frac{1 } {\sqrt{2 } } (H \ket {0 } + h \ket {1 } ) \\ \\ & = \frac{1 } {\sqrt{2 } } (\ket { +} + \ket { -}) = \frac12 (\ket{0 } + \ket{1 } + \ket{0 } -\ket{1 } ) = \ket{0 } .</span><span class="sxs-lookup"><span data-stu-id="78b3b-126">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
<span data-ttu-id="78b3b-127">\end{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-127">\end{align}</span></span>
$$

<span data-ttu-id="78b3b-128">No caso da definição de nosso $O Oracle $ , podemos usar de forma semelhante que qualquer estado $ \ket { \psi } $ em $n + m $ qubits pode ser escrito como</span><span class="sxs-lookup"><span data-stu-id="78b3b-128">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

<span data-ttu-id="78b3b-129">US $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-129">$$ \begin{align}</span></span>
<span data-ttu-id="78b3b-130">\ket { \psi } & = \ sum_ {x na \\ {0, 1 \\ } ^ n, y na \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y}</span><span class="sxs-lookup"><span data-stu-id="78b3b-130">\ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
<span data-ttu-id="78b3b-131">\end{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-131">\end{align}</span></span>
$$

<span data-ttu-id="78b3b-132">em que $ \alpha: \\ {0, 1 \\ } ^ n \times \\ {0, 1 \\ } ^ m \tO \mathbb{C } $ representa os coeficientes do estado $ \ket { \psi } $.</span><span class="sxs-lookup"><span data-stu-id="78b3b-132">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="78b3b-133">Assim,</span><span class="sxs-lookup"><span data-stu-id="78b3b-133">Thus,</span></span>

<span data-ttu-id="78b3b-134">US $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-134">$$ \begin{align}</span></span>
<span data-ttu-id="78b3b-135">O \ket { \psi } & = O \ sum_ {x na \\ {0, 1 \\ } ^ n, y na \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y } \\ \\ & = \ sum_ {x na \\ {0, 1 \\ } ^ n, y na \\ {0, 1 \\ } ^ m } \alpha (x, y) O \ket{x } \ket{y } \\ \\ & = \ sum_ {x na \\ {0, 1 \\ } ^ n, y na \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x \ket{y } \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="78b3b-135">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="78b3b-136">\end{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-136">\end{align}</span></span>
$$

## <a name="phase-oracles"></a><span data-ttu-id="78b3b-137">Fase Oracle</span><span class="sxs-lookup"><span data-stu-id="78b3b-137">Phase oracles</span></span>
<span data-ttu-id="78b3b-138">Como alternativa, podemos codificar $f $ em um $O Oracle $ aplicando uma _fase_ com base na entrada para $O $ .</span><span class="sxs-lookup"><span data-stu-id="78b3b-138">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$.</span></span>
<span data-ttu-id="78b3b-139">Por exemplo, podemos definir $O de $ modo que $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-139">For instance, we might define $O$ such that $$ \begin{align}</span></span>
    <span data-ttu-id="78b3b-140">O \ket{x } = (-1) ^ {f (x)} \ket{x } .</span><span class="sxs-lookup"><span data-stu-id="78b3b-140">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
<span data-ttu-id="78b3b-141">\end{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-141">\end{align}</span></span>
<span data-ttu-id="78b3b-142">$ $ Se uma fase Oracle age em um registro inicialmente em um estado de base computacional $ \ket{x } $, essa fase é uma fase global e, portanto, não observável.</span><span class="sxs-lookup"><span data-stu-id="78b3b-142">$$ If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="78b3b-143">Mas tal Oracle pode ser um recurso muito potente se aplicado a uma superposição ou como uma operação controlada.</span><span class="sxs-lookup"><span data-stu-id="78b3b-143">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="78b3b-144">Por exemplo, considere uma fase orcale $O _f $ para uma função de qubit única $f $ .</span><span class="sxs-lookup"><span data-stu-id="78b3b-144">For example, consider a phase orcale $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="78b3b-145">Em seguida, $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-145">Then, $$ \begin{align}</span></span>
    <span data-ttu-id="78b3b-146">O_f \ket { +} & = O_f (\ket{0 } + \ket{1 } )/\sqrt{2 } \\ \\ & = ((-1) ^ {f (0)} \ket{0 } + (-1) ^ {f (1)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} (\ket{0 } + (-1) ^ {f (1)-f (0)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \ket { +}.</span><span class="sxs-lookup"><span data-stu-id="78b3b-146">O_f \ket{+} & = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\ & = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
<span data-ttu-id="78b3b-147">\end{align}</span><span class="sxs-lookup"><span data-stu-id="78b3b-147">\end{align}</span></span>
$$

<span data-ttu-id="78b3b-148">Em geral, as duas exibições de Oracle podem ser ampliadas para representar funções clássicas que retornam números reais em vez de apenas um único bit.</span><span class="sxs-lookup"><span data-stu-id="78b3b-148">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="78b3b-149">Escolher a melhor maneira de implementar um Oracle depende muito da forma como esse Oracle será usado dentro de um determinado algoritmo.</span><span class="sxs-lookup"><span data-stu-id="78b3b-149">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="78b3b-150">Por exemplo, o [algoritmo Deutsch-Jozsa](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) depende do Oracle implementado na primeira forma, enquanto o [algoritmo de Grover](https://en.wikipedia.org/wiki/Grover's_algorithm) se baseia no Oracle implementado da segunda maneira.</span><span class="sxs-lookup"><span data-stu-id="78b3b-150">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="78b3b-151">Para obter mais detalhes, sugerimos a discussão em [Gilyén *et al*. 1711, 465](https://arxiv.org/abs/1711.00465).</span><span class="sxs-lookup"><span data-stu-id="78b3b-151">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
