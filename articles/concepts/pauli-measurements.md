---
<span data-ttu-id="f3111-101">Título: Descrição de medidas de Pauli: saiba como trabalhar com operações de medição de Pauli única e qubit.</span><span class="sxs-lookup"><span data-stu-id="f3111-101">title: Pauli Measurements description: Learn how to work with single- and multi-qubit Pauli measurement operations.</span></span>
<span data-ttu-id="f3111-102">Autor: QuantumWriter UID: Microsoft. Quantum. Concepts. Pauli MS. Author: nawiebe@microsoft.com MS. Date: 12/11/2017 MS. tópico: article no-loc:</span><span class="sxs-lookup"><span data-stu-id="f3111-102">author: QuantumWriter uid: microsoft.quantum.concepts.pauli ms.author: nawiebe@microsoft.com ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="f3111-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="f3111-103">"Q#"</span></span>
- <span data-ttu-id="f3111-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="f3111-104">"$$v"</span></span>
- <span data-ttu-id="f3111-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="f3111-105">"$$"</span></span>
- <span data-ttu-id="f3111-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="f3111-106">"$$"</span></span>
- <span data-ttu-id="f3111-107">"$"</span><span class="sxs-lookup"><span data-stu-id="f3111-107">"$"</span></span>
- <span data-ttu-id="f3111-108">"$"</span><span class="sxs-lookup"><span data-stu-id="f3111-108">"$"</span></span>
- <span data-ttu-id="f3111-109">"$"</span><span class="sxs-lookup"><span data-stu-id="f3111-109">"$"</span></span>
- <span data-ttu-id="f3111-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="f3111-110">"$$"</span></span>
- <span data-ttu-id="f3111-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="f3111-111">"\cdots"</span></span>
- <span data-ttu-id="f3111-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="f3111-112">"bmatrix"</span></span>
- <span data-ttu-id="f3111-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="f3111-113">"\ddots"</span></span>
- <span data-ttu-id="f3111-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="f3111-114">"\equiv"</span></span>
- <span data-ttu-id="f3111-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="f3111-115">"\sum"</span></span>
- <span data-ttu-id="f3111-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="f3111-116">"\begin"</span></span>
- <span data-ttu-id="f3111-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="f3111-117">"\end"</span></span>
- <span data-ttu-id="f3111-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="f3111-118">"\sqrt"</span></span>
- <span data-ttu-id="f3111-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="f3111-119">"\otimes"</span></span>
- <span data-ttu-id="f3111-120">"{"</span><span class="sxs-lookup"><span data-stu-id="f3111-120">"{"</span></span>
- <span data-ttu-id="f3111-121">"}"</span><span class="sxs-lookup"><span data-stu-id="f3111-121">"}"</span></span>
- <span data-ttu-id="f3111-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="f3111-122">"\text"</span></span>
- <span data-ttu-id="f3111-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="f3111-123">"\phi"</span></span>
- <span data-ttu-id="f3111-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="f3111-124">"\kappa"</span></span>
- <span data-ttu-id="f3111-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="f3111-125">"\psi"</span></span>
- <span data-ttu-id="f3111-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="f3111-126">"\alpha"</span></span>
- <span data-ttu-id="f3111-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="f3111-127">"\beta"</span></span>
- <span data-ttu-id="f3111-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="f3111-128">"\gamma"</span></span>
- <span data-ttu-id="f3111-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="f3111-129">"\delta"</span></span>
- <span data-ttu-id="f3111-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="f3111-130">"\omega"</span></span>
- <span data-ttu-id="f3111-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="f3111-131">"\bra"</span></span>
- <span data-ttu-id="f3111-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="f3111-132">"\ket"</span></span>
- <span data-ttu-id="f3111-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="f3111-133">"\boldone"</span></span>
- <span data-ttu-id="f3111-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="f3111-134">"\\\\"</span></span>
- <span data-ttu-id="f3111-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="f3111-135">"\\"</span></span>
- <span data-ttu-id="f3111-136">"="</span><span class="sxs-lookup"><span data-stu-id="f3111-136">"="</span></span>
- <span data-ttu-id="f3111-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="f3111-137">"\frac"</span></span>
- <span data-ttu-id="f3111-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="f3111-138">"\text"</span></span>
- <span data-ttu-id="f3111-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="f3111-139">"\mapsto"</span></span>
- <span data-ttu-id="f3111-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="f3111-140">"\dagger"</span></span>
- <span data-ttu-id="f3111-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="f3111-141">"\to"</span></span>
- <span data-ttu-id="f3111-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="f3111-142">"\begin{cases}"</span></span>
- <span data-ttu-id="f3111-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="f3111-143">"\end{cases}"</span></span>
- <span data-ttu-id="f3111-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="f3111-144">"\operatorname"</span></span>
- <span data-ttu-id="f3111-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="f3111-145">"\braket"</span></span>
- <span data-ttu-id="f3111-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="f3111-146">"\id"</span></span>
- <span data-ttu-id="f3111-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="f3111-147">"\expect"</span></span>
- <span data-ttu-id="f3111-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="f3111-148">"\defeq"</span></span>
- <span data-ttu-id="f3111-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="f3111-149">"\variance"</span></span>
- <span data-ttu-id="f3111-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="f3111-150">"\dd"</span></span>
- <span data-ttu-id="f3111-151">"&"</span><span class="sxs-lookup"><span data-stu-id="f3111-151">"&"</span></span>
- <span data-ttu-id="f3111-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="f3111-152">"\begin{align}"</span></span>
- <span data-ttu-id="f3111-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="f3111-153">"\end{align}"</span></span>
- <span data-ttu-id="f3111-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="f3111-154">"\Lambda"</span></span>
- <span data-ttu-id="f3111-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="f3111-155">"\lambda"</span></span>
- <span data-ttu-id="f3111-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="f3111-156">"\Omega"</span></span>
- <span data-ttu-id="f3111-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="f3111-157">"\mathrm"</span></span>
- <span data-ttu-id="f3111-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="f3111-158">"\left"</span></span>
- <span data-ttu-id="f3111-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="f3111-159">"\right"</span></span>
- <span data-ttu-id="f3111-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="f3111-160">"\qquad"</span></span>
- <span data-ttu-id="f3111-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="f3111-161">"\times"</span></span>
- <span data-ttu-id="f3111-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="f3111-162">"\big"</span></span>
- <span data-ttu-id="f3111-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="f3111-163">"\langle"</span></span>
- <span data-ttu-id="f3111-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="f3111-164">"\rangle"</span></span>
- <span data-ttu-id="f3111-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="f3111-165">"\bigg"</span></span>
- <span data-ttu-id="f3111-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="f3111-166">"\Big"</span></span>
- <span data-ttu-id="f3111-167">"|"</span><span class="sxs-lookup"><span data-stu-id="f3111-167">"|"</span></span>
- <span data-ttu-id="f3111-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="f3111-168">"\mathbb"</span></span>
- <span data-ttu-id="f3111-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="f3111-169">"\vec"</span></span>
- <span data-ttu-id="f3111-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="f3111-170">"\in"</span></span>
- <span data-ttu-id="f3111-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="f3111-171">"\texttt"</span></span>
- <span data-ttu-id="f3111-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="f3111-172">"\ne"</span></span>
- <span data-ttu-id="f3111-173">"<"</span><span class="sxs-lookup"><span data-stu-id="f3111-173">"<"</span></span>
- <span data-ttu-id="f3111-174">">"</span><span class="sxs-lookup"><span data-stu-id="f3111-174">">"</span></span>
- <span data-ttu-id="f3111-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="f3111-175">"\leq"</span></span>
- <span data-ttu-id="f3111-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="f3111-176">"\geq"</span></span>
- <span data-ttu-id="f3111-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="f3111-177">"~~"</span></span>
- <span data-ttu-id="f3111-178">"~"</span><span class="sxs-lookup"><span data-stu-id="f3111-178">"~"</span></span>
- <span data-ttu-id="f3111-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="f3111-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="f3111-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="f3111-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="f3111-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="f3111-181">"\_"</span></span>

