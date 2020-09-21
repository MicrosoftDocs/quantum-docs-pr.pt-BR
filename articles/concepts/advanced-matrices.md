---
<span data-ttu-id="fd713-101">Título: conceitos de matriz avançada Descrição: Saiba mais sobre os exponenciais eigenvectors, eigenvalues e Matrix, as ferramentas fundamentais usadas para descrever e simular os algoritmos Quantum.</span><span class="sxs-lookup"><span data-stu-id="fd713-101">title: Advanced matrix concepts description: Learn about eigenvectors, eigenvalues, and matrix exponentials, the fundamental tools used to describe and simulate quantum algorithms.</span></span>
<span data-ttu-id="fd713-102">Autor: QuantumWriter UID: Microsoft. Quantum. Concepts. Matrix-avançado MS. Author: v-benbra MS. Data: 12/11/2017 MS. Topic: artigo no-loc:</span><span class="sxs-lookup"><span data-stu-id="fd713-102">author: QuantumWriter uid: microsoft.quantum.concepts.matrix-advanced ms.author: v-benbra ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="fd713-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="fd713-103">"Q#"</span></span>
- <span data-ttu-id="fd713-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="fd713-104">"$$v"</span></span>
- <span data-ttu-id="fd713-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="fd713-105">"$$"</span></span>
- <span data-ttu-id="fd713-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="fd713-106">"$$"</span></span>
- <span data-ttu-id="fd713-107">"$"</span><span class="sxs-lookup"><span data-stu-id="fd713-107">"$"</span></span>
- <span data-ttu-id="fd713-108">"$"</span><span class="sxs-lookup"><span data-stu-id="fd713-108">"$"</span></span>
- <span data-ttu-id="fd713-109">"$"</span><span class="sxs-lookup"><span data-stu-id="fd713-109">"$"</span></span>
- <span data-ttu-id="fd713-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="fd713-110">"$$"</span></span>
- <span data-ttu-id="fd713-111">"$$$"</span><span class="sxs-lookup"><span data-stu-id="fd713-111">"$$$"</span></span>
- <span data-ttu-id="fd713-112">"$$$"</span><span class="sxs-lookup"><span data-stu-id="fd713-112">"$$$"</span></span>
- <span data-ttu-id="fd713-113">"$$$"</span><span class="sxs-lookup"><span data-stu-id="fd713-113">"$$$"</span></span>
- <span data-ttu-id="fd713-114">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="fd713-114">"\cdots"</span></span>
- <span data-ttu-id="fd713-115">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="fd713-115">"bmatrix"</span></span>
- <span data-ttu-id="fd713-116">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="fd713-116">"\ddots"</span></span>
- <span data-ttu-id="fd713-117">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="fd713-117">"\equiv"</span></span>
- <span data-ttu-id="fd713-118">"\sum"</span><span class="sxs-lookup"><span data-stu-id="fd713-118">"\sum"</span></span>
- <span data-ttu-id="fd713-119">"\begin"</span><span class="sxs-lookup"><span data-stu-id="fd713-119">"\begin"</span></span>
- <span data-ttu-id="fd713-120">"\end"</span><span class="sxs-lookup"><span data-stu-id="fd713-120">"\end"</span></span>
- <span data-ttu-id="fd713-121">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="fd713-121">"\sqrt"</span></span>
- <span data-ttu-id="fd713-122">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="fd713-122">"\otimes"</span></span>
- <span data-ttu-id="fd713-123">"{"</span><span class="sxs-lookup"><span data-stu-id="fd713-123">"{"</span></span>
- <span data-ttu-id="fd713-124">"}"</span><span class="sxs-lookup"><span data-stu-id="fd713-124">"}"</span></span>
- <span data-ttu-id="fd713-125">"\text"</span><span class="sxs-lookup"><span data-stu-id="fd713-125">"\text"</span></span>
- <span data-ttu-id="fd713-126">"\phi"</span><span class="sxs-lookup"><span data-stu-id="fd713-126">"\phi"</span></span>
- <span data-ttu-id="fd713-127">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="fd713-127">"\kappa"</span></span>
- <span data-ttu-id="fd713-128">"\psi"</span><span class="sxs-lookup"><span data-stu-id="fd713-128">"\psi"</span></span>
- <span data-ttu-id="fd713-129">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="fd713-129">"\alpha"</span></span>
- <span data-ttu-id="fd713-130">"\beta"</span><span class="sxs-lookup"><span data-stu-id="fd713-130">"\beta"</span></span>
- <span data-ttu-id="fd713-131">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="fd713-131">"\gamma"</span></span>
- <span data-ttu-id="fd713-132">"\delta"</span><span class="sxs-lookup"><span data-stu-id="fd713-132">"\delta"</span></span>
- <span data-ttu-id="fd713-133">"\omega"</span><span class="sxs-lookup"><span data-stu-id="fd713-133">"\omega"</span></span>
- <span data-ttu-id="fd713-134">"\bra"</span><span class="sxs-lookup"><span data-stu-id="fd713-134">"\bra"</span></span>
- <span data-ttu-id="fd713-135">"\ket"</span><span class="sxs-lookup"><span data-stu-id="fd713-135">"\ket"</span></span>
- <span data-ttu-id="fd713-136">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="fd713-136">"\boldone"</span></span>
- <span data-ttu-id="fd713-137">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="fd713-137">"\\\\"</span></span>
- <span data-ttu-id="fd713-138">"\\"</span><span class="sxs-lookup"><span data-stu-id="fd713-138">"\\"</span></span>
- <span data-ttu-id="fd713-139">"="</span><span class="sxs-lookup"><span data-stu-id="fd713-139">"="</span></span>
- <span data-ttu-id="fd713-140">"\frac"</span><span class="sxs-lookup"><span data-stu-id="fd713-140">"\frac"</span></span>
- <span data-ttu-id="fd713-141">"\text"</span><span class="sxs-lookup"><span data-stu-id="fd713-141">"\text"</span></span>
- <span data-ttu-id="fd713-142">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="fd713-142">"\mapsto"</span></span>
- <span data-ttu-id="fd713-143">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="fd713-143">"\dagger"</span></span>
- <span data-ttu-id="fd713-144">"\to"</span><span class="sxs-lookup"><span data-stu-id="fd713-144">"\to"</span></span>
- <span data-ttu-id="fd713-145">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="fd713-145">"\begin{cases}"</span></span>
- <span data-ttu-id="fd713-146">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="fd713-146">"\end{cases}"</span></span>
- <span data-ttu-id="fd713-147">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="fd713-147">"\operatorname"</span></span>
- <span data-ttu-id="fd713-148">"\braket"</span><span class="sxs-lookup"><span data-stu-id="fd713-148">"\braket"</span></span>
- <span data-ttu-id="fd713-149">"\id"</span><span class="sxs-lookup"><span data-stu-id="fd713-149">"\id"</span></span>
- <span data-ttu-id="fd713-150">"\expect"</span><span class="sxs-lookup"><span data-stu-id="fd713-150">"\expect"</span></span>
- <span data-ttu-id="fd713-151">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="fd713-151">"\defeq"</span></span>
- <span data-ttu-id="fd713-152">"\variance"</span><span class="sxs-lookup"><span data-stu-id="fd713-152">"\variance"</span></span>
- <span data-ttu-id="fd713-153">"\dd"</span><span class="sxs-lookup"><span data-stu-id="fd713-153">"\dd"</span></span>
- <span data-ttu-id="fd713-154">"&"</span><span class="sxs-lookup"><span data-stu-id="fd713-154">"&"</span></span>
- <span data-ttu-id="fd713-155">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="fd713-155">"\begin{align}"</span></span>
- <span data-ttu-id="fd713-156">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="fd713-156">"\end{align}"</span></span>
- <span data-ttu-id="fd713-157">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="fd713-157">"\Lambda"</span></span>
- <span data-ttu-id="fd713-158">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="fd713-158">"\lambda"</span></span>
- <span data-ttu-id="fd713-159">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="fd713-159">"\Omega"</span></span>
- <span data-ttu-id="fd713-160">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="fd713-160">"\mathrm"</span></span>
- <span data-ttu-id="fd713-161">"\left"</span><span class="sxs-lookup"><span data-stu-id="fd713-161">"\left"</span></span>
- <span data-ttu-id="fd713-162">"\right"</span><span class="sxs-lookup"><span data-stu-id="fd713-162">"\right"</span></span>
- <span data-ttu-id="fd713-163">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="fd713-163">"\qquad"</span></span>
- <span data-ttu-id="fd713-164">"\times"</span><span class="sxs-lookup"><span data-stu-id="fd713-164">"\times"</span></span>
- <span data-ttu-id="fd713-165">"\big"</span><span class="sxs-lookup"><span data-stu-id="fd713-165">"\big"</span></span>
- <span data-ttu-id="fd713-166">"\langle"</span><span class="sxs-lookup"><span data-stu-id="fd713-166">"\langle"</span></span>
- <span data-ttu-id="fd713-167">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="fd713-167">"\rangle"</span></span>
- <span data-ttu-id="fd713-168">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="fd713-168">"\bigg"</span></span>
- <span data-ttu-id="fd713-169">"\Big"</span><span class="sxs-lookup"><span data-stu-id="fd713-169">"\Big"</span></span>
- <span data-ttu-id="fd713-170">"|"</span><span class="sxs-lookup"><span data-stu-id="fd713-170">"|"</span></span>
- <span data-ttu-id="fd713-171">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="fd713-171">"\mathbb"</span></span>
- <span data-ttu-id="fd713-172">"\vec"</span><span class="sxs-lookup"><span data-stu-id="fd713-172">"\vec"</span></span>
- <span data-ttu-id="fd713-173">"\in"</span><span class="sxs-lookup"><span data-stu-id="fd713-173">"\in"</span></span>
- <span data-ttu-id="fd713-174">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="fd713-174">"\texttt"</span></span>
- <span data-ttu-id="fd713-175">"\ne"</span><span class="sxs-lookup"><span data-stu-id="fd713-175">"\ne"</span></span>
- <span data-ttu-id="fd713-176">"<"</span><span class="sxs-lookup"><span data-stu-id="fd713-176">"<"</span></span>
- <span data-ttu-id="fd713-177">">"</span><span class="sxs-lookup"><span data-stu-id="fd713-177">">"</span></span>
- <span data-ttu-id="fd713-178">"\leq"</span><span class="sxs-lookup"><span data-stu-id="fd713-178">"\leq"</span></span>
- <span data-ttu-id="fd713-179">"\geq"</span><span class="sxs-lookup"><span data-stu-id="fd713-179">"\geq"</span></span>
- <span data-ttu-id="fd713-180">"~~"</span><span class="sxs-lookup"><span data-stu-id="fd713-180">"~~"</span></span>
- <span data-ttu-id="fd713-181">"~"</span><span class="sxs-lookup"><span data-stu-id="fd713-181">"~"</span></span>
- <span data-ttu-id="fd713-182">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="fd713-182">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="fd713-183">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="fd713-183">"\end{bmatrix}"</span></span>
- <span data-ttu-id="fd713-184">"\_"</span><span class="sxs-lookup"><span data-stu-id="fd713-184">"\_"</span></span>

