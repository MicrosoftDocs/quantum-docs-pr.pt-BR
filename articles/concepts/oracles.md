---
<span data-ttu-id="5bc8f-101">Título: Descrição da Quantum Oracle: saiba como trabalhar com e definir Oracle Quantum, operações de caixa preta que são usadas como entrada para outro algoritmo.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-101">title: Quantum oracles description: Learn how to work with and define quantum oracles, black box operations that are used as input to another algorithm.</span></span>
<span data-ttu-id="5bc8f-102">Autor: cgranade UID: Microsoft. Quantum. Concepts. oraclees MS. Author: Christopher.Granade@microsoft.com MS. Data: 07/11/2018 MS. Topic: artigo no-loc:</span><span class="sxs-lookup"><span data-stu-id="5bc8f-102">author: cgranade uid: microsoft.quantum.concepts.oracles ms.author: Christopher.Granade@microsoft.com ms.date: 07/11/2018 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="5bc8f-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-103">"Q#"</span></span>
- <span data-ttu-id="5bc8f-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-104">"$$v"</span></span>
- <span data-ttu-id="5bc8f-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-105">"$$"</span></span>
- <span data-ttu-id="5bc8f-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-106">"$$"</span></span>
- <span data-ttu-id="5bc8f-107">"$"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-107">"$"</span></span>
- <span data-ttu-id="5bc8f-108">"$"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-108">"$"</span></span>
- <span data-ttu-id="5bc8f-109">"$"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-109">"$"</span></span>
- <span data-ttu-id="5bc8f-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-110">"$$"</span></span>
- <span data-ttu-id="5bc8f-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-111">"\cdots"</span></span>
- <span data-ttu-id="5bc8f-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-112">"bmatrix"</span></span>
- <span data-ttu-id="5bc8f-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-113">"\ddots"</span></span>
- <span data-ttu-id="5bc8f-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-114">"\equiv"</span></span>
- <span data-ttu-id="5bc8f-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-115">"\sum"</span></span>
- <span data-ttu-id="5bc8f-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-116">"\begin"</span></span>
- <span data-ttu-id="5bc8f-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-117">"\end"</span></span>
- <span data-ttu-id="5bc8f-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-118">"\sqrt"</span></span>
- <span data-ttu-id="5bc8f-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-119">"\otimes"</span></span>
- <span data-ttu-id="5bc8f-120">"{"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-120">"{"</span></span>
- <span data-ttu-id="5bc8f-121">"}"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-121">"}"</span></span>
- <span data-ttu-id="5bc8f-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-122">"\text"</span></span>
- <span data-ttu-id="5bc8f-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-123">"\phi"</span></span>
- <span data-ttu-id="5bc8f-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-124">"\kappa"</span></span>
- <span data-ttu-id="5bc8f-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-125">"\psi"</span></span>
- <span data-ttu-id="5bc8f-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-126">"\alpha"</span></span>
- <span data-ttu-id="5bc8f-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-127">"\beta"</span></span>
- <span data-ttu-id="5bc8f-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-128">"\gamma"</span></span>
- <span data-ttu-id="5bc8f-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-129">"\delta"</span></span>
- <span data-ttu-id="5bc8f-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-130">"\omega"</span></span>
- <span data-ttu-id="5bc8f-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-131">"\bra"</span></span>
- <span data-ttu-id="5bc8f-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-132">"\ket"</span></span>
- <span data-ttu-id="5bc8f-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-133">"\boldone"</span></span>
- <span data-ttu-id="5bc8f-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-134">"\\\\"</span></span>
- <span data-ttu-id="5bc8f-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-135">"\\"</span></span>
- <span data-ttu-id="5bc8f-136">"="</span><span class="sxs-lookup"><span data-stu-id="5bc8f-136">"="</span></span>
- <span data-ttu-id="5bc8f-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-137">"\frac"</span></span>
- <span data-ttu-id="5bc8f-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-138">"\text"</span></span>
- <span data-ttu-id="5bc8f-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-139">"\mapsto"</span></span>
- <span data-ttu-id="5bc8f-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-140">"\dagger"</span></span>
- <span data-ttu-id="5bc8f-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-141">"\to"</span></span>
- <span data-ttu-id="5bc8f-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-142">"\begin{cases}"</span></span>
- <span data-ttu-id="5bc8f-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-143">"\end{cases}"</span></span>
- <span data-ttu-id="5bc8f-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-144">"\operatorname"</span></span>
- <span data-ttu-id="5bc8f-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-145">"\braket"</span></span>
- <span data-ttu-id="5bc8f-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-146">"\id"</span></span>
- <span data-ttu-id="5bc8f-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-147">"\expect"</span></span>
- <span data-ttu-id="5bc8f-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-148">"\defeq"</span></span>
- <span data-ttu-id="5bc8f-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-149">"\variance"</span></span>
- <span data-ttu-id="5bc8f-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-150">"\dd"</span></span>
- <span data-ttu-id="5bc8f-151">"&"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-151">"&"</span></span>
- <span data-ttu-id="5bc8f-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-152">"\begin{align}"</span></span>
- <span data-ttu-id="5bc8f-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-153">"\end{align}"</span></span>
- <span data-ttu-id="5bc8f-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-154">"\Lambda"</span></span>
- <span data-ttu-id="5bc8f-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-155">"\lambda"</span></span>
- <span data-ttu-id="5bc8f-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-156">"\Omega"</span></span>
- <span data-ttu-id="5bc8f-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-157">"\mathrm"</span></span>
- <span data-ttu-id="5bc8f-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-158">"\left"</span></span>
- <span data-ttu-id="5bc8f-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-159">"\right"</span></span>
- <span data-ttu-id="5bc8f-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-160">"\qquad"</span></span>
- <span data-ttu-id="5bc8f-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-161">"\times"</span></span>
- <span data-ttu-id="5bc8f-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-162">"\big"</span></span>
- <span data-ttu-id="5bc8f-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-163">"\langle"</span></span>
- <span data-ttu-id="5bc8f-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-164">"\rangle"</span></span>
- <span data-ttu-id="5bc8f-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-165">"\bigg"</span></span>
- <span data-ttu-id="5bc8f-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-166">"\Big"</span></span>
- <span data-ttu-id="5bc8f-167">"|"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-167">"|"</span></span>
- <span data-ttu-id="5bc8f-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-168">"\mathbb"</span></span>
- <span data-ttu-id="5bc8f-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-169">"\vec"</span></span>
- <span data-ttu-id="5bc8f-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-170">"\in"</span></span>
- <span data-ttu-id="5bc8f-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-171">"\texttt"</span></span>
- <span data-ttu-id="5bc8f-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-172">"\ne"</span></span>
- <span data-ttu-id="5bc8f-173">"<"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-173">"<"</span></span>
- <span data-ttu-id="5bc8f-174">">"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-174">">"</span></span>
- <span data-ttu-id="5bc8f-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-175">"\leq"</span></span>
- <span data-ttu-id="5bc8f-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-176">"\geq"</span></span>
- <span data-ttu-id="5bc8f-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-177">"~~"</span></span>
- <span data-ttu-id="5bc8f-178">"~"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-178">"~"</span></span>
- <span data-ttu-id="5bc8f-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="5bc8f-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="5bc8f-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="5bc8f-181">"\_"</span></span>