---

# <a name="pauli-measurements"></a><span data-ttu-id="f3111-182">Medições de Pauli</span><span class="sxs-lookup"><span data-stu-id="f3111-182">Pauli Measurements</span></span>

<span data-ttu-id="f3111-183">Nas discussões anteriores, concentramos-se em medidas de base computacional.</span><span class="sxs-lookup"><span data-stu-id="f3111-183">In the previous discussions, we have focused on computational basis measurements.</span></span>
<span data-ttu-id="f3111-184">Na verdade, há outras medidas comuns que ocorrem na computação Quantum que, de uma perspectiva de notação, são convenientes para expressar em termos de medidas de base computacional.</span><span class="sxs-lookup"><span data-stu-id="f3111-184">In fact, there are other common measurements that occur in quantum computing that, from a notational perspective, are convenient to express in terms of computational basis measurements.</span></span>
<span data-ttu-id="f3111-185">À medida que você trabalha com Q# o, o tipo mais comum de medidas que você encontrará provavelmente serão as *medidas Paulis*, que generalizam as medidas de base computacional para incluir medidas em outras bases e de paridade entre diferentes qubits.</span><span class="sxs-lookup"><span data-stu-id="f3111-185">As you work with Q#, the most common kind of measurements that you'll run into will likely be *Pauli measurements*, which generalize computational basis measurements to include measurements in other bases, and of parity between different qubits.</span></span>
<span data-ttu-id="f3111-186">Nesses casos, é comum discutir a medição de um operador Pauli, em geral, um operador como $ X, Y, z $ ou $ z \otimes z, x \otimes x, x \otimes Y $ e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f3111-186">In such cases, it is common to discuss measuring a Pauli operator, in general an operator such as $X,Y,Z$ or $Z\otimes Z, X\otimes X, X\otimes Y$, and so forth.</span></span>

> [!TIP]
<span data-ttu-id="f3111-187">> No Q# , os operadores qubit Pauli geralmente são representados por matrizes do tipo `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="f3111-187">> In Q#, multi-qubit Pauli operators are generally represented by arrays of type `Pauli[]`.</span></span>
<span data-ttu-id="f3111-188">> Por exemplo, para representar $ X \otimes Z \otimes Y $ , você pode usar a matriz `[PauliX, PauliZ, PauliY]` .</span><span class="sxs-lookup"><span data-stu-id="f3111-188">> For example, to represent $X \otimes Z \otimes Y$, you can use the array `[PauliX, PauliZ, PauliY]`.</span></span>

<span data-ttu-id="f3111-189">Discutir a medição em termos de operadores Pauli é especialmente comum no subcampo de correção de erro Quantum.</span><span class="sxs-lookup"><span data-stu-id="f3111-189">Discussing measurement in terms of Pauli operators is especially common in the subfield of quantum error correction.</span></span>
<span data-ttu-id="f3111-190">No Q# , seguimos uma convenção semelhante; agora, explicamos essa exibição alternativa de medidas.</span><span class="sxs-lookup"><span data-stu-id="f3111-190">In Q#, we follow a similar convention; we now explain this alternative view of measurements.</span></span>

<span data-ttu-id="f3111-191">Antes de se aprofundar nos detalhes de como pensar em uma medida Pauli, é útil pensar em que a medição de um único qubit dentro de um computador Quantum faz o estado Quantum.</span><span class="sxs-lookup"><span data-stu-id="f3111-191">Before delving into the details of how to think of a Pauli measurement, it is useful to think about what measuring a single qubit inside a quantum computer does to the quantum state.</span></span>
<span data-ttu-id="f3111-192">Imagine que tenhamos um $ $ estado Quantum de n-qubit; então, medindo uma qubit imediatamente, as regras de metade das $ duas possibilidades de 2 ^ n $ em que o Estado poderia estar.</span><span class="sxs-lookup"><span data-stu-id="f3111-192">Imagine that we have an $n$-qubit quantum state; then measuring one qubit immediately rules out half of the $2^n$ possibilities that state could be in.</span></span>
<span data-ttu-id="f3111-193">Em outras palavras, a medida projeta o estado da Quantum em um dos dois espaços.</span><span class="sxs-lookup"><span data-stu-id="f3111-193">In other words, the measurement projects the quantum state onto one of two half-spaces.</span></span>
<span data-ttu-id="f3111-194">Podemos generalizar a maneira como pensamos na medição para refletir essa intuição.</span><span class="sxs-lookup"><span data-stu-id="f3111-194">We can generalize the way we think about measurement to reflect this intuition.</span></span>

