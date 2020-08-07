---
title: Usando a Q# biblioteca de numéricos da Microsoft
description: Saiba mais sobre os tipos e as operações disponíveis na biblioteca de numéricos do Microsoft Quantum.
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.usage
no-loc:
- Q#
- $$v
ms.openlocfilehash: 474fc74b9c92fbf28c0618a3090905d025699d32
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868790"
---
# <a name="using-the-numerics-library"></a><span data-ttu-id="cd928-103">Usando a biblioteca de numéricos</span><span class="sxs-lookup"><span data-stu-id="cd928-103">Using the Numerics library</span></span>

## <a name="overview"></a><span data-ttu-id="cd928-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="cd928-104">Overview</span></span>

<span data-ttu-id="cd928-105">A biblioteca de numéricos consiste em três componentes</span><span class="sxs-lookup"><span data-stu-id="cd928-105">The Numerics library consists of three components</span></span>

1. <span data-ttu-id="cd928-106">**Aritmética de inteiro básica** com somas e comparadores de inteiros</span><span class="sxs-lookup"><span data-stu-id="cd928-106">**Basic integer arithmetic** with integer adders and comparators</span></span>
1. <span data-ttu-id="cd928-107">**Funcionalidade de inteiro de alto nível** criada com base na funcionalidade básica; inclui multiplicação, divisão, inversão, etc.  para inteiros assinados e não assinados.</span><span class="sxs-lookup"><span data-stu-id="cd928-107">**High-level integer functionality** that is built on top of the basic  functionality; it includes multiplication, division, inversion, etc.  for signed and unsigned integers.</span></span>
1. <span data-ttu-id="cd928-108">**Funcionalidade aritmética de ponto fixo** com inicialização de ponto fixo, adição, multiplicação, recíproca, avaliação polinomial e medição.</span><span class="sxs-lookup"><span data-stu-id="cd928-108">**Fixed-point arithmetic functionality** with fixed-point initialization,  addition, multiplication, reciprocal, polynomial evaluation, and measurement.</span></span>

<span data-ttu-id="cd928-109">Todos esses componentes podem ser acessados usando uma única `open` instrução:</span><span class="sxs-lookup"><span data-stu-id="cd928-109">All of these components can be accessed using a single `open` statement:</span></span>
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a><span data-ttu-id="cd928-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="cd928-110">Types</span></span>

<span data-ttu-id="cd928-111">A biblioteca de numéricos dá suporte aos seguintes tipos</span><span class="sxs-lookup"><span data-stu-id="cd928-111">The numerics library supports the following types</span></span>

1. <span data-ttu-id="cd928-112">**`LittleEndian`**: Uma matriz qubit `qArr : Qubit[]` que representa um inteiro onde `qArr[0]` denota o bit menos significativo.</span><span class="sxs-lookup"><span data-stu-id="cd928-112">**`LittleEndian`**: A qubit array `qArr : Qubit[]` that represents an integer where `qArr[0]` denotes the least significant bit.</span></span>
1. <span data-ttu-id="cd928-113">**`SignedLittleEndian`**: Igual a `LittleEndian` , exceto que representa um inteiro assinado armazenado no complemento de dois.</span><span class="sxs-lookup"><span data-stu-id="cd928-113">**`SignedLittleEndian`**: Same as `LittleEndian` except that it represents a signed integer stored in two's complement.</span></span>
1. <span data-ttu-id="cd928-114">**`FixedPoint`**: Representa um número real que consiste em uma matriz qubit `qArr2 : Qubit[]` e uma posição de ponto binário `pos` , que conta o número de dígitos binários à esquerda do ponto binário.</span><span class="sxs-lookup"><span data-stu-id="cd928-114">**`FixedPoint`**: Represents a real number consisting of a qubit array `qArr2 : Qubit[]` and a binary point position `pos`, which counts the number of binary digits to the left of the binary point.</span></span> <span data-ttu-id="cd928-115">`qArr2`é armazenado da mesma maneira que o `SignedLittleEndian` .</span><span class="sxs-lookup"><span data-stu-id="cd928-115">`qArr2` is stored in the same way as `SignedLittleEndian`.</span></span>

## <a name="operations"></a><span data-ttu-id="cd928-116">Operações</span><span class="sxs-lookup"><span data-stu-id="cd928-116">Operations</span></span>

<span data-ttu-id="cd928-117">Para cada um dos três tipos acima, uma variedade de operações está disponível:</span><span class="sxs-lookup"><span data-stu-id="cd928-117">For each of the three types above, a variety of operations is available:</span></span>

1. **`LittleEndian`**
    - <span data-ttu-id="cd928-118">Adição</span><span class="sxs-lookup"><span data-stu-id="cd928-118">Addition</span></span>
    - <span data-ttu-id="cd928-119">Comparação</span><span class="sxs-lookup"><span data-stu-id="cd928-119">Comparison</span></span>
    - <span data-ttu-id="cd928-120">Multiplicação</span><span class="sxs-lookup"><span data-stu-id="cd928-120">Multiplication</span></span>
    - <span data-ttu-id="cd928-121">Elevar</span><span class="sxs-lookup"><span data-stu-id="cd928-121">Squaring</span></span>
    - <span data-ttu-id="cd928-122">Divisão (com restante)</span><span class="sxs-lookup"><span data-stu-id="cd928-122">Division (with remainder)</span></span>