---
# <a name="quantum-oracles"></a><span data-ttu-id="5bc8f-182">Oracle Quantum</span><span class="sxs-lookup"><span data-stu-id="5bc8f-182">Quantum Oracles</span></span>

<span data-ttu-id="5bc8f-183">Um Oracle $ O $ é uma operação de "caixa preta" que é usada como entrada para outro algoritmo.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-183">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="5bc8f-184">Muitas vezes, essas operações são definidas usando uma função clássica $ f: \\ { 0, 1 \\ } ^ n \to \\ { 0, 1 \\ } ^ m $ que usa $ uma $ entrada binária de n bits e produz $ uma $ saída binária de bit m.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-184">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="5bc8f-185">Para fazer isso, considere uma entrada binária específica $ x = (x_ { 0 } , x_ { 1 } , \dots, x_ { n-1 } ) $ .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-185">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="5bc8f-186">Podemos rotular Estados qubit como $ \ket { \vec { x } } = \ket { x_ { 0 } } \otimes \ket { x_ { 1 } } \otimes \cdots \otimes \ket { x_ { n-1 } } $ .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-186">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="5bc8f-187">Nós podemos primeiro tentar definir $ o $ para que $ o \ket { x } = \ket { f (x) } $ , mas isso tenha alguns problemas.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-187">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="5bc8f-188">Em primeiro lugar, $ f $ pode ter um tamanho diferente de entrada e saída ( $ n \ne m $ ), de modo que aplicar $ $ o seria alterar o número de qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-188">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="5bc8f-189">Em segundo lugar, mesmo se $ n = m $ , a função pode não ser invertível: se $ f (x) = f (y) $ para alguns $ x \ne y $ , em seguida, $ o \ket { x } = o \ket { y, } $ mas $ o ^ \dagger o \ket { x } \ne o ^ \dagger o \ket { y } $ .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-189">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="5bc8f-190">Isso significa que não será possível construir a operação de addefinição o $ ^ \dagger $ e os Oracle precisarão ter um adjacente definido para eles.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-190">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="5bc8f-191">Definindo um Oracle por seu efeito nos Estados de base computacional</span><span class="sxs-lookup"><span data-stu-id="5bc8f-191">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="5bc8f-192">Podemos lidar com esses dois problemas introduzindo um segundo registro de $ m $ qubits para manter nossa resposta.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-192">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="5bc8f-193">Em seguida, vamos definir o efeito do Oracle em todos os Estados de base computacional: para todos os $ x \in \\ { 0, 1 \\ } ^ n $ e $ y \in \\ { 0, 1 \\ } ^ m $ ,</span><span class="sxs-lookup"><span data-stu-id="5bc8f-193">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