<span data-ttu-id="f3111-195">Para identificar esses subespaços de forma concisa, precisamos de uma linguagem para descreve-los.</span><span class="sxs-lookup"><span data-stu-id="f3111-195">In order to concisely identify these subspaces, we need a language for describing them.</span></span>
<span data-ttu-id="f3111-196">Uma maneira de descrever os dois subespaços é especificando-os por meio de uma matriz que tem apenas duas eigenvalues exclusivas, tomadas pela Convenção para ser $ \pm 1 $ .</span><span class="sxs-lookup"><span data-stu-id="f3111-196">One way to describe the two subspaces is by specifying them through a matrix that just has two unique eigenvalues, taken by convention to be $\pm 1$.</span></span>
<span data-ttu-id="f3111-197">Para obter um exemplo simples de descrição de subespaços dessa forma, considere $ Z $ :</span><span class="sxs-lookup"><span data-stu-id="f3111-197">For a simple example of describing subspaces in this way, consider $Z$:</span></span>

$$
\begin{align}
  <span data-ttu-id="f3111-198">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="f3111-198">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="f3111-199">Lendo os elementos diagonais da matriz Pauli- $ Z $ , podemos ver que $ Z $ tem dois eigenvectors, $ \ket { 0 } $ e $ \ket { 1 } $ , com eigenvalues correspondente $ \pm 1 $ .</span><span class="sxs-lookup"><span data-stu-id="f3111-199">By reading the diagonal elements of the Pauli-$Z$ matrix, we can see that $Z$ has two eigenvectors, $\ket{0}$ and $\ket{1}$, with corresponding eigenvalues $\pm 1$.</span></span>
<span data-ttu-id="f3111-200">Portanto, se medirmos o qubit e obtivermos `Zero` (correspondente ao estado $ \ket { 0 } $ ), sabemos que o estado de nosso qubit é um $ eigenstate + 1 $ do $ $ operador Z.</span><span class="sxs-lookup"><span data-stu-id="f3111-200">Thus, if we measure the qubit and obtain `Zero` (corresponding to the state $\ket{0}$), we know that the state of our qubit is a $+1$ eigenstate of the $Z$ operator.</span></span>
<span data-ttu-id="f3111-201">Da mesma forma, se obtivermos `One` , sabemos que o estado de nosso qubit é um $ -1 $ eigenstate de $ Z $ . Esse processo é mencionado na linguagem de medidas Pauli como "medindo Pauli $ Z $ " e é totalmente equivalente a executar uma medição de base computacional.</span><span class="sxs-lookup"><span data-stu-id="f3111-201">Similarly, if we obtain `One`, we know that the state of our qubit is a $-1$ eigenstate of $Z$. This process is referred to in the language of Pauli measurements as "measuring Pauli $Z$," and is entirely equivalent to performing a computational basis measurement.</span></span>

<span data-ttu-id="f3111-202">Qualquer $ \times matriz 2 2 $ que seja uma transformação unitário de $ Z $ também atende a esses critérios.</span><span class="sxs-lookup"><span data-stu-id="f3111-202">Any $2\times 2$ matrix that is a unitary transformation of $Z$ also satisfies this criteria.</span></span>
<span data-ttu-id="f3111-203">Ou seja, também poderíamos usar uma matriz $ a = u ^ \dagger Z u $ , em que $ U $ é qualquer outra matriz de unitário, para dar uma matriz que define os dois resultados de uma medida em seu $ \pm 1 $ eigenvectors.</span><span class="sxs-lookup"><span data-stu-id="f3111-203">That is, we could also use a matrix $A=U^\dagger Z U$, where $U$ is any other unitary matrix, to give a matrix that defines the two outcomes of a measurement in its $\pm 1$ eigenvectors.</span></span>
<span data-ttu-id="f3111-204">A notação de medidas Pauli faz referência a essa equivalência unitário identificando $ as medidas X, Y, Z $ como medidas equivalentes que uma delas pode fazer para obter informações de um qubit.</span><span class="sxs-lookup"><span data-stu-id="f3111-204">The notation of Pauli measurements references this unitary equivalence by identifying $X,Y,Z$ measurements as equivalent measurements that one could do to gain information from a qubit.</span></span>
<span data-ttu-id="f3111-205">Essas medidas são fornecidas abaixo para sua conveniência.</span><span class="sxs-lookup"><span data-stu-id="f3111-205">These measurements are given below for convenience.</span></span>


<span data-ttu-id="f3111-206">|Transformação unitário de medição Pauli ||</span><span class="sxs-lookup"><span data-stu-id="f3111-206">|Pauli Measurement  |Unitary transformation  |</span></span>
|-------------------|------------------------|
<span data-ttu-id="f3111-207">|$ $ Z |               $\boldone$             |</span><span class="sxs-lookup"><span data-stu-id="f3111-207">| $Z$               | $\boldone$             |</span></span>
<span data-ttu-id="f3111-208">|$ $ X | $H               $                    |</span><span class="sxs-lookup"><span data-stu-id="f3111-208">| $X$               | $H$                    |</span></span>
<span data-ttu-id="f3111-209">|$ $ S | $HS ^               {\dagger}$         |</span><span class="sxs-lookup"><span data-stu-id="f3111-209">| $Y$               | $HS^{\dagger}$         |</span></span>

<span data-ttu-id="f3111-210">Ou seja, usar esse idioma, "Measure $ Y $ " é equivalente a aplicar $ HS ^ \dagger $ e, em seguida, medir na base computacional, em que [`S`](xref:microsoft.quantum.intrinsic.s) é uma operação Quantum intrínseca às vezes chamada de "portão de fase" e pode ser simulada pela matriz unitário</span><span class="sxs-lookup"><span data-stu-id="f3111-210">That is, using this language, "measure $Y$" is equivalent to applying $HS^\dagger$ and then measuring in the computational basis, where [`S`](xref:microsoft.quantum.intrinsic.s) is an intrinsic quantum operation sometimes called the "phase gate," and can be simulated by the unitary matrix</span></span>

$$
\begin{align}
    <span data-ttu-id="f3111-211">S =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="f3111-211">S = \begin{bmatrix}</span></span>
        <span data-ttu-id="f3111-212">1 & 0 \\\\ 0 & i \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="f3111-212">1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="f3111-213">Também é equivalente a aplicar $ HS ^ \dagger $ ao vetor de estado Quantum e, em seguida, medir $ Z $ , de modo que a seguinte operação seja equivalente a `Measure([PauliY], [q])` :</span><span class="sxs-lookup"><span data-stu-id="f3111-213">It is also equivalent to applying $HS^\dagger$ to the quantum state vector and then measuring $Z$, such that the following operation is equivalent to `Measure([PauliY], [q])`:</span></span>

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

