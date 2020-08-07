---
<span data-ttu-id="213f7-101">Título: vetores e matrizes na descrição da computação Quantum: Aprenda as noções básicas de como trabalhar com vetores e matrizes.</span><span class="sxs-lookup"><span data-stu-id="213f7-101">title: Vectors and matrices in quantum computing description: Learn the basics of how to work with vectors and matrices.</span></span>
<span data-ttu-id="213f7-102">Autor: QuantumWriter UID: Microsoft. Quantum. Concepts. vetores MS. Author: nawiebe@microsoft.com MS. Data: 12/11/2017 MS. Topic: artigo no-loc:</span><span class="sxs-lookup"><span data-stu-id="213f7-102">author: QuantumWriter uid: microsoft.quantum.concepts.vectors ms.author: nawiebe@microsoft.com ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="213f7-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="213f7-103">"Q#"</span></span>
- <span data-ttu-id="213f7-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="213f7-104">"$$v"</span></span>
- <span data-ttu-id="213f7-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="213f7-105">"$$"</span></span>
- <span data-ttu-id="213f7-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="213f7-106">"$$"</span></span>
- <span data-ttu-id="213f7-107">"$"</span><span class="sxs-lookup"><span data-stu-id="213f7-107">"$"</span></span>
- <span data-ttu-id="213f7-108">"$"</span><span class="sxs-lookup"><span data-stu-id="213f7-108">"$"</span></span>
- <span data-ttu-id="213f7-109">"$"</span><span class="sxs-lookup"><span data-stu-id="213f7-109">"$"</span></span>
- <span data-ttu-id="213f7-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="213f7-110">"$$"</span></span>
- <span data-ttu-id="213f7-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="213f7-111">"\cdots"</span></span>
- <span data-ttu-id="213f7-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="213f7-112">"bmatrix"</span></span>
- <span data-ttu-id="213f7-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="213f7-113">"\ddots"</span></span>
- <span data-ttu-id="213f7-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="213f7-114">"\equiv"</span></span>
- <span data-ttu-id="213f7-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="213f7-115">"\sum"</span></span>
- <span data-ttu-id="213f7-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="213f7-116">"\begin"</span></span>
- <span data-ttu-id="213f7-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="213f7-117">"\end"</span></span>
- <span data-ttu-id="213f7-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="213f7-118">"\sqrt"</span></span>
- <span data-ttu-id="213f7-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="213f7-119">"\otimes"</span></span>
- <span data-ttu-id="213f7-120">"{"</span><span class="sxs-lookup"><span data-stu-id="213f7-120">"{"</span></span>
- <span data-ttu-id="213f7-121">"}"</span><span class="sxs-lookup"><span data-stu-id="213f7-121">"}"</span></span>
- <span data-ttu-id="213f7-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="213f7-122">"\text"</span></span>
- <span data-ttu-id="213f7-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="213f7-123">"\phi"</span></span>
- <span data-ttu-id="213f7-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="213f7-124">"\kappa"</span></span>
- <span data-ttu-id="213f7-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="213f7-125">"\psi"</span></span>
- <span data-ttu-id="213f7-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="213f7-126">"\alpha"</span></span>
- <span data-ttu-id="213f7-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="213f7-127">"\beta"</span></span>
- <span data-ttu-id="213f7-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="213f7-128">"\gamma"</span></span>
- <span data-ttu-id="213f7-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="213f7-129">"\delta"</span></span>
- <span data-ttu-id="213f7-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="213f7-130">"\omega"</span></span>
- <span data-ttu-id="213f7-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="213f7-131">"\bra"</span></span>
- <span data-ttu-id="213f7-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="213f7-132">"\ket"</span></span>
- <span data-ttu-id="213f7-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="213f7-133">"\boldone"</span></span>
- <span data-ttu-id="213f7-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="213f7-134">"\\\\"</span></span>
- <span data-ttu-id="213f7-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="213f7-135">"\\"</span></span>
- <span data-ttu-id="213f7-136">"="</span><span class="sxs-lookup"><span data-stu-id="213f7-136">"="</span></span>
- <span data-ttu-id="213f7-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="213f7-137">"\frac"</span></span>
- <span data-ttu-id="213f7-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="213f7-138">"\text"</span></span>
- <span data-ttu-id="213f7-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="213f7-139">"\mapsto"</span></span>
- <span data-ttu-id="213f7-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="213f7-140">"\dagger"</span></span>
- <span data-ttu-id="213f7-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="213f7-141">"\to"</span></span>
- <span data-ttu-id="213f7-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="213f7-142">"\begin{cases}"</span></span>
- <span data-ttu-id="213f7-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="213f7-143">"\end{cases}"</span></span>
- <span data-ttu-id="213f7-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="213f7-144">"\operatorname"</span></span>
- <span data-ttu-id="213f7-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="213f7-145">"\braket"</span></span>
- <span data-ttu-id="213f7-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="213f7-146">"\id"</span></span>
- <span data-ttu-id="213f7-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="213f7-147">"\expect"</span></span>
- <span data-ttu-id="213f7-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="213f7-148">"\defeq"</span></span>
- <span data-ttu-id="213f7-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="213f7-149">"\variance"</span></span>
- <span data-ttu-id="213f7-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="213f7-150">"\dd"</span></span>
- <span data-ttu-id="213f7-151">"&"</span><span class="sxs-lookup"><span data-stu-id="213f7-151">"&"</span></span>
- <span data-ttu-id="213f7-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="213f7-152">"\begin{align}"</span></span>
- <span data-ttu-id="213f7-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="213f7-153">"\end{align}"</span></span>
- <span data-ttu-id="213f7-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="213f7-154">"\Lambda"</span></span>
- <span data-ttu-id="213f7-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="213f7-155">"\lambda"</span></span>
- <span data-ttu-id="213f7-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="213f7-156">"\Omega"</span></span>
- <span data-ttu-id="213f7-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="213f7-157">"\mathrm"</span></span>
- <span data-ttu-id="213f7-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="213f7-158">"\left"</span></span>
- <span data-ttu-id="213f7-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="213f7-159">"\right"</span></span>
- <span data-ttu-id="213f7-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="213f7-160">"\qquad"</span></span>
- <span data-ttu-id="213f7-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="213f7-161">"\times"</span></span>
- <span data-ttu-id="213f7-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="213f7-162">"\big"</span></span>
- <span data-ttu-id="213f7-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="213f7-163">"\langle"</span></span>
- <span data-ttu-id="213f7-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="213f7-164">"\rangle"</span></span>
- <span data-ttu-id="213f7-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="213f7-165">"\bigg"</span></span>
- <span data-ttu-id="213f7-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="213f7-166">"\Big"</span></span>
- <span data-ttu-id="213f7-167">"|"</span><span class="sxs-lookup"><span data-stu-id="213f7-167">"|"</span></span>
- <span data-ttu-id="213f7-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="213f7-168">"\mathbb"</span></span>
- <span data-ttu-id="213f7-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="213f7-169">"\vec"</span></span>
- <span data-ttu-id="213f7-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="213f7-170">"\in"</span></span>
- <span data-ttu-id="213f7-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="213f7-171">"\texttt"</span></span>
- <span data-ttu-id="213f7-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="213f7-172">"\ne"</span></span>
- <span data-ttu-id="213f7-173">"<"</span><span class="sxs-lookup"><span data-stu-id="213f7-173">"<"</span></span>
- <span data-ttu-id="213f7-174">">"</span><span class="sxs-lookup"><span data-stu-id="213f7-174">">"</span></span>
- <span data-ttu-id="213f7-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="213f7-175">"\leq"</span></span>
- <span data-ttu-id="213f7-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="213f7-176">"\geq"</span></span>
- <span data-ttu-id="213f7-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="213f7-177">"~~"</span></span>
- <span data-ttu-id="213f7-178">"~"</span><span class="sxs-lookup"><span data-stu-id="213f7-178">"~"</span></span>
- <span data-ttu-id="213f7-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="213f7-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="213f7-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="213f7-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="213f7-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="213f7-181">"\_"</span></span>