$$
\begin{align}
    <span data-ttu-id="5bc8f-194">O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \oplus f (x) } .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-194">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

<span data-ttu-id="5bc8f-195">Agora $ o = ^ \dagger $ por construção, portanto, resolvemos os dois problemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-195">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
<span data-ttu-id="5bc8f-196">>Para ver que $ o o = ^ { \dagger } $ , observe que o $ ^ 2, = \boldone $ desde $ um \oplus b \oplus b = a $ para todos os $ , b \in \: :: no-Loc ({)::: 0, 1 \: :: no-Loc (})::: $ .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-196">> To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
<span data-ttu-id="5bc8f-197">>Como resultado, $ O \ket { x } \ket { y \oplus f (x) } = \ket { x } \ket { y \oplus f (x) \oplus f (x) } = \ket { x } \ket { y } $ .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-197">> As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="5bc8f-198">De forma importante, definir um Oracle dessa maneira para cada Estado de base computacional $ \ket { x } \ket { y } $ também define como $ O O $ age para qualquer outro Estado.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-198">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="5bc8f-199">Isso é seguido imediatamente do fato de que $ O $ , como todas as operações de Quantum, é linear no estado em que ele atua.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-199">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="5bc8f-200">Considere a operação Hadamard, por exemplo, que é definida por $ h \ket { 0 } = \ket { + } $ e $ h \ket { 1 } = \ket { - } $ .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-200">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="5bc8f-201">Se quisermos saber como $ h $ atua $ \ket { + } $ , podemos usar que $ h $ seja linear,</span><span class="sxs-lookup"><span data-stu-id="5bc8f-201">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

$$
\begin{align}
<span data-ttu-id="5bc8f-202">H \ket { + } & = \frac { 1 } { \sqrt { 2 } } h ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + h \ket { 1 } )\\\\</span><span class="sxs-lookup"><span data-stu-id="5bc8f-202">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\</span></span>
           <span data-ttu-id="5bc8f-203">&= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-203">& = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
\end{align}
$$