<span data-ttu-id="f3111-214">O estado correto seria então encontrado transformando de volta para a base computacional, que valores para aplicar $ sh $ ao vetor de estado Quantum; no trecho acima, a transformação de volta para a base computacional é manipulada automaticamente pelo uso do `within … apply` bloco.</span><span class="sxs-lookup"><span data-stu-id="f3111-214">The correct state would then be found by transforming back to the computational basis, which amounts to applying $SH$ to the quantum state vector; in the above snippet, the transformation back to the computational basis is handled automatically by the use of the `within … apply` block.</span></span>

<span data-ttu-id="f3111-215">No Q# , dizemos que o resultado---ou seja, as informações clássicas extraídas da interação com o estado---são dadas por um `Result` valor $ j \in \\ { \texttt { zero } , \texttt { um } \\ } $ que indica se o resultado está no $ (-1) ^ j $ eigenspace do operador Pauli medido.</span><span class="sxs-lookup"><span data-stu-id="f3111-215">In Q#, we say the outcome---that is, the classical information extracted from interacting with the state---is given by a `Result` value $j \in \\{\texttt{Zero}, \texttt{One}\\}$ indicating if the result is in the $(-1)^j$ eigenspace of the Pauli operator measured.</span></span>


## <a name="multiple-qubit-measurements"></a><span data-ttu-id="f3111-216">Medições de várias qubit</span><span class="sxs-lookup"><span data-stu-id="f3111-216">Multiple-qubit measurements</span></span>

<span data-ttu-id="f3111-217">As medições de operadores qubit Pauli são definidas da mesma forma, como visto em:</span><span class="sxs-lookup"><span data-stu-id="f3111-217">Measurements of multi-qubit Pauli operators are defined similarly, as seen from:</span></span>

$$
<span data-ttu-id="f3111-218">Z \otimes z 1 0 0 0 0 = \begin{bmatrix} & & -1 0 0 0 0 & \\\\ & & & \\\\ & & -1 & 0 \\\\ & & & \end{bmatrix} 0 0 0 1.</span><span class="sxs-lookup"><span data-stu-id="f3111-218">Z\otimes Z = \begin{bmatrix}1 &0 &0&0\\\\  0&-1&0&0\\\\ 0&0&-1&0\\\\ 0&0&0&1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="f3111-219">Assim, os produtos tensor de dois operadores Pauli- $ Z $ formam uma matriz composta de dois espaços que consistem em $ + 1 $ e $ -1 $ eigenvalues.</span><span class="sxs-lookup"><span data-stu-id="f3111-219">Thus the tensor products of two Pauli-$Z$ operators forms a matrix composed of two spaces consisting of $+1$ and $-1$ eigenvalues.</span></span>
<span data-ttu-id="f3111-220">Assim como no caso de qubit único, ambos constituem um meio-espaço que significa que metade do espaço de vetor acessível pertence ao $ + 1 $ eigenspace e à metade restante para $ -1 $ eigenspace.</span><span class="sxs-lookup"><span data-stu-id="f3111-220">As with the single-qubit case, both constitute a half-space meaning that half of the accessible vector space belongs to the $+1$ eigenspace and the remaining half to the $-1$ eigenspace.</span></span>
<span data-ttu-id="f3111-221">Em geral, é fácil ver a definição do produto tensor que qualquer produto tensor de operadores Pauli- $ Z $ e a identidade também obedece a isso.</span><span class="sxs-lookup"><span data-stu-id="f3111-221">In general, it is easy to see from the definition of the tensor product that any tensor product of Pauli-$Z$ operators and the identity also obeys this.</span></span>
<span data-ttu-id="f3111-222">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="f3111-222">For example,</span></span>

$$
\begin{align}
    <span data-ttu-id="f3111-223">\otimes \boldone Z =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="f3111-223">Z \otimes \boldone = \begin{bmatrix}</span></span>
        <span data-ttu-id="f3111-224">1 & 0 & 0 0 &\\\\</span><span class="sxs-lookup"><span data-stu-id="f3111-224">1 &  0 &  0 &  0 \\\\</span></span>
        <span data-ttu-id="f3111-225">0 &  1 &  0 &  0 \\\\</span><span class="sxs-lookup"><span data-stu-id="f3111-225">0 &  1 &  0 &  0 \\\\</span></span>
        <span data-ttu-id="f3111-226">0 &  0 & -1 &  0 \\\\</span><span class="sxs-lookup"><span data-stu-id="f3111-226">0 &  0 & -1 &  0 \\\\</span></span>
        <span data-ttu-id="f3111-227">0 &  0 &  0 & -1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="f3111-227">0 &  0 &  0 & -1 \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="f3111-228">Como antes, qualquer transformação unitário dessas matrizes também descreve dois espaços de meia rotulados por $ \pm 1 $ eigenvalues.</span><span class="sxs-lookup"><span data-stu-id="f3111-228">As before, any unitary transformation of such matrices also describes two half-spaces labeled by $\pm 1$ eigenvalues.</span></span>
<span data-ttu-id="f3111-229">Por exemplo, $ x \otimes x = h \otimes h (z \otimes z) h \otimes h $  da identidade que $ Z = HxH $ .</span><span class="sxs-lookup"><span data-stu-id="f3111-229">For example, $X\otimes X = H\otimes H(Z\otimes Z)H\otimes H$  from the identity that $Z=HXH$.</span></span>
<span data-ttu-id="f3111-230">Semelhante ao caso qubit, todas as medidas de Pauli qubit podem ser escritas como $ u ^ \dagger (Z \otimes \id ) u $ para $ 4 matrizes de 2 \times $ $ unidades $ . Enumeramos as transformações na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f3111-230">Similar to the one-qubit case, all two-qubit Pauli-measurements can be written as $U^\dagger (Z\otimes \id) U$ for $4\times 4$ unitary matrices $U$. We enumerate the transformations in the following table.</span></span>

