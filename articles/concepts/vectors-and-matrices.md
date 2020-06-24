---
title: Vetores e matrizes na computação quântica
description: Aprenda as noções básicas de como trabalhar com vetores e matrizes.
author: QuantumWriter
uid: microsoft.quantum.concepts.vectors
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
ms.openlocfilehash: f9d4e14742b7d06a6e90af0902b31fbdf17aedab
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269534"
---
# <a name="vectors-and-matrices"></a><span data-ttu-id="294f5-103">Vetores e matrizes</span><span class="sxs-lookup"><span data-stu-id="294f5-103">Vectors and Matrices</span></span>

<span data-ttu-id="294f5-104">Alguma familiaridade com vetores e matrizes é essencial para entender a computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="294f5-104">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="294f5-105">Fornecemos uma breve introdução abaixo e os leitores interessados são recomendados para ler uma referência padrão em Algebra linear, como *Strang, G. (1993). Introdução à algebra linear (Vol. 3). Wellesley, MA: Wellesley-Cambridge, Press* ou uma referência online, como [Algebra linear](http://joshua.smcvt.edu/linearalgebra/).</span><span class="sxs-lookup"><span data-stu-id="294f5-105">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="294f5-106">Um vetor de coluna (ou simplesmente [*vetor*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v $ de dimensão (ou tamanho) $n $ é uma coleção de $n $ números complexos $ (v_1, v_2, \ldots, v_n) $ organizados como uma coluna:</span><span class="sxs-lookup"><span data-stu-id="294f5-106">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="294f5-107">$ $v = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-107">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="294f5-108">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-108">v_1\\\\</span></span>
<span data-ttu-id="294f5-109">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-109">v_2\\\\</span></span>
<span data-ttu-id="294f5-110">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-110">\vdots\\\\</span></span>
<span data-ttu-id="294f5-111">v_n \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="294f5-111">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="294f5-112">A norma de um $v de vetor $ é definida como $ \sqrt { \sum \_ i | v \_ i | ^ 2 } $.</span><span class="sxs-lookup"><span data-stu-id="294f5-112">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="294f5-113">Um vetor é considerado como sendo a norma da unidade (ou, como alternativa, é chamado de [*vetor de unidade*](https://en.wikipedia.org/wiki/Unit_vector)) se sua norma for $1 $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-113">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="294f5-114">O [*adjoin de um $v de vetor*](https://en.wikipedia.org/wiki/Adjoint_matrix) $ é indicado $v ^ \dagger $ e é definido para ser o seguinte vetor de linha, em que $ \* $ denota o conjugado complexo,</span><span class="sxs-lookup"><span data-stu-id="294f5-114">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="294f5-115">$ $ \begin{ bmatrix } v_1 \\ \\ \vdots \\ \\ v_n \end{ bmatrix } ^ \dagger = \begin{ bmatrix } v_1 ^ \* & \cdots & v_n ^ \* \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="294f5-115">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="294f5-116">A maneira mais comum de multiplicar dois vetores juntos é por meio do [*produto interno*](https://en.wikipedia.org/wiki/Inner_product_space), também conhecido como produto de ponto.</span><span class="sxs-lookup"><span data-stu-id="294f5-116">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="294f5-117">O produto interno fornece a projeção de um vetor para outro e é inestimável na descrição de como expressar um vetor como uma soma de outros vetores mais simples.</span><span class="sxs-lookup"><span data-stu-id="294f5-117">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="294f5-118">O produto interno entre $u $ e $v $ , denotado $ \left \langle u, v \right \rangle $ é definido como</span><span class="sxs-lookup"><span data-stu-id="294f5-118">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

<span data-ttu-id="294f5-119">$ $ \langle u, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="294f5-119">$$ \langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="294f5-120">Essa notação também permite que a norma de um vetor $v $ seja escrita como $ \sqrt { \langle v, v \rangle } $.</span><span class="sxs-lookup"><span data-stu-id="294f5-120">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="294f5-121">Podemos multiplicar um vetor com um número $c $ para formar um novo vetor cujas entradas são multiplicadas por $c $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-121">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="294f5-122">Também podemos adicionar dois vetores $u $ e $v $ para formar um novo vetor cujas entradas são a soma das entradas de $u $ e $v $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-122">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="294f5-123">Essas operações são descritas abaixo:</span><span class="sxs-lookup"><span data-stu-id="294f5-123">These operations are depicted below:</span></span>

<span data-ttu-id="294f5-124">$ $ \mathrm{If } ~ u = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-124">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="294f5-125">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-125">u_1\\\\</span></span>
<span data-ttu-id="294f5-126">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-126">u_2\\\\</span></span>
<span data-ttu-id="294f5-127">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-127">\vdots\\\\</span></span>
<span data-ttu-id="294f5-128">u_n \end{ bmatrix } ~ \mathrm{and } ~ v = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-128">u_n \end{bmatrix}~\mathrm{and}~ v =\begin{bmatrix}</span></span>
    <span data-ttu-id="294f5-129">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-129">v_1\\\\</span></span>
    <span data-ttu-id="294f5-130">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-130">v_2\\\\</span></span>
    <span data-ttu-id="294f5-131">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-131">\vdots\\\\</span></span>
    <span data-ttu-id="294f5-132">v_n \end{ bmatrix } , ~ \mathrm{then } ~ au + BV = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-132">v_n \end{bmatrix},~\mathrm{then}~ au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="294f5-133">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-133">au_1+bv_1\\\\</span></span>
<span data-ttu-id="294f5-134">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-134">au_2+bv_2\\\\</span></span>
<span data-ttu-id="294f5-135">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-135">\vdots\\\\</span></span>
<span data-ttu-id="294f5-136">au_n + bv_n \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="294f5-136">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="294f5-137">Uma [*matriz*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) de tamanho $m \times n $ é uma coleção de $ números complexos $MN organizados em $m $ linhas e $n $ colunas, conforme mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="294f5-137">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="294f5-138">$ $M = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-138">$$M = \begin{bmatrix}</span></span>
<span data-ttu-id="294f5-139">M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2n } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-139">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="294f5-140">M_ {M1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {Mn } \\ \\ \end{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="294f5-140">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\ \end{bmatrix}.$$</span></span>

<span data-ttu-id="294f5-141">Observe que um vetor de $n de dimensão $ é simplesmente uma matriz de tamanho $n \times 1 $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-141">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="294f5-142">Assim como acontece com os vetores, podemos multiplicar uma matriz com um número $c $ para obter uma nova matriz em que cada entrada é multiplicada com $c $ , e podemos adicionar duas matrizes do mesmo tamanho para produzir uma nova matriz cujas entradas são a soma das respectivas entradas das duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="294f5-142">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="294f5-143">Multiplicação de matriz e produtos tensor</span><span class="sxs-lookup"><span data-stu-id="294f5-143">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="294f5-144">Também podemos multiplicar duas matrizes $M $ da dimensão $m \times n $ e $N $ da dimensão $n \times p $ para obter uma nova matriz $P $ do Dimension $m \times p da $ seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="294f5-144">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

<span data-ttu-id="294f5-145">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="294f5-145">\begin{align}</span></span>
<span data-ttu-id="294f5-146">& \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-146">&\begin{bmatrix}</span></span>
    <span data-ttu-id="294f5-147">M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2n } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-147">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
    <span data-ttu-id="294f5-148">M_ {M1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {MN}</span><span class="sxs-lookup"><span data-stu-id="294f5-148">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
<span data-ttu-id="294f5-149">completobmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-149">\end{bmatrix}</span></span>
<span data-ttu-id="294f5-150">Comecebmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-150">\begin{bmatrix}</span></span>
<span data-ttu-id="294f5-151">N_ {11 } ~ ~ N_ {12 } ~ ~ \cdots ~ ~ N_ {1p } \\ \\ N_ {21 } ~ ~ N_ {22 } ~ ~ \cdots ~ ~ N_ {2P } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-151">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\ N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="294f5-152">N_ {N1 } ~ ~ N_ {N2 } ~ ~ \cdots ~ ~ N_ {NP}</span><span class="sxs-lookup"><span data-stu-id="294f5-152">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
<span data-ttu-id="294f5-153">\end{ bmatrix } = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-153">\end{bmatrix}=\begin{bmatrix}</span></span>
<span data-ttu-id="294f5-154">P_ {11 } ~ ~ P_ {12 } ~ ~ \cdots ~ ~ P_ {1p } \\ \\ P_ {21 } ~ ~ P_ {22 } ~ ~ \cdots ~ ~ P_ {2P } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-154">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\ P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="294f5-155">P_ {M1 } ~ ~ P_ {m2 } ~ ~ \cdots ~ ~ P_ {MP}</span><span class="sxs-lookup"><span data-stu-id="294f5-155">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
<span data-ttu-id="294f5-156">completobmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-156">\end{bmatrix}</span></span>
<span data-ttu-id="294f5-157">\end{align}</span><span class="sxs-lookup"><span data-stu-id="294f5-157">\end{align}</span></span>

<span data-ttu-id="294f5-158">onde as entradas de $P $ são $P _ {IK } = \ sum_j M_ {ij} N_ {JK } $.</span><span class="sxs-lookup"><span data-stu-id="294f5-158">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="294f5-159">Por exemplo, a entrada $P _ {11 } $ é o produto interno da primeira linha de $M $ com a primeira coluna de $N $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-159">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$.</span></span> <span data-ttu-id="294f5-160">Observe que, como um vetor é simplesmente um caso especial de uma matriz, essa definição se estende à multiplicação do vetor de matriz.</span><span class="sxs-lookup"><span data-stu-id="294f5-160">Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="294f5-161">Todas as matrizes que consideramos serão matrizes quadradas, em que o número de linhas e colunas são iguais, ou vetores, que correspondem a apenas $1 $ colunas.</span><span class="sxs-lookup"><span data-stu-id="294f5-161">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="294f5-162">Uma matriz quadrada especial é a [*matriz de identidade*](https://en.wikipedia.org/wiki/Identity_matrix), denotada $ \boldone $ , que tem todos os elementos diagonais iguais a $1 $ e os elementos restantes iguais a $0 $ :</span><span class="sxs-lookup"><span data-stu-id="294f5-162">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

<span data-ttu-id="294f5-163">US $ $ \boldone = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-163">$$\boldone=\begin{bmatrix}</span></span>
<span data-ttu-id="294f5-164">1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-164">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="294f5-165">0 ~ ~ 1 ~ ~ \cdots ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-165">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="294f5-166">~ ~ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-166">~~ \ddots\\\\</span></span>
<span data-ttu-id="294f5-167">0 ~ ~ 0 ~ ~ \cdots ~ ~ 1 \end{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="294f5-167">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="294f5-168">Para uma matriz quadrada $A $ , dizemos que uma matriz $B $ é seu [*inverso*](https://en.wikipedia.org/wiki/Invertible_matrix) se $AB = BA = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-168">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="294f5-169">O inverso de uma matriz não precisa existir, mas quando ela existe, ela é exclusiva e a denotamos $A ^ {-1 } $.</span><span class="sxs-lookup"><span data-stu-id="294f5-169">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="294f5-170">Para qualquer matriz $M $ , a transpoção adjacente ou Conjugate de $M $ é uma matriz $N de $ forma que $N _ {IJ } = M_ {ji } ^ \* $.</span><span class="sxs-lookup"><span data-stu-id="294f5-170">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="294f5-171">Em geral, o adjoin of $M $ é indicado $M ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-171">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="294f5-172">Dizemos que um $U de matriz $ é [*unitário*](https://en.wikipedia.org/wiki/Unitary_matrix) se $uu ^ \dagger = U ^ \dagger u = \boldone $ ou equivalente, $U ^ {-1 } = u ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-172">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="294f5-173">Talvez a propriedade mais importante das matrizes de unitários seja que elas preservam a norma de um vetor.</span><span class="sxs-lookup"><span data-stu-id="294f5-173">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="294f5-174">Isso acontece porque</span><span class="sxs-lookup"><span data-stu-id="294f5-174">This happens because</span></span> 

<span data-ttu-id="294f5-175">$ $ \langle v, v \rangle = v ^ \dagger v = v ^ \dagger U ^ {-1 } u v = v ^ \Dagger U ^ \Dagger u v = \Langle u v, u v \rangle . $ $</span><span class="sxs-lookup"><span data-stu-id="294f5-175">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="294f5-176">Um $M de matriz $ é considerado [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) se $M = M ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="294f5-176">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="294f5-177">Por fim, o [*produto tensor*](https://en.wikipedia.org/wiki/Tensor_product) (ou o produto Kronecker) de duas matrizes $M $ de tamanho $m \times n $ e $N $ de tamanho $p \times q $ é uma matriz maior $P = M \otimes n $ de tamanho $mp \times NQ $ e é obtido de $M $ e $N da $ seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="294f5-177">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

<span data-ttu-id="294f5-178">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="294f5-178">\begin{align}</span></span>
    <span data-ttu-id="294f5-179">M \otimes N &= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-179">M \otimes N &= \begin{bmatrix}</span></span>
        <span data-ttu-id="294f5-180">M_ {11 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-180">M_{11} ~~ \cdots ~~ M_{1n} \\\\ \ddots\\\\</span></span>
        <span data-ttu-id="294f5-181">M_ {M1 } ~ ~ \cdots ~ ~ M_ {MN}</span><span class="sxs-lookup"><span data-stu-id="294f5-181">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    <span data-ttu-id="294f5-182">completobmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-182">\end{bmatrix}</span></span>
    <span data-ttu-id="294f5-183">\otimes \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-183">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="294f5-184">N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-184">N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="294f5-185">N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq}</span><span class="sxs-lookup"><span data-stu-id="294f5-185">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    <span data-ttu-id="294f5-186">\end{ bmatrix } \\ \\ &= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-186">\end{bmatrix}\\\\ &= \begin{bmatrix}</span></span>
        <span data-ttu-id="294f5-187">M_ {11 } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq } \end{ bmatrix } ~ ~ \cdots ~ ~ M_ {1N } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq } \end{ bmatrix } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="294f5-187">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="294f5-188">M_ {M1 } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq } \end{ bmatrix } ~ ~ \cdots ~ ~ M_ {Mn } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq } \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-188">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="294f5-189">\end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="294f5-189">\end{bmatrix}.</span></span>
<span data-ttu-id="294f5-190">\end{align}</span><span class="sxs-lookup"><span data-stu-id="294f5-190">\end{align}</span></span>

<span data-ttu-id="294f5-191">Isso é melhor demonstrado com alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="294f5-191">This is better demonstrated with some examples:</span></span>

<span data-ttu-id="294f5-192">US $ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-192">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="294f5-193">a \\ \\ b \end{ bmatrix } \otimes \begin{ bmatrix } c \\ \\ d \\ \\ e \end{ bmatrix } = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-193">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} = \begin{bmatrix}</span></span>
        <span data-ttu-id="294f5-194">\begin{ bmatrix } c \\ \\ d \\ \\ e \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-194">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="294f5-195">\\\\[1,5 em] b \begin{ bmatrix } c \\ \\ d \\ \\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-195">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    <span data-ttu-id="294f5-196">completobmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-196">\end{bmatrix}</span></span>
    <span data-ttu-id="294f5-197">= \begin{ bmatrix } a \\ \\ d a \\ \\ e \\ \\ b c \\ \\ b d \\ \\\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-197">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="294f5-198">e</span><span class="sxs-lookup"><span data-stu-id="294f5-198">and</span></span>