1. **`SignedLittleEndian`**
    - <span data-ttu-id="cd928-123">Adição</span><span class="sxs-lookup"><span data-stu-id="cd928-123">Addition</span></span>
    - <span data-ttu-id="cd928-124">Comparação</span><span class="sxs-lookup"><span data-stu-id="cd928-124">Comparison</span></span>
    - <span data-ttu-id="cd928-125">Complemento do módulo 2 da inversão</span><span class="sxs-lookup"><span data-stu-id="cd928-125">Inversion modulo 2's complement</span></span>
    - <span data-ttu-id="cd928-126">Multiplicação</span><span class="sxs-lookup"><span data-stu-id="cd928-126">Multiplication</span></span>
    - <span data-ttu-id="cd928-127">Elevar</span><span class="sxs-lookup"><span data-stu-id="cd928-127">Squaring</span></span>

1. **`FixedPoint`**
    - <span data-ttu-id="cd928-128">Preparação/inicialização para um valor clássico</span><span class="sxs-lookup"><span data-stu-id="cd928-128">Preparation / initialization to a classical values</span></span>
    - <span data-ttu-id="cd928-129">Adição (constante clássica ou outro ponto fixo da Quantum)</span><span class="sxs-lookup"><span data-stu-id="cd928-129">Addition (classical constant or other quantum fixed-point)</span></span>
    - <span data-ttu-id="cd928-130">Comparação</span><span class="sxs-lookup"><span data-stu-id="cd928-130">Comparison</span></span>
    - <span data-ttu-id="cd928-131">Multiplicação</span><span class="sxs-lookup"><span data-stu-id="cd928-131">Multiplication</span></span>
    - <span data-ttu-id="cd928-132">Elevar</span><span class="sxs-lookup"><span data-stu-id="cd928-132">Squaring</span></span>
    - <span data-ttu-id="cd928-133">Avaliação polinomial com especialização para funções pares e ímpares</span><span class="sxs-lookup"><span data-stu-id="cd928-133">Polynomial evaluation with specialization for even and odd functions</span></span>
    - <span data-ttu-id="cd928-134">Recíproco (1/x)</span><span class="sxs-lookup"><span data-stu-id="cd928-134">Reciprocal (1/x)</span></span>
    - <span data-ttu-id="cd928-135">Medida (duplo clássico)</span><span class="sxs-lookup"><span data-stu-id="cd928-135">Measurement (classical Double)</span></span>

<span data-ttu-id="cd928-136">Para obter mais informações e documentação detalhada para cada uma dessas operações, consulte os Q# documentos de referência da biblioteca em [docs.Microsoft.com](https://docs.microsoft.com/quantum)</span><span class="sxs-lookup"><span data-stu-id="cd928-136">For more information and detailed documentation for each of these operations, see the Q# library reference docs at [docs.microsoft.com](https://docs.microsoft.com/quantum)</span></span>

## <a name="sample-integer-addition"></a><span data-ttu-id="cd928-137">Exemplo: adição de inteiro</span><span class="sxs-lookup"><span data-stu-id="cd928-137">Sample: Integer addition</span></span>

<span data-ttu-id="cd928-138">Como um exemplo básico, considere a operação $ $ \ket x\ket y\mapsto \ket x\ket {x + y} $ $ ou seja, uma operação que usa um inteiro n-qubit $x $ e um n-ou (n + 1)-qubit registrar $y $ como entrada, o último que ele mapeia para a soma $ (x + y) $.</span><span class="sxs-lookup"><span data-stu-id="cd928-138">As a basic example, consider the operation $$ \ket x\ket y\mapsto \ket x\ket{x+y} $$ that is, an operation that takes an n-qubit integer $x$ and an n- or (n+1)-qubit register $y$ as input, the latter of which it maps to the sum $(x+y)$.</span></span> <span data-ttu-id="cd928-139">Observe que a soma é o módulo computado $2 ^ n $ se $y $ é armazenado em um registro de $n de bits.</span><span class="sxs-lookup"><span data-stu-id="cd928-139">Note that the sum is computed modulo $2^n$ if $y$ is stored in an $n$-bit register.</span></span>