> [!NOTE]
<span data-ttu-id="f3111-231">>Na tabela a seguir, usamos $ \operatorname { swap } $ para indicar a matriz >$$</span><span class="sxs-lookup"><span data-stu-id="f3111-231">> In the table below, we use $\operatorname{SWAP}$ to indicate the matrix > $$</span></span>
<span data-ttu-id="f3111-232">> \begin{align}</span><span class="sxs-lookup"><span data-stu-id="f3111-232">> \begin{align}</span></span>
<span data-ttu-id="f3111-233">>     \operatorname{TROCAR } &=</span><span class="sxs-lookup"><span data-stu-id="f3111-233">>     \operatorname{SWAP} & =</span></span>
<span data-ttu-id="f3111-234">>     \left( \begin { matriz}</span><span class="sxs-lookup"><span data-stu-id="f3111-234">>     \left(\begin{matrix}</span></span>
<span data-ttu-id="f3111-235">>1 & 0 & 0 0 &\\\\</span><span class="sxs-lookup"><span data-stu-id="f3111-235">>         1 & 0 & 0 & 0 \\\\</span></span>
<span data-ttu-id="f3111-236">>         0 & 0 & 1 & 0 \\\\</span><span class="sxs-lookup"><span data-stu-id="f3111-236">>         0 & 0 & 1 & 0 \\\\</span></span>
<span data-ttu-id="f3111-237">>         0 & 1 & 0 & 0 \\\\</span><span class="sxs-lookup"><span data-stu-id="f3111-237">>         0 & 1 & 0 & 0 \\\\</span></span>
<span data-ttu-id="f3111-238">>0 & 0 & 0 & 1 > \end { matriz } \right ) >     \end{align}</span><span class="sxs-lookup"><span data-stu-id="f3111-238">>         0 & 0 & 0 & 1 >     \end{matrix}\right) > \end{align}</span></span>
<span data-ttu-id="f3111-239">> $$</span><span class="sxs-lookup"><span data-stu-id="f3111-239">> $$</span></span>
<span data-ttu-id="f3111-240">> usado para simular a operação intrínseca [`SWAP`](xref:microsoft.quantum.intrinsic) .</span><span class="sxs-lookup"><span data-stu-id="f3111-240">> used to simulate the intrinsic operation [`SWAP`](xref:microsoft.quantum.intrinsic).</span></span>

<span data-ttu-id="f3111-241">|Transformação unitário de medição Pauli ||</span><span class="sxs-lookup"><span data-stu-id="f3111-241">|Pauli Measurement     |Unitary transformation  |</span></span>
|----------------------|------------------------|
<span data-ttu-id="f3111-242">|$ \otimes \boldone Z $ | $\boldone\otimes \boldone$|</span><span class="sxs-lookup"><span data-stu-id="f3111-242">| $Z\otimes \boldone$ | $\boldone\otimes \boldone$ |</span></span>
<span data-ttu-id="f3111-243">|$ \otimes \boldone X $ | $ \otimes \boldone H $|</span><span class="sxs-lookup"><span data-stu-id="f3111-243">| $X\otimes \boldone$ | $H\otimes \boldone$ |</span></span>
<span data-ttu-id="f3111-244">|$ \otimes \boldone S $ | $ HS \dagger \otimes \boldone ^ $|</span><span class="sxs-lookup"><span data-stu-id="f3111-244">| $Y\otimes \boldone$ | $HS^\dagger\otimes \boldone$ |</span></span>
<span data-ttu-id="f3111-245">|$\boldone \otimes $ | $ \operatorname { permuta } Z $|</span><span class="sxs-lookup"><span data-stu-id="f3111-245">| $\boldone \otimes Z$ | $\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="f3111-246">|$\boldone \otimes $ | $ \otimes \boldone \operatorname { permuta } X (H $ )|</span><span class="sxs-lookup"><span data-stu-id="f3111-246">| $\boldone \otimes X$ | $(H\otimes \boldone)\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="f3111-247">|$\boldone \otimes s $ | $ (HS ^ \dagger \otimes \boldone ) \operatorname { permuta } $|</span><span class="sxs-lookup"><span data-stu-id="f3111-247">| $\boldone \otimes Y$ | $(HS^\dagger\otimes \boldone)\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="f3111-248">|$Z \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } $|</span><span class="sxs-lookup"><span data-stu-id="f3111-248">| $Z\otimes Z$ | $\operatorname{CNOT}\_{10}$ |</span></span>
<span data-ttu-id="f3111-249">|$X \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes \boldone ) $|</span><span class="sxs-lookup"><span data-stu-id="f3111-249">| $X\otimes Z$ | $\operatorname{CNOT}\_{10}(H\otimes \boldone)$ |</span></span>
<span data-ttu-id="f3111-250">|$S \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes \boldone ) $|</span><span class="sxs-lookup"><span data-stu-id="f3111-250">| $Y\otimes Z$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes \boldone)$ |</span></span>
<span data-ttu-id="f3111-251">|$Z \otimes X $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes H) $|</span><span class="sxs-lookup"><span data-stu-id="f3111-251">| $Z\otimes X$ | $\operatorname{CNOT}\_{10}(\boldone\otimes H)$ |</span></span>
<span data-ttu-id="f3111-252">|$X \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (h \otimes h) $|</span><span class="sxs-lookup"><span data-stu-id="f3111-252">| $X\otimes X$ | $\operatorname{CNOT}\_{10}(H\otimes H)$ |</span></span>
<span data-ttu-id="f3111-253">|$S \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes H) $|</span><span class="sxs-lookup"><span data-stu-id="f3111-253">| $Y\otimes X$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes H)$ |</span></span>
<span data-ttu-id="f3111-254">|$Z \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes HS ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="f3111-254">| $Z\otimes Y$ | $\operatorname{CNOT}\_{10}(\boldone \otimes HS^\dagger)$ |</span></span>
<span data-ttu-id="f3111-255">|$X \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes HS ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="f3111-255">| $X\otimes Y$ | $\operatorname{CNOT}\_{10}(H\otimes HS^\dagger)$ |</span></span>
<span data-ttu-id="f3111-256">|$S \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes HS ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="f3111-256">| $Y\otimes Y$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes HS^\dagger)$ |</span></span>