---

# <a name="vectors-and-matrices"></a><span data-ttu-id="213f7-182">Vetores e matrizes</span><span class="sxs-lookup"><span data-stu-id="213f7-182">Vectors and Matrices</span></span>

<span data-ttu-id="213f7-183">Alguma familiaridade com vetores e matrizes é essencial para entender a computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="213f7-183">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="213f7-184">Fornecemos uma breve introdução abaixo e os leitores interessados são recomendados para ler uma referência padrão em Algebra linear, como *Strang, G. (1993). Introdução à algebra linear (Vol. 3). Wellesley, MA: Wellesley-Cambridge, Press* ou uma referência online, como [Algebra linear](http://joshua.smcvt.edu/linearalgebra/).</span><span class="sxs-lookup"><span data-stu-id="213f7-184">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="213f7-185">Um vetor de coluna (ou simplesmente [*vetor*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ v $ de Dimension (ou tamanho) $ n $ é uma coleção de $ n $ números complexos $ (v_1, v_2, \ldots, v_n) $ organizados como uma coluna:</span><span class="sxs-lookup"><span data-stu-id="213f7-185">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="213f7-186">$$v =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-186">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="213f7-187">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-187">v_1\\\\</span></span>
<span data-ttu-id="213f7-188">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-188">v_2\\\\</span></span>
<span data-ttu-id="213f7-189">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-189">\vdots\\\\</span></span>
<span data-ttu-id="213f7-190">v_n\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="213f7-190">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="213f7-191">A norma de um vetor $ v $ é definida como $ \sqrt { \sum \_ i | v \_ | ^ 2 } $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-191">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="213f7-192">Um vetor é considerado como sendo a norma da unidade (ou, como alternativa, é chamado de [*vetor de unidade*](https://en.wikipedia.org/wiki/Unit_vector)) se a sua norma for $ 1 $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-192">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="213f7-193">O [*adjoin de um vetor*](https://en.wikipedia.org/wiki/Adjoint_matrix) $ v $ é indicado $ como v ^ \dagger $ e é definido para ser o seguinte vetor de linha, em que $ \* $ denota o conjugado complexo,</span><span class="sxs-lookup"><span data-stu-id="213f7-193">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="213f7-194">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} v_1 ^ \* & \cdots & v_n ^ \*\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="213f7-194">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="213f7-195">A maneira mais comum de multiplicar dois vetores juntos é por meio do [*produto interno*](https://en.wikipedia.org/wiki/Inner_product_space), também conhecido como produto de ponto.</span><span class="sxs-lookup"><span data-stu-id="213f7-195">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="213f7-196">O produto interno fornece a projeção de um vetor para outro e é inestimável na descrição de como expressar um vetor como uma soma de outros vetores mais simples.</span><span class="sxs-lookup"><span data-stu-id="213f7-196">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="213f7-197">O produto interno entre $ u $ e $ v $ , denotado $ \left \langle u, v \right \rangle $ é definido como</span><span class="sxs-lookup"><span data-stu-id="213f7-197">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

$$
<span data-ttu-id="213f7-198">\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="213f7-198">\langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="213f7-199">Essa notação também permite que a norma de um vetor $ v $ seja escrita como $ \sqrt { \langle v, v \rangle } $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-199">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="213f7-200">Podemos multiplicar um vetor com um número $ c $ para formar um novo vetor cujas entradas são multiplicadas por $ c $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-200">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="213f7-201">Também podemos adicionar dois vetores $ u $ e $ v $ para formar um novo vetor cujas entradas são a soma das entradas de $ u $ e $ v $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-201">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="213f7-202">Essas operações são descritas abaixo:</span><span class="sxs-lookup"><span data-stu-id="213f7-202">These operations are depicted below:</span></span>

<span data-ttu-id="213f7-203">$$\mathrm{Se } ~ u=\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-203">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="213f7-204">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-204">u_1\\\\</span></span>
<span data-ttu-id="213f7-205">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-205">u_2\\\\</span></span>
<span data-ttu-id="213f7-206">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-206">\vdots\\\\</span></span>
<span data-ttu-id="213f7-207">u_n \end{bmatrix} ~ \mathrm { e}~</span><span class="sxs-lookup"><span data-stu-id="213f7-207">u_n \end{bmatrix}~\mathrm{and}~</span></span>
<span data-ttu-id="213f7-208">l=\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-208">v =\begin{bmatrix}</span></span>
    <span data-ttu-id="213f7-209">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-209">v_1\\\\</span></span>
    <span data-ttu-id="213f7-210">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-210">v_2\\\\</span></span>
    <span data-ttu-id="213f7-211">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-211">\vdots\\\\</span></span>
    <span data-ttu-id="213f7-212">v_n \end{bmatrix} , ~ \mathrm { em seguida,}~</span><span class="sxs-lookup"><span data-stu-id="213f7-212">v_n \end{bmatrix},~\mathrm{then}~</span></span>
<span data-ttu-id="213f7-213">au + BV=\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-213">au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="213f7-214">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-214">au_1+bv_1\\\\</span></span>
<span data-ttu-id="213f7-215">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-215">au_2+bv_2\\\\</span></span>
<span data-ttu-id="213f7-216">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-216">\vdots\\\\</span></span>
<span data-ttu-id="213f7-217">au_n + bv_n \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="213f7-217">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="213f7-218">Uma [*matriz*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) de tamanho $ m \times n $ é uma coleção de $ $ números complexos de MN organizadas nas $ $ linhas m e $ n $ colunas, conforme mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="213f7-218">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="213f7-219">$$D=</span><span class="sxs-lookup"><span data-stu-id="213f7-219">$$M =</span></span> 
\begin{bmatrix}
<span data-ttu-id="213f7-220">M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-220">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\</span></span>
<span data-ttu-id="213f7-221">M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-221">M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="213f7-222">M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { MN}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-222">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\</span></span>
<span data-ttu-id="213f7-223">\end{bmatrix}.$$</span><span class="sxs-lookup"><span data-stu-id="213f7-223">\end{bmatrix}.$$</span></span>

<span data-ttu-id="213f7-224">Observe que um vetor de dimensão $ n $ é simplesmente uma matriz de tamanho $ n \times 1 $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-224">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="213f7-225">Assim como acontece com os vetores, podemos multiplicar uma matriz com um número $ c $ para obter uma nova matriz em que cada entrada é multiplicada por $ c $ , e podemos adicionar duas matrizes do mesmo tamanho para produzir uma nova matriz cujas entradas são a soma das respectivas entradas das duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="213f7-225">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="213f7-226">Multiplicação de matriz e produtos tensor</span><span class="sxs-lookup"><span data-stu-id="213f7-226">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="213f7-227">Também podemos multiplicar duas matrizes $ m $ da dimensão $ m \times n $ e $ n $ da dimensão $ n \times p $ para obter uma nova matriz $ p $ da dimensão $ m p da \times $ seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="213f7-227">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

\begin{align}
&\begin{bmatrix}
    <span data-ttu-id="213f7-228">M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-228">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\</span></span>
    <span data-ttu-id="213f7-229">M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-229">M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\</span></span>
    \ddots\\\\
    <span data-ttu-id="213f7-230">M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { MN}</span><span class="sxs-lookup"><span data-stu-id="213f7-230">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
\end{bmatrix}
\begin{bmatrix}
<span data-ttu-id="213f7-231">N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1P}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-231">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\</span></span>
<span data-ttu-id="213f7-232">N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2P}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-232">N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="213f7-233">N_ { N1 } ~~ N_ { N2 } ~~ \cdots ~~ N_ { NP}</span><span class="sxs-lookup"><span data-stu-id="213f7-233">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
\end{bmatrix}=\begin{bmatrix}
<span data-ttu-id="213f7-234">P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1P}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-234">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\</span></span>
<span data-ttu-id="213f7-235">P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2P}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-235">P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="213f7-236">P_ { M1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { MP}</span><span class="sxs-lookup"><span data-stu-id="213f7-236">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
\end{bmatrix}
\end{align}