<span data-ttu-id="5bc8f-204">No caso de definir nosso Oracle $ O $ , podemos usar de forma semelhante que qualquer estado $ \ket { \psi } $ em $ n + m $ qubits pode ser escrito como</span><span class="sxs-lookup"><span data-stu-id="5bc8f-204">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

$$
\begin{align}
<span data-ttu-id="5bc8f-205">\ket{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}</span><span class="sxs-lookup"><span data-stu-id="5bc8f-205">\ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
\end{align}
$$

<span data-ttu-id="5bc8f-206">em que $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C } $ representa os coeficientes do estado $ \ket { \psi } $ .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-206">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="5bc8f-207">Assim,</span><span class="sxs-lookup"><span data-stu-id="5bc8f-207">Thus,</span></span>

$$
\begin{align}
<span data-ttu-id="5bc8f-208">O \ket { \psi } & = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) O \sum _ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\</span><span class="sxs-lookup"><span data-stu-id="5bc8f-208">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\</span></span>
             <span data-ttu-id="5bc8f-209">&= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \oplus f (x) } .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-209">& = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

## <a name="phase-oracles"></a><span data-ttu-id="5bc8f-210">Fase Oracle</span><span class="sxs-lookup"><span data-stu-id="5bc8f-210">Phase oracles</span></span>
<span data-ttu-id="5bc8f-211">Como alternativa, podemos codificar $ f $ em um Oracle $ O $ aplicando uma _fase_ com base na entrada para $ o $ . Por exemplo, poderemos definir $ O $ como$$</span><span class="sxs-lookup"><span data-stu-id="5bc8f-211">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$. For instance, we might define $O$ such that $$</span></span>
\begin{align}
    <span data-ttu-id="5bc8f-212">O \ket { x } = (-1) ^ { f (x) } \ket { x } .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-212">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
\end{align}
$$
<span data-ttu-id="5bc8f-213">Se uma fase da Oracle age em um registro inicialmente em um estado de base computacional $ \ket { x } $ , essa fase é uma fase global e, portanto, não observável.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-213">If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="5bc8f-214">Mas tal Oracle pode ser um recurso muito potente se aplicado a uma superposição ou como uma operação controlada.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-214">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="5bc8f-215">Por exemplo, considere uma fase de $ O_f $ da Oracle para uma função f de qubit única $ $ .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-215">For example, consider a phase oracle $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="5bc8f-216">Clique$$</span><span class="sxs-lookup"><span data-stu-id="5bc8f-216">Then, $$</span></span>
\begin{align}
    <span data-ttu-id="5bc8f-217">O_f\ket{+}</span><span class="sxs-lookup"><span data-stu-id="5bc8f-217">O_f \ket{+}</span></span>
        <span data-ttu-id="5bc8f-218">&=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="5bc8f-218">& = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="5bc8f-219">&=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="5bc8f-219">& = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="5bc8f-220">&=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="5bc8f-220">& = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="5bc8f-221">&=(-1) ^ { f (0) } Z ^ { f (0)-f (1) } \ket { + } .</span><span class="sxs-lookup"><span data-stu-id="5bc8f-221">& = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
\end{align}
$$

<span data-ttu-id="5bc8f-222">Em geral, as duas exibições de Oracle podem ser ampliadas para representar funções clássicas que retornam números reais em vez de apenas um único bit.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-222">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="5bc8f-223">Escolher a melhor maneira de implementar um Oracle depende muito da forma como esse Oracle será usado dentro de um determinado algoritmo.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-223">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="5bc8f-224">Por exemplo, o [algoritmo Deutsch-Jozsa](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) depende do Oracle implementado na primeira forma, enquanto o [algoritmo de Grover](https://en.wikipedia.org/wiki/Grover's_algorithm) se baseia no Oracle implementado da segunda maneira.</span><span class="sxs-lookup"><span data-stu-id="5bc8f-224">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="5bc8f-225">Para obter mais detalhes, sugerimos a discussão em [Gilyén *et al*. 1711, 465](https://arxiv.org/abs/1711.00465).</span><span class="sxs-lookup"><span data-stu-id="5bc8f-225">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