<span data-ttu-id="f3111-257">Aqui, a [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) operação é exibida pelo seguinte motivo.</span><span class="sxs-lookup"><span data-stu-id="f3111-257">Here, the [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) operation appears for the following reason.</span></span>
<span data-ttu-id="f3111-258">Cada medida de Pauli que não inclui a $ \boldone $ matriz é equivalente a um unitário de $ z \otimes z $ pelo raciocínio acima.</span><span class="sxs-lookup"><span data-stu-id="f3111-258">Each Pauli measurement that does not include the $\boldone$ matrix is equivalent up to a unitary to $Z\otimes Z$ by the above reasoning.</span></span>
<span data-ttu-id="f3111-259">O eigenvalues de $ z \otimes z $ depende apenas da paridade do qubits que compõe cada vetor base computacional, e as operações controladas não servem para computar essa paridade e armazená-las no primeiro bit.</span><span class="sxs-lookup"><span data-stu-id="f3111-259">The eigenvalues of $Z\otimes Z$ only depend on the parity of the qubits that comprise each computational basis vector, and the controlled-not operations serve to compute this parity and store it in the first bit.</span></span>
<span data-ttu-id="f3111-260">Depois que o primeiro bit é medido, podemos recuperar a identidade do espaço resultante, que é equivalente a medir o operador Pauli.</span><span class="sxs-lookup"><span data-stu-id="f3111-260">Then once the first bit is measured, we can recover the identity of the resultant half-space, which is equivalent to measuring the Pauli operator.</span></span>

<span data-ttu-id="f3111-261">Uma observação adicional: embora possa ser tentador pressupor que medir $ z \otimes z $ é o mesmo que medir sequencialmente $ Z \otimes \mathbb { 1 } $ e, em seguida $ \mathbb { , 1 } \otimes Z $ , essa suposição seria falsa.</span><span class="sxs-lookup"><span data-stu-id="f3111-261">One additional note: while it may be tempting to assume that measuring $Z\otimes Z$ is the same as sequentially measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$, this assumption would be false.</span></span>
<span data-ttu-id="f3111-262">O motivo é que a medição de $ \otimes projetos z z é $ o estado da Quantum na $ eigenstate + 1 $ ou $ -1 $ desses operadores.</span><span class="sxs-lookup"><span data-stu-id="f3111-262">The reason is that measuring $Z\otimes Z$ projects the quantum state into either the $+1$ or $-1$ eigenstate of these operators.</span></span>
<span data-ttu-id="f3111-263">Medindo $ \otimes \mathbb { o z 1 } $ e, em seguida, $ \mathbb { 1 } \otimes $ a z projeta o vetor de estado da Quantum primeiro em um semestre de $ Z \otimes \mathbb { 1 } $ e, em seguida, em um semestre de $ \mathbb { 1 a } \otimes z $ . Como há quatro vetores de base computacional, a execução de ambas as medidas reduz o estado para um quarto de espaço e, portanto, reduz-a para um único vetor de computação.</span><span class="sxs-lookup"><span data-stu-id="f3111-263">Measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$ projects the quantum state vector first onto a half space of $Z\otimes \mathbb{1}$ and then onto a half space of $\mathbb{1} \otimes Z$. As there are four computational basis vectors, performing both measurements reduces the state to a quarter-space and hence reduces it to a single computational basis vector.</span></span>

## <a name="correlations-between-qubits"></a><span data-ttu-id="f3111-264">Correlações entre qubits</span><span class="sxs-lookup"><span data-stu-id="f3111-264">Correlations between qubits</span></span>
<span data-ttu-id="f3111-265">Outra maneira de observar a medição de produtos tensor de matrizes Pauli como $ x \otimes x $ ou $ z \otimes z $ é que essas medidas permitem que você examine as informações armazenadas nas correlações entre os dois qubits.</span><span class="sxs-lookup"><span data-stu-id="f3111-265">Another way of looking at measuring tensor products of Pauli matrices such as $X\otimes X$ or $Z\otimes Z$ is that these measurements let you look at information stored in the correlations between the two qubits.</span></span>
<span data-ttu-id="f3111-266">A medição de $ X \otimes \id $ permite que você examine as informações armazenadas localmente no primeiro qubit.</span><span class="sxs-lookup"><span data-stu-id="f3111-266">Measuring $X\otimes \id$ lets you look at information that is locally stored in the first qubit.</span></span>
<span data-ttu-id="f3111-267">Embora os dois tipos de medidas sejam igualmente valiosos na computação Quantum, o primeiro ilumina o poder da computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="f3111-267">While both types of measurements are equally valuable in quantum computing, the former illuminates the power of quantum computing.</span></span>
<span data-ttu-id="f3111-268">Ele revela que, na computação Quantum, geralmente as informações que você deseja aprender não são armazenadas em nenhum único qubit, mas armazenadas não localmente em todas as qubits de uma vez e, portanto, apenas examinando-as por meio de uma medida conjunta (por exemplo, $ z \otimes z $ ), essas informações se tornam manifestos.</span><span class="sxs-lookup"><span data-stu-id="f3111-268">It reveals that in quantum computing, often the information you wish to learn is not stored in any single qubit but rather stored non-locally in all the qubits at once, and therefore only by looking at it through a joint measurement (e.g. $Z\otimes Z$) does this information become manifest.</span></span>

<span data-ttu-id="f3111-269">Por exemplo, na correção de erros, muitas vezes desejamos saber qual erro ocorreu ao aprender nada sobre o estado que estamos tentando proteger.</span><span class="sxs-lookup"><span data-stu-id="f3111-269">For example, in error correction, we often wish to learn what error occurred while learning nothing about the state that we're trying to protect.</span></span>
<span data-ttu-id="f3111-270">O [exemplo de código de inversão de bits](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) mostra um exemplo de como você pode fazer isso usando medidas como $ z \otimes z \otimes \id $ e $ \id \otimes z z \otimes $ . < ! --TODO: altere isso para um link para o navegador de exemplos assim que o exemplo de código de inversão de bits estiver integrado.</span><span class="sxs-lookup"><span data-stu-id="f3111-270">The [bit-flip code sample](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) shows an example of how you can do that using measurements like $Z \otimes Z \otimes \id$ and $\id \otimes Z \otimes Z$. <!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded.</span></span> -->

<span data-ttu-id="f3111-271">Operadores Pauli arbitrários, como $ X \otimes Y Z, \otimes \otimes \boldone $ também podem ser medidos.</span><span class="sxs-lookup"><span data-stu-id="f3111-271">Arbitrary Pauli operators such as $X\otimes Y \otimes Z \otimes \boldone$ can also be measured.</span></span>
<span data-ttu-id="f3111-272">Todos esses produtos tensor de operadores Pauli têm apenas dois eigenvalues $ \pm 1 $ e ambos eigenspaces constituem metades do espaço de vetor inteiro.</span><span class="sxs-lookup"><span data-stu-id="f3111-272">All such tensor products of Pauli operators have only two eigenvalues $\pm 1$ and both eigenspaces constitute half-spaces of the entire vector space.</span></span>
<span data-ttu-id="f3111-273">Portanto, eles coincidem com os requisitos declarados acima.</span><span class="sxs-lookup"><span data-stu-id="f3111-273">Thus they coincide with the requirements stated above.</span></span>