<span data-ttu-id="213f7-237">onde as entradas de $ P $ são $ P_ { IK } = \sum _j M_ { IJ } N_ { JK } $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-237">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="213f7-238">Por exemplo, a entrada $ P_ { 11 } $ é o produto interno da primeira linha de $ M $ com a primeira coluna de $ N $ . Observe que, como um vetor é simplesmente um caso especial de uma matriz, essa definição se estende à multiplicação do vetor de matriz.</span><span class="sxs-lookup"><span data-stu-id="213f7-238">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$. Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="213f7-239">Todas as matrizes que consideramos serão matrizes quadradas, em que o número de linhas e colunas são iguais, ou vetores, que correspondem a apenas $ uma $ coluna.</span><span class="sxs-lookup"><span data-stu-id="213f7-239">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="213f7-240">Uma matriz quadrada especial é a [*matriz de identidade*](https://en.wikipedia.org/wiki/Identity_matrix), denotada $ \boldone $ , que tem todos os elementos diagonais iguais a $ 1 $ e os elementos restantes iguais a $ 0 $ :</span><span class="sxs-lookup"><span data-stu-id="213f7-240">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

$$\boldone=\begin{bmatrix}
<span data-ttu-id="213f7-241">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-241">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="213f7-242">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-242">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="213f7-243">~~ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-243">~~ \ddots\\\\</span></span>
<span data-ttu-id="213f7-244">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$</span><span class="sxs-lookup"><span data-stu-id="213f7-244">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="213f7-245">Para uma matriz quadrada $ $ , dizemos que uma matriz $ B $ é seu [*inverso*](https://en.wikipedia.org/wiki/Invertible_matrix) se a $ = BA = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-245">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="213f7-246">O inverso de uma matriz não precisa existir, mas quando ela existe, ela é exclusiva e denotamos $ um ^ { -1 } $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-246">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="213f7-247">Para qualquer matriz $ m $ , a transpoção adjacente ou conjugada de $ M $ é uma matriz $ N $ , de modo que $ N_ { IJ } = M_ { ji } ^ \* $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-247">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="213f7-248">O adjoin of $ m $ é geralmente indicado $ m ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-248">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="213f7-249">Dizemos que uma matriz $ U $ é [*unitário*](https://en.wikipedia.org/wiki/Unitary_matrix) se $ uu ^ \dagger = u ^ \dagger u = \boldone $ ou equivalente, $ u ^ { -1 } = U ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-249">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="213f7-250">Talvez a propriedade mais importante das matrizes de unitários seja que elas preservam a norma de um vetor.</span><span class="sxs-lookup"><span data-stu-id="213f7-250">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="213f7-251">Isso acontece porque</span><span class="sxs-lookup"><span data-stu-id="213f7-251">This happens because</span></span> 

<span data-ttu-id="213f7-252">$$\langlev, v \rangle = v ^ v v ^ u ^-1 U v v ^ u ^ u v s v \dagger = \dagger { } = \dagger \dagger = \langle , u v \rangle .$$</span><span class="sxs-lookup"><span data-stu-id="213f7-252">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="213f7-253">Uma matriz $ M $ é considerada [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) se m $ = m ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="213f7-253">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="213f7-254">Por fim, o [*produto tensor*](https://en.wikipedia.org/wiki/Tensor_product) (ou o produto Kronecker) de duas matrizes $ $ de tamanho $ m \times n $ e $ n $ de tamanho $ p \times q $ é uma matriz maior $ p = m \otimes n $ de tamanho $ MP \times NQ $ e é obtido de $ M $ e n da $ $ seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="213f7-254">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

\begin{align}
    <span data-ttu-id="213f7-255">M \otimes N&=</span><span class="sxs-lookup"><span data-stu-id="213f7-255">M \otimes N &=</span></span>
    \begin{bmatrix}
        <span data-ttu-id="213f7-256">M_ { 11 } ~~ \cdots ~~ M_ { 1N }\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-256">M_{11} ~~ \cdots ~~ M_{1n} \\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="213f7-257">M_ { M1 } ~~ \cdots ~~ M_ { MN  }</span><span class="sxs-lookup"><span data-stu-id="213f7-257">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        <span data-ttu-id="213f7-258">N_ { 11 } ~~ \cdots ~~ N_ { 1Q  }\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-258">N_{11}  ~~ \cdots ~~ N_{1q}\\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="213f7-259">N_ { P1 } ~~ \cdots ~~ N_ { pq}</span><span class="sxs-lookup"><span data-stu-id="213f7-259">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        <span data-ttu-id="213f7-260">M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~</span><span class="sxs-lookup"><span data-stu-id="213f7-260">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~</span></span> 
        <span data-ttu-id="213f7-261">M_ { 1N } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-261">M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="213f7-262">M_ { M1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~</span><span class="sxs-lookup"><span data-stu-id="213f7-262">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~</span></span> 
        <span data-ttu-id="213f7-263">M_ { Mn } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-263">M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="213f7-264">\end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="213f7-264">\end{bmatrix}.</span></span>
\end{align}

<span data-ttu-id="213f7-265">Isso é melhor demonstrado com alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="213f7-265">This is better demonstrated with some examples:</span></span>

$$
    \begin{bmatrix}
        <span data-ttu-id="213f7-266">a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}=</span><span class="sxs-lookup"><span data-stu-id="213f7-266">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} =</span></span>
    \begin{bmatrix}
        <span data-ttu-id="213f7-267">a \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-267">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="213f7-268">\\\\[1,5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-268">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    \end{bmatrix}
    <span data-ttu-id="213f7-269">=r a \begin{bmatrix} \\\\ d \\\\ a e \\\\ b c \\\\ b d \\\\\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-269">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="213f7-270">e</span><span class="sxs-lookup"><span data-stu-id="213f7-270">and</span></span>