<span data-ttu-id="cd928-140">Usando o kit de desenvolvimento Quantum, essa operação pode ser aplicada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cd928-140">Using the Quantum Development Kit, this operation can be applied as follows:</span></span>
```qsharp
operation TestMyAddition(xValue : Int, yValue : Int, n : Int) : Unit {
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        let x = LittleEndian(xQubits); // define bit order
        let y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xValue, x); // initialize values
        ApplyXorInPlace(yValue, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a><span data-ttu-id="cd928-141">Exemplo: avaliando funções suaves</span><span class="sxs-lookup"><span data-stu-id="cd928-141">Sample: Evaluating smooth functions</span></span>

<span data-ttu-id="cd928-142">Para avaliar funções suaves, como $ \sin (x) $ em um computador Quantum, em que $x $ é um `FixedPoint` número Quantum, a biblioteca de numéricos do Quantum Development Kit fornece as operações `EvaluatePolynomialFxP` e `Evaluate[Even/Odd]PolynomialFxP` .</span><span class="sxs-lookup"><span data-stu-id="cd928-142">To evaluate smooth functions such as $\sin(x)$ on a quantum computer, where $x$ is a quantum `FixedPoint` number, the Quantum Development Kit numerics library provides the operations `EvaluatePolynomialFxP` and `Evaluate[Even/Odd]PolynomialFxP`.</span></span>

<span data-ttu-id="cd928-143">O primeiro, `EvaluatePolynomialFxP` , permite avaliar um polinomial da forma $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \cdots + a_dx ^ d, $ $, em que $d $ denota o *grau*.</span><span class="sxs-lookup"><span data-stu-id="cd928-143">The first, `EvaluatePolynomialFxP`, allows to evaluate a polynomial of the form $$ P(x) = a_0 + a_1x + a_2x^2 + \cdots + a_dx^d, $$ where $d$ denotes the *degree*.</span></span> <span data-ttu-id="cd928-144">Para fazer isso, tudo o que é necessário são os coeficientes polinomiais `[a_0,..., a_d]` (do tipo `Double[]` ), a entrada `x : FixedPoint` e a saída `y : FixedPoint` (inicialmente zero):</span><span class="sxs-lookup"><span data-stu-id="cd928-144">To do so, all that is needed are the polynomial coefficients `[a_0,..., a_d]` (of type `Double[]`), the input `x : FixedPoint` and the output `y : FixedPoint` (initially zero):</span></span>
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="cd928-145">O resultado, $P (x) = 1 + 2x $, será armazenado em `yFxP` .</span><span class="sxs-lookup"><span data-stu-id="cd928-145">The result, $P(x)=1+2x$, will be stored in `yFxP`.</span></span>

<span data-ttu-id="cd928-146">A segunda, `EvaluateEvenPolynomialFxP` e a terceira, `EvaluateOddPolynomialFxP` são especializações para os casos de funções pares e ímpares, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cd928-146">The second, `EvaluateEvenPolynomialFxP`, and the third, `EvaluateOddPolynomialFxP`, are specializations for the cases of even and odd functions, respectively.</span></span> <span data-ttu-id="cd928-147">Ou seja, para uma função par/ímpar $f (x) $ e $ $ P_ {mesmo} (x) = a_0 + a_1 x ^ 2 + a_2 x ^ 4 + \cdots + a_d x ^ {2D}, $ $ $f (x) $ é aproximado bem pelo $P _ {mesmo} (x) $ ou $P _ {Odd} (x): = x\cdot P_ {mesmo} (x) $, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cd928-147">That is, for an even/odd function $f(x)$ and $$ P_{even}(x)=a_0 + a_1 x^2 + a_2 x^4 + \cdots + a_d x^{2d}, $$ $f(x)$ is approximated well by $P_{even}(x)$ or $P_{odd}(x) := x\cdot P_{even}(x)$, respectively.</span></span>
<span data-ttu-id="cd928-148">No Q# , esses dois casos podem ser tratados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cd928-148">In Q#, these two cases can be handled as follows:</span></span>
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="cd928-149">que avalia $P _ {mesmo} (x) = 1 + 2x ^ 2 $ e</span><span class="sxs-lookup"><span data-stu-id="cd928-149">which evaluates $P_{even}(x) = 1 + 2x^2$, and</span></span>
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="cd928-150">que avalia $P _ {Odd} (x) = x + 2x ^ 3 $.</span><span class="sxs-lookup"><span data-stu-id="cd928-150">which evaluates $P_{odd}(x) = x + 2x^3$.</span></span>

## <a name="more-samples"></a><span data-ttu-id="cd928-151">Mais exemplos</span><span class="sxs-lookup"><span data-stu-id="cd928-151">More samples</span></span>

<span data-ttu-id="cd928-152">Você pode encontrar mais exemplos no [repositório principal de exemplos](https://github.com/Microsoft/Quantum).</span><span class="sxs-lookup"><span data-stu-id="cd928-152">You can find more samples in the [main samples repository](https://github.com/Microsoft/Quantum).</span></span>

<span data-ttu-id="cd928-153">Para começar, clone o repositório e abra a `Numerics` subpasta:</span><span class="sxs-lookup"><span data-stu-id="cd928-153">To get started, clone the repo and open the `Numerics` subfolder:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/Numerics
```

<span data-ttu-id="cd928-154">Em seguida, `cd` em uma das pastas de exemplo e executar o exemplo via</span><span class="sxs-lookup"><span data-stu-id="cd928-154">Then, `cd` into one of the sample folders and run the sample via</span></span>

```bash
dotnet run
```