<span data-ttu-id="f3111-274">No Q# , essas medidas retornam $ j $ se a medida produz um resultado no eigenspace de sinal $ (-1) ^ j $ .</span><span class="sxs-lookup"><span data-stu-id="f3111-274">In Q#, such measurements return $j$ if the measurement yields a result in the eigenspace of sign $(-1)^j$.</span></span>
<span data-ttu-id="f3111-275">Ter medidas de Pauli como um recurso interno no Q# é útil porque a medição desses operadores requer cadeias longas de Gates e transformações de base controladas para descrever a diagonal de $ U $ portão necessário para expressar a operação como um produto tensor de $ Z $ e $ \id $ .</span><span class="sxs-lookup"><span data-stu-id="f3111-275">Having Pauli measurements as a built-in feature in Q# is helpful because measuring such operators requires long chains of controlled-NOT gates and basis transformations to describe the diagonalizing $U$ gate needed to express the operation as a tensor product of $Z$ and $\id$.</span></span>
<span data-ttu-id="f3111-276">Ao ser capaz de especificar que você deseja realizar uma dessas medidas predefinidas, você não precisa se preocupar em como transformar sua base de forma que uma medida de base computacional forneça as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="f3111-276">By being able to specify that you wish to do one of these pre-defined measurements, you don't need to worry about how to transform your basis such that a computational basis measurement provides the necessary information.</span></span>
<span data-ttu-id="f3111-277">Q# manipula todas as transformações de base necessárias automaticamente para você.</span><span class="sxs-lookup"><span data-stu-id="f3111-277">Q# handles all the necessary basis transformations for you automatically.</span></span>
<span data-ttu-id="f3111-278">Para obter mais informações, consulte [`Measure`](xref:microsoft.quantum.intrinsic.measure) as [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) operações e.</span><span class="sxs-lookup"><span data-stu-id="f3111-278">For more information, see the [`Measure`](xref:microsoft.quantum.intrinsic.measure) and [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) operations.</span></span>

## <a name="the-no-cloning-theorem"></a><span data-ttu-id="f3111-279">O teorema no-Cloning</span><span class="sxs-lookup"><span data-stu-id="f3111-279">The No-Cloning Theorem</span></span>

<span data-ttu-id="f3111-280">As informações da Quantum são poderosas.</span><span class="sxs-lookup"><span data-stu-id="f3111-280">Quantum information is powerful.</span></span>
<span data-ttu-id="f3111-281">Ele nos permite fazer coisas incríveis, como números de fator exponencialmente mais rápidos do que os melhores algoritmos clássicos conhecidos, ou simular com eficiência sistemas de informações de alta correlação que exigem, de modo clássico, o custo exponencial para simular com precisão.</span><span class="sxs-lookup"><span data-stu-id="f3111-281">It enables us to do amazing things such as factor numbers exponentially faster than the best known classical algorithms, or efficiently simulate correlated electron systems that classically require exponential cost to simulate accurately.</span></span>
<span data-ttu-id="f3111-282">No entanto, há limitações no poder da computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="f3111-282">However, there are limitations to the power of quantum computing.</span></span>
<span data-ttu-id="f3111-283">Uma dessas limitações é fornecida pelo *teorema no-Cloning*.</span><span class="sxs-lookup"><span data-stu-id="f3111-283">One such limitation is given by the *No-Cloning Theorem*.</span></span>

<span data-ttu-id="f3111-284">O teorema no-Cloning é adequadamente nomeado.</span><span class="sxs-lookup"><span data-stu-id="f3111-284">The No-Cloning Theorem is aptly named.</span></span>
<span data-ttu-id="f3111-285">Ele não permite a clonagem de Estados de Quantum genérico por um computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="f3111-285">It disallows cloning of generic quantum states by a quantum computer.</span></span>
<span data-ttu-id="f3111-286">A prova do teorema é bastante simples.</span><span class="sxs-lookup"><span data-stu-id="f3111-286">The proof of the theorem is remarkably straightforward.</span></span>
<span data-ttu-id="f3111-287">Embora uma prova completa do teorema sem clonagem seja um pouco técnica para nossa discussão aqui, a prova no caso de nenhum qubits auxiliar adicional está dentro de nosso escopo (auxiliares qubits são qubits usados para espaço transitório durante uma computação e são facilmente usados e gerenciados no Q# , consulte [qubits emprestados](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span><span class="sxs-lookup"><span data-stu-id="f3111-287">While a full proof of the no-cloning theorem is a little too technical for our discussion here, the proof in the case of no additional auxiliary qubits is within our scope (auxiliary qubits are qubits used for scratch space during a computation and are easily used and managed in Q#, see [borrowed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span></span>

<span data-ttu-id="f3111-288">Para esse computador Quantum, a operação de clonagem deve ser descrita por uma matriz unitário.</span><span class="sxs-lookup"><span data-stu-id="f3111-288">For such a quantum computer, the cloning operation must be described by a unitary matrix.</span></span>
<span data-ttu-id="f3111-289">Não permitimos a medição, já que corromperia o estado Quantum que estamos tentando clonar.</span><span class="sxs-lookup"><span data-stu-id="f3111-289">We disallow measurement, since it would corrupt the quantum state we are trying to clone.</span></span>
<span data-ttu-id="f3111-290">Para simular a operação de clonagem, queremos que a matriz unitário usada tenha a propriedade que $$</span><span class="sxs-lookup"><span data-stu-id="f3111-290">To simulate the cloning operation, we want the unitary matrix used to have the property that $$</span></span>
  <span data-ttu-id="f3111-291">U \ket { \psi } \ket { 0 } = \ket { \psi }\ket{\psi}</span><span class="sxs-lookup"><span data-stu-id="f3111-291">U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}</span></span>
$$
<span data-ttu-id="f3111-292">para qualquer estado $ \ket { \psi } $ .</span><span class="sxs-lookup"><span data-stu-id="f3111-292">for any state $\ket{\psi}$.</span></span>
<span data-ttu-id="f3111-293">Em seguida, a propriedade linear da multiplicação de matriz implica que, para qualquer segundo estado Quantum $ \ket { \phi } $ ,</span><span class="sxs-lookup"><span data-stu-id="f3111-293">The linearity property of matrix multiplication then implies that for any second quantum state $\ket{\phi}$,</span></span>

