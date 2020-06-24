---
title: Conceitos avançados sobre matriz
description: Saiba mais sobre os exponenciais eigenvectors, eigenvalues e Matrix, as ferramentas fundamentais usadas para descrever e simular algoritmos Quantum.
author: QuantumWriter
uid: microsoft.quantum.concepts.matrix-advanced
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
- $$
- $$
- $$
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
ms.openlocfilehash: 71923247121eae6a1d4e26d2664d8e547370ba3a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269449"
---
# <a name="advanced-matrix-concepts"></a><span data-ttu-id="9768c-103">Conceitos de matriz avançada</span><span class="sxs-lookup"><span data-stu-id="9768c-103">Advanced Matrix Concepts</span></span> #

<span data-ttu-id="9768c-104">Agora, estendemos nossa manipulação de matrizes para [*eigenvalues, eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) e [*exponencials*](https://en.wikipedia.org/wiki/Matrix_exponential) que formam um conjunto fundamental de ferramentas que precisamos para descrever e implementar os algoritmos Quantum.</span><span class="sxs-lookup"><span data-stu-id="9768c-104">We now extend our manipulation of Matrices to [*Eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) and [*Exponentials*](https://en.wikipedia.org/wiki/Matrix_exponential) which form a fundamental set of tools we need to describe and implement quantum algorithms.</span></span>

## <a name="eigenvalues-and-eigenvectors"></a><span data-ttu-id="9768c-105">Eigenvalues e eigenvectors</span><span class="sxs-lookup"><span data-stu-id="9768c-105">Eigenvalues and Eigenvectors</span></span> ##

<span data-ttu-id="9768c-106">Permita que $M $ seja uma matriz quadrada e $v $ seja um vetor que não seja o vetor de todos os zeros (ou seja, o vetor com todas as entradas iguais a $0 $ ).</span><span class="sxs-lookup"><span data-stu-id="9768c-106">Let $M$ be a square matrix and $v$ be a vector that is not the all zeros vector (i.e., the vector with all entries equal to $0$).</span></span>

<span data-ttu-id="9768c-107">Dizemos $v $ é um [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) de $M $ se $MV = CV $ por algum $c de número $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-107">We say $v$ is an [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of  $M$ if $Mv = cv$ for some number $c$.</span></span> <span data-ttu-id="9768c-108">Dizemos $c $ é o [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) correspondente ao $v de eigenvector $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-108">We say $c$ is the [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) corresponding to the eigenvector $v$.</span></span> <span data-ttu-id="9768c-109">Em geral, uma matriz $M $ pode transformar um vetor em qualquer outro vetor, mas um eigenvector é especial porque permanece inalterado, exceto por ser multiplicado por um número.</span><span class="sxs-lookup"><span data-stu-id="9768c-109">In general a matrix $M$ may transform a vector into any other vector, but an eigenvector is special because it is left unchanged except for being multiplied by a number.</span></span> <span data-ttu-id="9768c-110">Observe que, se $v $ for um eigenvector com eigenvalue $c $ , $AV $ também será um eigenvector (para qualquer $a diferente de zero $ ) com o mesmo eigenvalue.</span><span class="sxs-lookup"><span data-stu-id="9768c-110">Note that if $v$ is an eigenvector with eigenvalue $c$, then $av$ is also an eigenvector (for any nonzero $a$) with the same eigenvalue.</span></span>

<span data-ttu-id="9768c-111">Por exemplo, para a matriz de identidade, cada $v de vetor $ é um eigenvector com eigenvalue $1 $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-111">For example, for the identity matrix, every vector $v$ is an eigenvector with eigenvalue $1$.</span></span>

<span data-ttu-id="9768c-112">Como outro exemplo, considere uma [*matriz diagonal*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D $ que tem apenas entradas diferentes de zero na diagonal:</span><span class="sxs-lookup"><span data-stu-id="9768c-112">As another example, consider a [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D$ which only has nonzero entries on the diagonal:</span></span>

<span data-ttu-id="9768c-113">US $ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="9768c-113">$$ \begin{bmatrix}</span></span>
<span data-ttu-id="9768c-114">d_1 & 0 & 0 \\ \\ 0 & d_2 & 0 \\ \\ 0 & 0 & d_3 \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="9768c-114">d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="9768c-115">Os vetores</span><span class="sxs-lookup"><span data-stu-id="9768c-115">The vectors</span></span>

<span data-ttu-id="9768c-116">$ $ \begin{ bmatrix } 1 \\ \\ 0 0 \\ \\ \end{ bmatrix } , \begin{ bmatrix } 0 \\ \\ 1 \\ \\ 0 \end{bmatrix} e \begin{ bmatrix } 0 \\ \\ 0 \\ \\ 1\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="9768c-116">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0\end{bmatrix} and \begin{bmatrix}0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span></span>

<span data-ttu-id="9768c-117">são eigenvectors dessa matriz com eigenvalues $d _1 $ , $d _2 $ e $d _3 $ , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9768c-117">are eigenvectors of this matrix with eigenvalues  $d_1$, $d_2$, and $d_3$, respectively.</span></span> <span data-ttu-id="9768c-118">Se $d _1 $ , $d _2 $ e $d _3 $ forem números distintos, esses vetores (e seus múltiplos) serão os únicos eigenvectors da matriz $D $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-118">If $d_1$, $d_2$, and $d_3$ are distinct numbers, then these vectors (and their multiples) are the only eigenvectors of the matrix $D$.</span></span> <span data-ttu-id="9768c-119">Em geral, para uma matriz diagonal, é fácil ler eigenvalues e eigenvectors.</span><span class="sxs-lookup"><span data-stu-id="9768c-119">In general, for a diagonal matrix it is easy to read off the eigenvalues and eigenvectors.</span></span> <span data-ttu-id="9768c-120">Eigenvalues são todos os números que aparecem na diagonal e seus respectivos eigenvectors são os vetores de unidade com uma entrada igual a $1 $ e as entradas restantes iguais a $0 $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-120">The eigenvalues are all the numbers appearing on the diagonal, and their respective eigenvectors are the unit vectors with one entry equal to $1$ and the remaining entries equal to $0$.</span></span>

<span data-ttu-id="9768c-121">Observe no exemplo acima que o eigenvectors de $D $ formam uma base para $ vetores $3-dimensional.</span><span class="sxs-lookup"><span data-stu-id="9768c-121">Note in the above example that the eigenvectors of $D$ form a basis for $3$-dimensional vectors.</span></span> <span data-ttu-id="9768c-122">Uma base é um conjunto de vetores, de modo que qualquer vetor pode ser escrito como uma combinação linear deles.</span><span class="sxs-lookup"><span data-stu-id="9768c-122">A basis is a set of vectors such that any vector can be written as a linear combination of them.</span></span> <span data-ttu-id="9768c-123">Mais explicitamente, $v _1 $ , $v _2 $ e $v _3 $ formam uma base se qualquer $v vetorial $ puder ser escrito como $v = a_1 v_1 + a_2 v_2 + a_3 v_3 $ para alguns números $a _1 $ , $a _2 $ e $a _3 $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-123">More explicitly, $v_1$, $v_2$, and $v_3$ form a basis if any vector $v$ can be written as $v=a_1 v_1 + a_2 v_2 + a_3 v_3$ for some numbers $a_1$, $a_2$, and $a_3$.</span></span>

<span data-ttu-id="9768c-124">Lembre-se de que uma matriz Hermitian (também chamada de auto-adjacente) é uma matriz quadrada complexa igual à sua própria conjugada complexa, enquanto uma matriz unitário é uma matriz quadrada complexa cujo inverso é igual ao seu conjugado complexo.</span><span class="sxs-lookup"><span data-stu-id="9768c-124">Recall that a Hermitian matrix (also called self-adjoint) is a complex square matrix equal to its own complex conjugate, while a unitary matrix is a complex square matrix whose inverse is equal to its complex conjugate.</span></span>
<span data-ttu-id="9768c-125">Para matrizes Hermitian e unitários, que são essencialmente as únicas matrizes encontradas na computação Quantum, há um resultado geral conhecido como [*Spectral teorema*](https://en.wikipedia.org/wiki/Spectral_theorem), que declara o seguinte: para qualquer matriz Hermitian ou unitário $M $ , existe um $U unitário de $ tal forma que $M = U ^ \dagger D U $ para algum $D de matriz diagonal $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-125">For Hermitian and unitary matrices, which are essentially the only matrices encountered in quantum computing, there is a general result known as the [*spectral theorem*](https://en.wikipedia.org/wiki/Spectral_theorem), which asserts the following: For any Hermitian or unitary matrix $M$, there exists a unitary $U$ such that $M=U^\dagger D U$ for some diagonal matrix $D$.</span></span> <span data-ttu-id="9768c-126">Além disso, as entradas diagonais de $D $ serão a eigenvalues de $M $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-126">Furthermore, the diagonal entries of $D$ will be the eigenvalues of $M$.</span></span>

<span data-ttu-id="9768c-127">Já sabemos como calcular o eigenvalues e o eigenvectors de uma matriz diagonal $D $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-127">We already know how to compute the eigenvalues and eigenvectors of a diagonal matrix $D$.</span></span> <span data-ttu-id="9768c-128">Usando este teorema, sabemos que, se $v $ for um eigenvector de $D $ com eigenvalue $c $ , ou seja, $DV = CV $ , $U ^ \dagger v $ será um eigenvector de $M $ com eigenvalue $c $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-128">Using this theorem we know that if $v$ is an eigenvector of $D$ with eigenvalue $c$, i.e., $Dv = cv$, then $U^\dagger v$ will be an eigenvector of $M$ with eigenvalue $c$.</span></span> <span data-ttu-id="9768c-129">Isso ocorre porque</span><span class="sxs-lookup"><span data-stu-id="9768c-129">This is because</span></span>

<span data-ttu-id="9768c-130">$ $M (U ^ \dagger v) = U ^ \dagger D U (U ^ \dagger v) = U ^ \dagger D (U U ^ \dagger) v = U ^ \dagger D v = c U ^ \dagger v. $ $</span><span class="sxs-lookup"><span data-stu-id="9768c-130">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span></span>

## <a name="matrix-exponentials"></a><span data-ttu-id="9768c-131">Exponenciais de matriz</span><span class="sxs-lookup"><span data-stu-id="9768c-131">Matrix Exponentials</span></span>
<span data-ttu-id="9768c-132">Um [*exponencial de matriz*](https://en.wikipedia.org/wiki/Matrix_exponential) também pode ser definido de acordo com a analogia exata com a função exponencial.</span><span class="sxs-lookup"><span data-stu-id="9768c-132">A [*matrix exponential*](https://en.wikipedia.org/wiki/Matrix_exponential) can also be defined in exact analogy to the exponential function.</span></span>  <span data-ttu-id="9768c-133">O exponencial de matriz de um $A de matriz $ pode ser expresso como</span><span class="sxs-lookup"><span data-stu-id="9768c-133">The matrix exponential of a matrix $A$ can be expressed as</span></span>

<span data-ttu-id="9768c-134">$ $ e ^ A = \boldone + A + \frac{A ^ 2 } {2!} + \frac{A ^ 3 } {3!} + \cdots $ $</span><span class="sxs-lookup"><span data-stu-id="9768c-134">$$ e^A=\boldone + A + \frac{A^2}{2!}+\frac{A^3}{3!}+\cdots $$</span></span>

<span data-ttu-id="9768c-135">Isso é importante porque a evolução do tempo mecânico da Quantum é descrita por uma matriz unitário do formulário $e ^ {iB } $ para a matriz Hermitian $B $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-135">This is important because quantum mechanical time evolution is described by a unitary matrix of the form $e^{iB}$ for Hermitian matrix $B$.</span></span>  <span data-ttu-id="9768c-136">Por esse motivo, a execução de exponencials de matriz é uma parte fundamental da computação Quantum e, como tal, Q # oferece rotinas intrínsecas para descrever essas operações.</span><span class="sxs-lookup"><span data-stu-id="9768c-136">For this reason, performing matrix exponentials is a fundamental part of quantum computing and as such Q# offers intrinsic routines for describing these operations.</span></span>
<span data-ttu-id="9768c-137">Há muitas maneiras de fazer a computação de um exponencial de matriz em um computador clássico e, em geral, o aproximar de forma numérica como tal exponencial é muito perigoso com Peril.</span><span class="sxs-lookup"><span data-stu-id="9768c-137">There are many ways in practice to compute a matrix exponential on a classical computer, and in general numerically approximating such an exponential is fraught with peril.</span></span>  <span data-ttu-id="9768c-138">Confira [*Cleve Moler e Charles Van empréstimo. "Dezenove duvidosa maneiras de computar o exponencial de uma matriz". SIAM revisar 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) para obter mais informações sobre os desafios envolvidos.</span><span class="sxs-lookup"><span data-stu-id="9768c-138">See [*Cleve Moler and Charles Van Loan. "Nineteen dubious ways to compute the exponential of a matrix." SIAM review 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) for more information about the challenges involved.</span></span>

<span data-ttu-id="9768c-139">A maneira mais fácil de entender como computar o exponencial de uma matriz é por meio de eigenvalues e eigenvectors dessa matriz.</span><span class="sxs-lookup"><span data-stu-id="9768c-139">The easiest way to understand how to compute the exponential of a matrix is through the eigenvalues and eigenvectors of that matrix.</span></span>  <span data-ttu-id="9768c-140">Especificamente, o Spectral teorema discutido acima diz que para cada matriz Hermitian ou unitário $A $ existe um $U de matriz unitário $ e uma matriz diagonal $D de $ forma que $A = u ^ \dagger D U $ .  Devido às propriedades de unitarity, temos isso $A ^ 2 = U ^ \dagger D ^ 2 U $ e, da mesma forma, para qualquer $p de energia $ $A ^ p = u ^ \dagger D ^ p u $ .  Se substituímos isso na definição de operador do exponencial de operador, obtemos:</span><span class="sxs-lookup"><span data-stu-id="9768c-140">Specifically, the spectral theorem discussed above says that for every Hermitian or unitary matrix $A$ there exists a unitary matrix $U$ and a diagonal matrix $D$ such that $A=U^\dagger D U$.  Because of the properties of unitarity we have that $A^2 = U^\dagger D^2 U$ and similarly for any power $p$ $A^p = U^\dagger D^p U$.  If we substitute this into the operator definition of the operator exponential we obtain:</span></span>

<span data-ttu-id="9768c-141">$ $ e ^ A = U ^ \dagger \left (\boldone + D + \frac{D ^ 2 } {2!} + \cdots \right) U = u ^ \dagger \begin{ bmatrix } \exp (D_ {11 } ) & 0 & \cdots &0 \\\\ 0 & \exp (D_ {22 } ) & \cdots & 0 \\\\ \vdots & \vdots & \ddots & \vdots \\\\ 0&0 & \cdots & \exp (D_ {NN } ) \end{ bmatrix } U. $ $</span><span class="sxs-lookup"><span data-stu-id="9768c-141">$$ e^A= U^\dagger \left(\boldone +D +\frac{D^2}{2!}+\cdots \right)U= U^\dagger \begin{bmatrix}\exp(D_{11}) & 0 &\cdots &0\\\\ 0 & \exp(D_{22})&\cdots& 0\\\\ \vdots &\vdots &\ddots &\vdots\\\\ 0&0&\cdots&\exp(D_{NN}) \end{bmatrix} U. $$</span></span>

<span data-ttu-id="9768c-142">Em outras palavras, se você transformar para o eigenbasis da matriz $A a $ computação do exponencial de matriz será equivalente a computar o exponencial comum do eigenvalues da matriz.</span><span class="sxs-lookup"><span data-stu-id="9768c-142">In other words, if you transform to the eigenbasis of the matrix $A$ then computing the matrix exponential is equivalent to computing the ordinary exponential of the eigenvalues of the matrix.</span></span>  <span data-ttu-id="9768c-143">Como muitas operações na computação Quantum envolvem a execução de exponenciais de matriz, esse truque de transformar em eigenbasis de uma matriz para simplificar a execução do operador exponencial é exibido com frequência e é a base por trás de muitos algoritmos Quantum, como os métodos de simulação de Quantum Trotter – Suzuki-Style discutidos posteriormente neste guia.</span><span class="sxs-lookup"><span data-stu-id="9768c-143">As many operations in quantum computing involve performing matrix exponentials, this trick of transforming into the eigenbasis of a matrix to simplify performing the operator exponential appears frequently and is the basis behind many quantum algorithms such as Trotter–Suzuki-style quantum simulation methods discussed later in this guide.</span></span>

<span data-ttu-id="9768c-144">Outra propriedade útil é se $B $ for unitário e Hermitian, ou seja, $B = b ^ {-1 } = b ^ \dagger $ e $B ^ 2 = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="9768c-144">Another useful property is if $B$ is both unitary and Hermitian, i.e., $B=B^{-1}=B^\dagger$ then $B^2=\boldone$.</span></span> <span data-ttu-id="9768c-145">Ao aplicar essa regra à expansão acima do exponencial de matriz e ao agrupar o $ \boldone $ e os termos de $B $ juntos, ele pode ver que, para qualquer valor real $x $ a identidade</span><span class="sxs-lookup"><span data-stu-id="9768c-145">By applying this rule to the above expansion of the matrix exponential and by grouping the $\boldone$ and the $B$ terms together, it can be see that for any real value $x$ the identity</span></span>

<span data-ttu-id="9768c-146">$ $e ^ {iBx } = \boldone \cos (x) + iB\sin (x) $ $</span><span class="sxs-lookup"><span data-stu-id="9768c-146">$$e^{iBx}=\boldone \cos(x)+ iB\sin(x)$$</span></span>


<span data-ttu-id="9768c-147">realiza.</span><span class="sxs-lookup"><span data-stu-id="9768c-147">holds.</span></span> <span data-ttu-id="9768c-148">Esse truque é especialmente útil, pois ele permite que o motivo dos exponencials de matriz de ações tenha, mesmo se a dimensão de $B $ for exponencialmente grande, para o caso especial quando $B $ for unitário e Hermitian.</span><span class="sxs-lookup"><span data-stu-id="9768c-148">This trick is especially useful because it allows to reason about the actions matrix exponentials have, even if the dimension of $B$ is exponentially large, for the special case when $B$ is both unitary and Hermitian.</span></span>