<span data-ttu-id="294f5-199">US $ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-199">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="294f5-200">a \ b \\ \\ c \ d \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-200">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    <span data-ttu-id="294f5-201">\otimes \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-201">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="294f5-202">e \ f \\ \\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-202">e\ f\\\\g\ h \end{bmatrix}</span></span>
     <span data-ttu-id="294f5-203">= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-203">= \begin{bmatrix}</span></span>
    <span data-ttu-id="294f5-204">um\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-204">a\begin{bmatrix}</span></span>
    <span data-ttu-id="294f5-205">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-205">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="294f5-206">b\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-206">b\begin{bmatrix}</span></span>
    <span data-ttu-id="294f5-207">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-207">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="294f5-208">\\\\[1em] c\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-208">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="294f5-209">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-209">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="294f5-210">3D\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-210">d\begin{bmatrix}</span></span>
    <span data-ttu-id="294f5-211">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-211">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="294f5-212">completobmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-212">\end{bmatrix}</span></span>
    <span data-ttu-id="294f5-213">= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="294f5-213">= \begin{bmatrix}</span></span>
    <span data-ttu-id="294f5-214">AE \ AF \ ser \ BF \\ \\ AG \ Ah \ BG \ BH \\ \\ CE \ CF \ de \ DF \\ \\ CG \ ch \ DG \ DH \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="294f5-214">ae\ af\ be\ bf \\\\ ag\ ah\ bg\ bh \\\\ ce\ cf\ de\ df \\\\ cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="294f5-215">Uma Convenção de notação útil final ao redor dos produtos tensor é que, para qualquer vetor $v $ ou matriz $M $ , $v ^ {\otimes n } $ ou $M ^ {\otimes n } $ é curto para um $ produto tensor repetido de $n.</span><span class="sxs-lookup"><span data-stu-id="294f5-215">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="294f5-216">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="294f5-216">For example:</span></span>

<span data-ttu-id="294f5-217">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="294f5-217">\begin{align}</span></span>
<span data-ttu-id="294f5-218">& \begin{ bmatrix } 1 \\ \\ 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 1 \\ \\ 0 \end{ bmatrix } , \qquad \begin{bmatrix} 1 \\ \\ 0 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 1 0 0 0 \\ \\ \\ \\ \\ \\ \end{ bmatrix } , \qquad \begin{bmatrix} 1 \\ \\ -1 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 1 \\ \\ -1 \\ \\ -1 \\ \\ 1 \end{ bmatrix } , \\ \\ & \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } , \qquad \begin{bmatrix} 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 0 &0&0&1 \\ \\ 0 &0&1&0 \\ \\ 0 &1&0&0 \\\\ 1 &0&0&0 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="294f5-218">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\ &\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}    0& 1 \\\\ 1& 0  \end{bmatrix},  \qquad\begin{bmatrix} 0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
<span data-ttu-id="294f5-219">\end{align}</span><span class="sxs-lookup"><span data-stu-id="294f5-219">\end{align}</span></span>