$$
\begin{align}
    <span data-ttu-id="f3111-294">U \left [ \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ] \ket { 0}</span><span class="sxs-lookup"><span data-stu-id="f3111-294">U \left[ \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right] \ket{0}</span></span>
    <span data-ttu-id="f3111-295">&= \frac{ 1 } { \sqrt { 2 } } U \ket { \phi } \ket { 0}</span><span class="sxs-lookup"><span data-stu-id="f3111-295">& = \frac{1}{\sqrt{2}} U\ket{\phi}\ket{0}</span></span>
      <span data-ttu-id="f3111-296">+ \frac{1 } { \sqrt { 2 } } U \ket { \psi } \ket { 0 }\\\\</span><span class="sxs-lookup"><span data-stu-id="f3111-296">+ \frac{1}{\sqrt{2}} U\ket{\psi}\ket{0} \\\\</span></span>
    <span data-ttu-id="f3111-297">&= \frac{ 1 } { \sqrt { 2 } } \left ( \ket { \phi } \ket { \phi }  +  \ket { \psi }\ket{\psi}</span><span class="sxs-lookup"><span data-stu-id="f3111-297">& = \frac{1}{\sqrt{2}} \left( \ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi}</span></span>
        <span data-ttu-id="f3111-298">\right) \\\\</span><span class="sxs-lookup"><span data-stu-id="f3111-298">\right) \\\\</span></span>
    <span data-ttu-id="f3111-299">&\ne \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ) \otimes \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ).</span><span class="sxs-lookup"><span data-stu-id="f3111-299">& \ne \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right) \otimes \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right).</span></span>
\end{align}
$$

<span data-ttu-id="f3111-300">Isso fornece a intuição fundamental por trás do teorema sem clonagem: qualquer dispositivo que copia um estado de Quantum desconhecido deve induzir erros em pelo menos alguns dos Estados que ele copia.</span><span class="sxs-lookup"><span data-stu-id="f3111-300">This provides the fundamental intuition behind the No-Cloning Theorem: any device that copies an unknown quantum state must induce errors on at least some of the states it copies.</span></span>
<span data-ttu-id="f3111-301">Embora a principal suposição de que o Cloner atue linearmente no estado de entrada possa ser violada por meio da adição e da medição do qubits auxiliar, essas interações também vazam informações sobre o sistema por meio de estatísticas de medição e impedem a clonagem exata nesses casos.</span><span class="sxs-lookup"><span data-stu-id="f3111-301">While the key assumption that the cloner acts linearly on the input state can be violated through the addition and measurement of auxiliary qubits, such interactions also leak information about the system through the measurement statistics and prevent exact cloning in such cases as well.</span></span>
<span data-ttu-id="f3111-302">Para obter uma prova mais completa dos teorema sem clonagem, consulte [para obter mais informações](xref:microsoft.quantum.more-information).</span><span class="sxs-lookup"><span data-stu-id="f3111-302">For a more complete proof of the No-Cloning Theorem see [For more information](xref:microsoft.quantum.more-information).</span></span>

<span data-ttu-id="f3111-303">O teorema no-Cloning é importante para uma compreensão qualitativa da computação Quantum porque, se você puder clonar os Estados da Quantum de forma incara, terá uma capacidade quase mágico de aprender com os Estados da Quantum.</span><span class="sxs-lookup"><span data-stu-id="f3111-303">The No-Cloning Theorem is important for qualitative understanding of quantum computing because if you could clone quantum states inexpensively then you would be granted a near-magical ability to learn from quantum states.</span></span>
<span data-ttu-id="f3111-304">Na verdade, você poderia violar o princípio de incerteza de vaunted da Heisenberg.</span><span class="sxs-lookup"><span data-stu-id="f3111-304">Indeed, you could violate Heisenberg's vaunted uncertainty principle.</span></span>
<span data-ttu-id="f3111-305">Como alternativa, você pode usar um Cloner ideal para pegar um único exemplo de uma distribuição de Quantum complexa e aprender tudo o que poderia ser possível saber sobre essa distribuição de apenas uma amostra.</span><span class="sxs-lookup"><span data-stu-id="f3111-305">Alternatively, you could use an optimal cloner to take a single sample from a complex quantum distribution and learn everything you could possibly learn about that distribution from just one sample.</span></span>
<span data-ttu-id="f3111-306">Isso seria como você invertendo uma moeda e observando a cabeça e, depois, ao informar a um amigo sobre o resultado que eles respondem "Ah, a distribuição dessa moeda deve ser Bernoulli com $ p = 0.512643 \ ldots $ !"</span><span class="sxs-lookup"><span data-stu-id="f3111-306">This would be like you flipping a coin and observing heads and then upon telling a friend about the result having them respond "Ah the distribution of that coin must be Bernoulli with $p=0.512643\ldots$!"</span></span>  <span data-ttu-id="f3111-307">Essa instrução seria não sensical porque um pouco de informação (o resultado dos cabeçotes) simplesmente não pode fornecer muitas informações necessárias para codificar a distribuição sem informações substanciais anteriores.</span><span class="sxs-lookup"><span data-stu-id="f3111-307">Such a statement would be non-sensical because one bit of information (the heads outcome) simply cannot provide the many bits of information needed to encode the distribution without substantial prior information.</span></span>
<span data-ttu-id="f3111-308">Da mesma forma, sem informações anteriores, não podemos clonar perfeitamente um estado Quantum da mesma forma que não podemos preparar uma Ensemble dessas moedas sem saber $ p $ .</span><span class="sxs-lookup"><span data-stu-id="f3111-308">Similarly, without prior information we cannot perfectly clone a quantum state just as we cannot prepare an ensemble of such coins without knowing $p$.</span></span>

<span data-ttu-id="f3111-309">As informações não são gratuitas na computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="f3111-309">Information is not free in quantum computing.</span></span>
<span data-ttu-id="f3111-310">Cada qubit medido fornece uma única informação, e o teorema no-Cloning mostra que não há nenhum backdoor que possa ser explorado para contornar a compensação fundamental entre as informações obtidas sobre o sistema e o distúrbios invocado sobre ele.</span><span class="sxs-lookup"><span data-stu-id="f3111-310">Each qubit measured gives a single bit of information, and the No-Cloning Theorem shows that there is no backdoor that can be exploited to get around the fundamental tradeoff between information gained about the system and the disturbance invoked upon it.</span></span>