---
# <a name="advanced-matrix-concepts"></a><span data-ttu-id="fd713-185">Conceitos de matriz avançada</span><span class="sxs-lookup"><span data-stu-id="fd713-185">Advanced Matrix Concepts</span></span> #

<span data-ttu-id="fd713-186">Agora, estendemos nossa manipulação de matrizes para [*eigenvalues, eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) e [*exponencials*](https://en.wikipedia.org/wiki/Matrix_exponential) que formam um conjunto fundamental de ferramentas que precisamos para descrever e implementar os algoritmos Quantum.</span><span class="sxs-lookup"><span data-stu-id="fd713-186">We now extend our manipulation of Matrices to [*Eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) and [*Exponentials*](https://en.wikipedia.org/wiki/Matrix_exponential) which form a fundamental set of tools we need to describe and implement quantum algorithms.</span></span>

## <a name="eigenvalues-and-eigenvectors"></a><span data-ttu-id="fd713-187">Eigenvalues e eigenvectors</span><span class="sxs-lookup"><span data-stu-id="fd713-187">Eigenvalues and Eigenvectors</span></span> ##

<span data-ttu-id="fd713-188">Deixe que $ M $ seja uma matriz quadrada e $ v $ seja um vetor que não seja o vetor de todos os zeros (ou seja, o vetor com todas as entradas iguais a $ 0 $ ).</span><span class="sxs-lookup"><span data-stu-id="fd713-188">Let $M$ be a square matrix and $v$ be a vector that is not the all zeros vector (i.e., the vector with all entries equal to $0$).</span></span>

<span data-ttu-id="fd713-189">Dizemos que $ v $ é um [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) de  $ M se o $ $ MV = vc $ de algum número $ c $ .</span><span class="sxs-lookup"><span data-stu-id="fd713-189">We say $v$ is an [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of  $M$ if $Mv = cv$ for some number $c$.</span></span> <span data-ttu-id="fd713-190">Dizemos que $ c $ é o [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) correspondente ao eigenvector $ v $ .</span><span class="sxs-lookup"><span data-stu-id="fd713-190">We say $c$ is the [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) corresponding to the eigenvector $v$.</span></span> <span data-ttu-id="fd713-191">Em geral, uma matriz $ M $ pode transformar um vetor em qualquer outro vetor, mas um eigenvector é especial porque permanece inalterado, exceto por ser multiplicado por um número.</span><span class="sxs-lookup"><span data-stu-id="fd713-191">In general a matrix $M$ may transform a vector into any other vector, but an eigenvector is special because it is left unchanged except for being multiplied by a number.</span></span> <span data-ttu-id="fd713-192">Observe que se $ v $ for um eigenvector com eigenvalue $ c $ , $ o AV $ também será um eigenvector (para qualquer outro diferente de zero $ $ ) com o mesmo eigenvalue.</span><span class="sxs-lookup"><span data-stu-id="fd713-192">Note that if $v$ is an eigenvector with eigenvalue $c$, then $av$ is also an eigenvector (for any nonzero $a$) with the same eigenvalue.</span></span>

<span data-ttu-id="fd713-193">Por exemplo, para a matriz de identidade, cada vetor $ v $ é um eigenvector com eigenvalue $ 1 $ .</span><span class="sxs-lookup"><span data-stu-id="fd713-193">For example, for the identity matrix, every vector $v$ is an eigenvector with eigenvalue $1$.</span></span>

<span data-ttu-id="fd713-194">Como outro exemplo, considere uma [*matriz diagonal*](https://en.wikipedia.org/wiki/Diagonal_matrix) $ D $ que tem apenas entradas diferentes de zero na diagonal:</span><span class="sxs-lookup"><span data-stu-id="fd713-194">As another example, consider a [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D$ which only has nonzero entries on the diagonal:</span></span>

$$
\begin{bmatrix}
<span data-ttu-id="fd713-195">d_1 & 0 0 0 & \\\\ & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="fd713-195">d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="fd713-196">Os vetores</span><span class="sxs-lookup"><span data-stu-id="fd713-196">The vectors</span></span>

<span data-ttu-id="fd713-197">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \end{bmatrix} e \begin{bmatrix} 0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="fd713-197">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0\end{bmatrix} and \begin{bmatrix}0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span></span>

<span data-ttu-id="fd713-198">são eigenvectors dessa matriz com eigenvalues  $ d_1 $ , $ d_2 $ e $ d_3 $ , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fd713-198">are eigenvectors of this matrix with eigenvalues  $d_1$, $d_2$, and $d_3$, respectively.</span></span> <span data-ttu-id="fd713-199">Se $ d_1 $ , $ d_2 $ e $ d_3 $ forem números distintos, esses vetores (e seus múltiplos) serão os únicos eigenvectors da matriz $ d $ . Em geral, para uma matriz diagonal, é fácil ler eigenvalues e eigenvectors.</span><span class="sxs-lookup"><span data-stu-id="fd713-199">If $d_1$, $d_2$, and $d_3$ are distinct numbers, then these vectors (and their multiples) are the only eigenvectors of the matrix $D$. In general, for a diagonal matrix it is easy to read off the eigenvalues and eigenvectors.</span></span> <span data-ttu-id="fd713-200">Eigenvalues são todos os números que aparecem na diagonal e seus respectivos eigenvectors são os vetores de unidade com uma entrada igual a $ 1 $ e as entradas restantes iguais a $ 0 $ .</span><span class="sxs-lookup"><span data-stu-id="fd713-200">The eigenvalues are all the numbers appearing on the diagonal, and their respective eigenvectors are the unit vectors with one entry equal to $1$ and the remaining entries equal to $0$.</span></span>

<span data-ttu-id="fd713-201">Observe no exemplo acima que a eigenvectors de $ D $ formam uma base para $ $ vetores tridimensionais.</span><span class="sxs-lookup"><span data-stu-id="fd713-201">Note in the above example that the eigenvectors of $D$ form a basis for $3$-dimensional vectors.</span></span> <span data-ttu-id="fd713-202">Uma base é um conjunto de vetores, de modo que qualquer vetor pode ser escrito como uma combinação linear deles.</span><span class="sxs-lookup"><span data-stu-id="fd713-202">A basis is a set of vectors such that any vector can be written as a linear combination of them.</span></span> <span data-ttu-id="fd713-203">Mais explicitamente, $ v_1 $ , $ v_2 $ e $ v_3 $ formam uma base se qualquer tipo $ de vetor v $ puder ser escrito como $ v = a_1 v_1 + a_2 v_2 + a_3 v_3 $ para alguns números $ a_1 $ , $ a_2 $ e $ a_3 $ .</span><span class="sxs-lookup"><span data-stu-id="fd713-203">More explicitly, $v_1$, $v_2$, and $v_3$ form a basis if any vector $v$ can be written as $v=a_1 v_1 + a_2 v_2 + a_3 v_3$ for some numbers $a_1$, $a_2$, and $a_3$.</span></span>

<span data-ttu-id="fd713-204">Lembre-se de que uma matriz Hermitian (também chamada de auto-adjacente) é uma matriz quadrada complexa igual à sua própria transpoção conjugada complexa, enquanto uma matriz unitário é uma matriz quadrada complexa cujo inverso é igual à sua Transpose de conjugado ou complexa.</span><span class="sxs-lookup"><span data-stu-id="fd713-204">Recall that a Hermitian matrix (also called self-adjoint) is a complex square matrix equal to its own complex conjugate transpose, while a unitary matrix is a complex square matrix whose inverse is equal to its adjoint or complex conjugate transpose.</span></span>
<span data-ttu-id="fd713-205">Para matrizes Hermitian e unitários, que são essencialmente as únicas matrizes encontradas na computação Quantum, há um resultado geral conhecido como [*Spectral teorema*](https://en.wikipedia.org/wiki/Spectral_theorem), que declara o seguinte: para qualquer matriz Hermitian ou unitário $ $ 2, existe um U unitário $ $ como $ m = u ^ \dagger D u $ para alguma matriz diagonal $ d $ . Além disso, as entradas diagonais de $ D $ serão o eigenvalues de $ M $ .</span><span class="sxs-lookup"><span data-stu-id="fd713-205">For Hermitian and unitary matrices, which are essentially the only matrices encountered in quantum computing, there is a general result known as the [*spectral theorem*](https://en.wikipedia.org/wiki/Spectral_theorem), which asserts the following: For any Hermitian or unitary matrix $M$, there exists a unitary $U$ such that $M=U^\dagger D U$ for some diagonal matrix $D$. Furthermore, the diagonal entries of $D$ will be the eigenvalues of $M$.</span></span>

<span data-ttu-id="fd713-206">Já sabemos como calcular o eigenvalues e o eigenvectors de uma matriz diagonal $ D $ . Usando este teorema, sabemos que, se $ v $ for um eigenvector de $ D $ com eigenvalue $ c $ , ou seja, $ o DV = CV $ , $ U ^ \dagger v $ será um eigenvector de $ M $ com eigenvalue $ c $ .</span><span class="sxs-lookup"><span data-stu-id="fd713-206">We already know how to compute the eigenvalues and eigenvectors of a diagonal matrix $D$. Using this theorem we know that if $v$ is an eigenvector of $D$ with eigenvalue $c$, i.e., $Dv = cv$, then $U^\dagger v$ will be an eigenvector of $M$ with eigenvalue $c$.</span></span> <span data-ttu-id="fd713-207">Isso ocorre porque</span><span class="sxs-lookup"><span data-stu-id="fd713-207">This is because</span></span>

<span data-ttu-id="fd713-208">$$M (U ^ \dagger v) = u ^ \dagger d u (u ^ \dagger v) = U ^ \dagger d (u u ^ \dagger ) v = u ^ \dagger D v = c u ^ \dagger v.$$</span><span class="sxs-lookup"><span data-stu-id="fd713-208">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span></span>

## <a name="matrix-exponentials"></a><span data-ttu-id="fd713-209">Exponenciais de matriz</span><span class="sxs-lookup"><span data-stu-id="fd713-209">Matrix Exponentials</span></span>
<span data-ttu-id="fd713-210">Um [*exponencial de matriz*](https://en.wikipedia.org/wiki/Matrix_exponential) também pode ser definido de acordo com a analogia exata com a função exponencial.</span><span class="sxs-lookup"><span data-stu-id="fd713-210">A [*matrix exponential*](https://en.wikipedia.org/wiki/Matrix_exponential) can also be defined in exact analogy to the exponential function.</span></span>  <span data-ttu-id="fd713-211">O exponencial de matriz de uma matriz $ a $ pode ser expresso como</span><span class="sxs-lookup"><span data-stu-id="fd713-211">The matrix exponential of a matrix $A$ can be expressed as</span></span>

$$
<span data-ttu-id="fd713-212">e ^ A = \boldone + a + \frac { a ^ 2 } { 2! } + \frac { Um ^ 3 3 } { !}+\cdots</span><span class="sxs-lookup"><span data-stu-id="fd713-212">e^A=\boldone + A + \frac{A^2}{2!}+\frac{A^3}{3!}+\cdots</span></span>
$$

<span data-ttu-id="fd713-213">Isso é importante porque a evolução do tempo mecânico da Quantum é descrita por uma matriz unitário do formato $ e ^ { IB } $ para a matriz Hermitian $ B $ .  Por esse motivo, a execução de exponencials de matriz é uma parte fundamental da computação Quantum e, como tal, Q# oferece rotinas intrínsecas para descrever essas operações.</span><span class="sxs-lookup"><span data-stu-id="fd713-213">This is important because quantum mechanical time evolution is described by a unitary matrix of the form $e^{iB}$ for Hermitian matrix $B$.  For this reason, performing matrix exponentials is a fundamental part of quantum computing and as such Q# offers intrinsic routines for describing these operations.</span></span>
<span data-ttu-id="fd713-214">Há muitas maneiras de fazer a computação de um exponencial de matriz em um computador clássico e, em geral, o aproximar de forma numérica como tal exponencial é muito perigoso com Peril.</span><span class="sxs-lookup"><span data-stu-id="fd713-214">There are many ways in practice to compute a matrix exponential on a classical computer, and in general numerically approximating such an exponential is fraught with peril.</span></span>  <span data-ttu-id="fd713-215">Confira [*Cleve Moler e Charles Van empréstimo. "Dezenove duvidosa maneiras de computar o exponencial de uma matriz". SIAM revisar 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) para obter mais informações sobre os desafios envolvidos.</span><span class="sxs-lookup"><span data-stu-id="fd713-215">See [*Cleve Moler and Charles Van Loan. "Nineteen dubious ways to compute the exponential of a matrix." SIAM review 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) for more information about the challenges involved.</span></span>

<span data-ttu-id="fd713-216">A maneira mais fácil de entender como computar o exponencial de uma matriz é por meio de eigenvalues e eigenvectors dessa matriz.</span><span class="sxs-lookup"><span data-stu-id="fd713-216">The easiest way to understand how to compute the exponential of a matrix is through the eigenvalues and eigenvectors of that matrix.</span></span>  <span data-ttu-id="fd713-217">Especificamente, o Spectral teorema discutido acima diz que para cada matriz Hermitian ou unitário $ a $ existe uma matriz unitário $ u $ e uma matriz diagonal $ d, de $ modo que u $ = ^ \dagger d u $ .  Devido às propriedades de unitarity, temos esse $ ^ 2 = u ^ \dagger d ^ 2 u $ e, da mesma forma, para qualquer Power $ p $ $ A ^ p = u ^ \dagger d ^ p u $ .  Se substituímos isso na definição de operador do exponencial de operador, obtemos:</span><span class="sxs-lookup"><span data-stu-id="fd713-217">Specifically, the spectral theorem discussed above says that for every Hermitian or unitary matrix $A$ there exists a unitary matrix $U$ and a diagonal matrix $D$ such that $A=U^\dagger D U$.  Because of the properties of unitarity we have that $A^2 = U^\dagger D^2 U$ and similarly for any power $p$ $A^p = U^\dagger D^p U$.  If we substitute this into the operator definition of the operator exponential we obtain:</span></span>

$$
<span data-ttu-id="fd713-218">e ^ A = U ^ \dagger \left ( \boldone + d + \frac { d ^ 2 } { 2! } + \cdots \right ) U = u ^ \dagger \begin{bmatrix} \exp (D_ { 11 } ) & 0 & \cdots & 0 \\\\ 0 & \exp (D_ { 22 } ) & \cdots & 0 \\\\ \vdots & \vdots & \ddots & \vdots \\\\ 0 & 0 & \cdots & \exp (D_ { NN } ) \end{bmatrix} U.$$</span><span class="sxs-lookup"><span data-stu-id="fd713-218">e^A= U^\dagger \left(\boldone +D +\frac{D^2}{2!}+\cdots \right)U= U^\dagger \begin{bmatrix}\exp(D_{11}) & 0 &\cdots &0\\\\ 0 & \exp(D_{22})&\cdots& 0\\\\ \vdots &\vdots &\ddots &\vdots\\\\ 0&0&\cdots&\exp(D_{NN}) \end{bmatrix} U. $$</span></span>

<span data-ttu-id="fd713-219">Em outras palavras, se você transformar para o eigenbasis da matriz $ a $ , a computação do exponencial de matriz será equivalente a computar o exponencial comum do eigenvalues da matriz.</span><span class="sxs-lookup"><span data-stu-id="fd713-219">In other words, if you transform to the eigenbasis of the matrix $A$ then computing the matrix exponential is equivalent to computing the ordinary exponential of the eigenvalues of the matrix.</span></span>  <span data-ttu-id="fd713-220">Como muitas operações na computação Quantum envolvem a execução de exponenciais de matriz, esse truque de transformar em eigenbasis de uma matriz para simplificar a execução do operador exponencial é exibido com frequência e é a base por trás de muitos algoritmos Quantum, como os métodos de simulação de Quantum Trotter – Suzuki-Style discutidos posteriormente neste guia.</span><span class="sxs-lookup"><span data-stu-id="fd713-220">As many operations in quantum computing involve performing matrix exponentials, this trick of transforming into the eigenbasis of a matrix to simplify performing the operator exponential appears frequently and is the basis behind many quantum algorithms such as Trotter–Suzuki-style quantum simulation methods discussed later in this guide.</span></span>

<span data-ttu-id="fd713-221">Outra propriedade útil é se $ B $ for unitário e Hermitian, ou seja, $ b = b ^ { -1 } = b ^ \dagger $ e $ B ^ 2 = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="fd713-221">Another useful property is if $B$ is both unitary and Hermitian, i.e., $B=B^{-1}=B^\dagger$ then $B^2=\boldone$.</span></span> <span data-ttu-id="fd713-222">Ao aplicar essa regra à expansão acima do exponencial de matriz e agrupar os $ \boldone $ e os $ $ termos B juntos, ele pode ver que, para qualquer valor real $ x $ a identidade</span><span class="sxs-lookup"><span data-stu-id="fd713-222">By applying this rule to the above expansion of the matrix exponential and by grouping the $\boldone$ and the $B$ terms together, it can be see that for any real value $x$ the identity</span></span>

<span data-ttu-id="fd713-223">$$e ^ { iBx } = \boldone \cos (x) + iB\sin (x)$$</span><span class="sxs-lookup"><span data-stu-id="fd713-223">$$e^{iBx}=\boldone \cos(x)+ iB\sin(x)$$</span></span>


<span data-ttu-id="fd713-224">realiza.</span><span class="sxs-lookup"><span data-stu-id="fd713-224">holds.</span></span> <span data-ttu-id="fd713-225">Esse truque é especialmente útil, pois ele permite que o motivo dos exponencials de matriz de ações tenha, mesmo se a dimensão de $ B $ for exponencialmente grande, para o caso especial quando $ B $ for unitário e Hermitian.</span><span class="sxs-lookup"><span data-stu-id="fd713-225">This trick is especially useful because it allows to reason about the actions matrix exponentials have, even if the dimension of $B$ is exponentially large, for the special case when $B$ is both unitary and Hermitian.</span></span>
