---
title: Introdução à Biblioteca de Numéricos do Quantum | Microsoft Docs
description: Introdução à Biblioteca de Numéricos do Quantum
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.intro
ms.openlocfilehash: efd1a712616534ac281433fc008f0983271881d7
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442446"
---
# <a name="introduction-to-the-quantum-numerics-library"></a><span data-ttu-id="eb091-103">Introdução à Biblioteca de Numéricos do Quantum</span><span class="sxs-lookup"><span data-stu-id="eb091-103">Introduction to the Quantum Numerics Library</span></span>

<span data-ttu-id="eb091-104">Muitos algoritmos quantum dependem de [oracles](xref:microsoft.quantum.concepts.oracles) que avaliam as funções matemáticas em uma superposição de entradas.</span><span class="sxs-lookup"><span data-stu-id="eb091-104">Many quantum algorithms rely on [oracles](xref:microsoft.quantum.concepts.oracles) that evaluate mathematical functions on a superposition of inputs.</span></span>
<span data-ttu-id="eb091-105">O principal componente do algoritmo de Shor, por exemplo, avalia $f(x) = a^x\operatorname{mod} N$ para um $a$ fixo, o número para fatorar $N$ e um inteiro de $x$ a $2n$ qubits em uma superposição uniforme em todas as cadeias de caracteres de $2n$ bits.</span><span class="sxs-lookup"><span data-stu-id="eb091-105">The main component of Shor's algorithm, for example, evaluates $f(x) = a^x\operatorname{mod} N$ for a fixed $a$, the number to factor $N$, and $x$ a $2n$-qubit integer in a uniform superposition over all $2n$-bit strings.</span></span>

<span data-ttu-id="eb091-106">Para executar o algoritmo de Shor em um computador quantum real, essa função precisa ser escrita em termos das operações nativas do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="eb091-106">To run Shor's algorithm on an actual quantum computer, this function has to be written in terms of the native operations of the target machine.</span></span>
<span data-ttu-id="eb091-107">Usando a representação binária de $x$ com $x_i$ denotando a contagem de bits $i$-ésimos do bit menos significativo, $f(x)$ pode ser escrito como $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$.</span><span class="sxs-lookup"><span data-stu-id="eb091-107">Using the binary representation of $x$ with $x_i$ denoting the $i$-th bit counting from the least-significant bit, $f(x)$ can be written as $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$.</span></span>
<span data-ttu-id="eb091-108">Por sua vez, isso pode ser escrito como um produto (mod N) de termos $a^{2^i x_i}=(a^{2^i})^{x_i}$.</span><span class="sxs-lookup"><span data-stu-id="eb091-108">In turn, this can be written as a product (mod N) of terms $a^{2^i x_i}=(a^{2^i})^{x_i}$.</span></span> <span data-ttu-id="eb091-109">A função $f(x)$ pode, portanto, ser implementada usando uma sequência de multiplicações $2n$ (modulares) por $a^{2^i}$ condicional em $x_i$ sendo diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="eb091-109">The function $f(x)$ can thus be implemented using a sequence of $2n$ (modular) multiplications by $a^{2^i}$ conditional on $x_i$ being nonzero.</span></span> <span data-ttu-id="eb091-110">As constantes $a^{2^i}$ podem ser pré-calculadas e de módulo N reduzido antes da execução do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="eb091-110">The constants $a^{2^i}$ can be precomputed and reduced modulo N before running the algorithm.</span></span>

<span data-ttu-id="eb091-111">Essa sequência de multiplicações modulares controladas pode ser simplificada ainda mais: Cada multiplicação pode ser efetuada usando uma sequência de $n$ adições modulares controladas; e cada adição modular pode ser criada com base em uma adição regular e um comparador.</span><span class="sxs-lookup"><span data-stu-id="eb091-111">This sequence of controlled modular multiplications can be simplified further: Each multiplication can be performed using a sequence of $n$ controlled modular additions; and each modular addition can be built from a regular addition and a comparator.</span></span>


<span data-ttu-id="eb091-112">Considerando que muitas etapas são necessárias para se chegar a uma implementação real, seria extremamente útil ter essa funcionalidade disponível desde o início.</span><span class="sxs-lookup"><span data-stu-id="eb091-112">Given that so many steps are necessary to arrive at an actual implementation, it would be extremely helpful to have such functionality available from the start.</span></span>
<span data-ttu-id="eb091-113">É por isso que o Quantum Development Kit oferece suporte para uma ampla variedade de funcionalidades numéricas.</span><span class="sxs-lookup"><span data-stu-id="eb091-113">This is why the Quantum Development Kit provides support for a wide range of numerics functionality.</span></span>


## <a name="functionality"></a><span data-ttu-id="eb091-114">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="eb091-114">Functionality</span></span>

<span data-ttu-id="eb091-115">Além da aritmética de inteiros mencionada até agora, a biblioteca de numéricos fornece</span><span class="sxs-lookup"><span data-stu-id="eb091-115">Besides the integer arithmetic mentioned thus far, the numerics library provides</span></span>

 - <span data-ttu-id="eb091-116">Funcionalidade de inteiro com (sem) sinal (multiplicação, quadrado, divisão com resto, inversão...) com um ou dois números inteiros quantum como entrada</span><span class="sxs-lookup"><span data-stu-id="eb091-116">(Un)signed integer functionality (multiply, square, division with remainder, inversion, ...) with one or two quantum integer numbers as input</span></span>
 - <span data-ttu-id="eb091-117">Funcionalidade de ponto fixo (adição/subtração, multiplicação, quadrado, 1/x, avaliação polinomial) com um ou dois números de ponto fixo quantum como entrada</span><span class="sxs-lookup"><span data-stu-id="eb091-117">Fixed-point functionality (add / subtract, multiply, square, 1/x, polynomial evaluation) with one or two quantum fixed-point numbers as input</span></span>

## <a name="getting-started"></a><span data-ttu-id="eb091-118">Introdução</span><span class="sxs-lookup"><span data-stu-id="eb091-118">Getting started</span></span>

<span data-ttu-id="eb091-119">Para começar a usar a biblioteca numérica, confira o [guia de instalação](xref:microsoft.quantum.numerics.installation) e mais informações sobre [como usar a biblioteca numérica](xref:microsoft.quantum.numerics.usage).</span><span class="sxs-lookup"><span data-stu-id="eb091-119">To get started with the Numerics Library, check out the [installation guide](xref:microsoft.quantum.numerics.installation) and more information on [using the Numerics Library](xref:microsoft.quantum.numerics.usage).</span></span>