$$
    \begin{bmatrix}
        <span data-ttu-id="213f7-271">a \ b \\\\ c \ d\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-271">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    \otimes 
    \begin{bmatrix}
        <span data-ttu-id="213f7-272">e \ f \\\\ g \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-272">e\ f\\\\g\ h \end{bmatrix}</span></span>
     =
    \begin{bmatrix}
    <span data-ttu-id="213f7-273">um\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-273">a\begin{bmatrix}</span></span>
    <span data-ttu-id="213f7-274">e \ f \\\\ g \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-274">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="213f7-275">b\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-275">b\begin{bmatrix}</span></span>
    <span data-ttu-id="213f7-276">e \ f \\\\ g \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-276">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="213f7-277">\\\\[1em] c\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-277">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="213f7-278">e \ f \\\\ g \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-278">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="213f7-279">3D\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-279">d\begin{bmatrix}</span></span>
    <span data-ttu-id="213f7-280">e \ f \\\\ g \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="213f7-280">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    \end{bmatrix}
    =
    \begin{bmatrix}
    <span data-ttu-id="213f7-281">AE \ AF \ ser \ BF\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-281">ae\ af\ be\ bf \\\\</span></span>
    <span data-ttu-id="213f7-282">AG \ Ah \ BG \ BH\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-282">ag\ ah\ bg\ bh \\\\</span></span>
    <span data-ttu-id="213f7-283">CE \ CF \ de \ DF\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-283">ce\ cf\ de\ df \\\\</span></span>
    <span data-ttu-id="213f7-284">CG \ ch \ DG \ DH \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="213f7-284">cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="213f7-285">Uma Convenção de notação útil final ao redor dos produtos tensor é que, para qualquer vetor $ $ ou matriz $ M $ , $ v ^ { \otimes n } $ ou $ m ^ { \otimes n } $ é curto para $ um $ produto tensor repetido n-fold.</span><span class="sxs-lookup"><span data-stu-id="213f7-285">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="213f7-286">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="213f7-286">For example:</span></span>

\begin{align}
<span data-ttu-id="213f7-287">&\begin{bmatrix}1 \\\\ 0 1 \end{bmatrix} ^ { \otimes } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ -1 \\\\ -1 \\\\ 1 \end{bmatrix} ,\\\\</span><span class="sxs-lookup"><span data-stu-id="213f7-287">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\</span></span>
  <span data-ttu-id="213f7-288">&\begin{bmatrix}0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} , \qquad \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 1 & 0 & & \end{bmatrix} 0 0.</span><span class="sxs-lookup"><span data-stu-id="213f7-288">&\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}  0& 1 \\\\ 1& 0    \end{bmatrix},    \qquad\begin{bmatrix}   0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
\end{align}
