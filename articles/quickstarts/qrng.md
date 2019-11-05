---
title: Criar um Gerador de Número Quântico Aleatório
description: Crie um projeto em Q# que demonstra conceitos quânticos fundamentais, como sobreposição, criando um gerador de número quântico aleatório.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: a7c077eda3e46430cbe6598cb899adb460451f75
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443912"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="661e5-103">Início Rápido: Implementar um Gerador de Número Quântico Aleatório em Q#</span><span class="sxs-lookup"><span data-stu-id="661e5-103">Quickstart: Implement a Quantum Random Number Generator in Q#</span></span>
<span data-ttu-id="661e5-104">Um exemplo simples de um algoritmo quântico escrito em Q# é um gerador de número quântico aleatório.</span><span class="sxs-lookup"><span data-stu-id="661e5-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="661e5-105">Esse algoritmo usa a natureza da mecânica quântica para produzir um número aleatório.</span><span class="sxs-lookup"><span data-stu-id="661e5-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="661e5-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="661e5-106">Prerequisites</span></span>

- <span data-ttu-id="661e5-107">O Microsoft [Quantum development kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="661e5-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="661e5-108">Criar um projeto Q#</span><span class="sxs-lookup"><span data-stu-id="661e5-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a><span data-ttu-id="661e5-109">Escrever uma operação Q#</span><span class="sxs-lookup"><span data-stu-id="661e5-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="661e5-110">Código de operação Q#</span><span class="sxs-lookup"><span data-stu-id="661e5-110">Q# operation code</span></span>

1. <span data-ttu-id="661e5-111">Substitua o conteúdo do arquivo Operations.qs pelo seguinte código:</span><span class="sxs-lookup"><span data-stu-id="661e5-111">Replace the contents of the Operation.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum {
        open Microsoft.Quantum.Intrinsic;

        operation QuantumRandomNumberGenerator() : Result {
            using(q = Qubit())  { // Allocate a qubit.
                H(q);             // Put the qubit to superposition. It now has a 50% chance of being 0 or 1.
                let r = M(q);     // Measure the qubit value.
                Reset(q);
                return r;
            }
        }
    }
    ```

<span data-ttu-id="661e5-112">Conforme mencionado em nosso artigo [O que é Computação Quântica?](xref:microsoft.quantum.overview.what), um qubit é uma unidade de informações quânticas que podem estar em sobreposição.</span><span class="sxs-lookup"><span data-stu-id="661e5-112">As mentioned in our [What is Quantum Computing?](xref:microsoft.quantum.overview.what) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="661e5-113">Quando medido, um qubit pode ser apenas 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="661e5-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="661e5-114">No entanto, durante a execução, o estado do qubit representa a probabilidade de ler 0 ou 1 com uma medida.</span><span class="sxs-lookup"><span data-stu-id="661e5-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="661e5-115">Esse estado probabilístico é conhecido como sobreposição.</span><span class="sxs-lookup"><span data-stu-id="661e5-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="661e5-116">Podemos usar essa probabilidade para gerar números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="661e5-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="661e5-117">Em nossa operação de Q#, apresentamos o tipo de dados `Qubit`, nativo para Q#.</span><span class="sxs-lookup"><span data-stu-id="661e5-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="661e5-118">Podemos alocar apenas um `Qubit` com uma instrução `using`.</span><span class="sxs-lookup"><span data-stu-id="661e5-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="661e5-119">Quando é alocado, um qubit está sempre no estado `Zero`.</span><span class="sxs-lookup"><span data-stu-id="661e5-119">When it gets allocated a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="661e5-120">Usando a operação `H`, podemos colocar nosso `Qubit` em sobreposição.</span><span class="sxs-lookup"><span data-stu-id="661e5-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="661e5-121">Para medir um qubit e ler seu valor, use a operação intrínseca `M`.</span><span class="sxs-lookup"><span data-stu-id="661e5-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="661e5-122">Ao colocar nosso `Qubit` em sobreposição e medi-lo, nosso resultado será um valor diferente cada vez que o código for invocado.</span><span class="sxs-lookup"><span data-stu-id="661e5-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span> 

<span data-ttu-id="661e5-123">Quando um `Qubit` for desalocado, ele deverá ser explicitamente definido de volta para o estado `Zero`; caso contrário, o simulador relatará um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="661e5-123">When a `Qubit` is de-allocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="661e5-124">Uma maneira fácil de alcançar isso é invocar `Reset`.</span><span class="sxs-lookup"><span data-stu-id="661e5-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="661e5-125">Visualizar o código com a esfera Bloch</span><span class="sxs-lookup"><span data-stu-id="661e5-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="661e5-126">Na esfera Bloch, o polo norte representa o valor clássico **0** e o polo sul representa o valor clássico **1**.</span><span class="sxs-lookup"><span data-stu-id="661e5-126">In the Bloch sphere the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="661e5-127">Qualquer sobreposição pode ser representada por um ponto na esfera (representada por uma seta).</span><span class="sxs-lookup"><span data-stu-id="661e5-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="661e5-128">Quanto mais próxima a extremidade da seta estiver de um polo, maior a probabilidade de o qubit recolher o valor clássico atribuído a esse polo quando medido.</span><span class="sxs-lookup"><span data-stu-id="661e5-128">When the closer the end of the arrow to a pole, the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="661e5-129">Por exemplo, o estado do qubit representado pela seta vermelha abaixo terá uma probabilidade mais alta de dar o valor **0** se medirmos isso.</span><span class="sxs-lookup"><span data-stu-id="661e5-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="./Bloch.svg" width="175">

<span data-ttu-id="661e5-130">Podemos usar essa representação para visualizar o que o código está fazendo:</span><span class="sxs-lookup"><span data-stu-id="661e5-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="661e5-131">Primeiro, começamos com um qubit inicializado no estado **0** e aplicamos `H` para criar uma sobreposição na qual as probabilidades de **0** e **1** são as mesmas.</span><span class="sxs-lookup"><span data-stu-id="661e5-131">First we start with a qubit initalizated in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="./H.svg" width="450">

* <span data-ttu-id="661e5-132">Em seguida, medimos o qubit e salvamos a saída:</span><span class="sxs-lookup"><span data-stu-id="661e5-132">Then we measure the qubit and save the output:</span></span>

<img src="./Measurement2.svg" width="450">

<span data-ttu-id="661e5-133">Como o resultado da medição é completamente aleatório, obtivemos um bit aleatório.</span><span class="sxs-lookup"><span data-stu-id="661e5-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="661e5-134">Podemos chamar essa função várias vezes para criar inteiros.</span><span class="sxs-lookup"><span data-stu-id="661e5-134">We can call this function several times to create integers.</span></span> <span data-ttu-id="661e5-135">Por exemplo, se chamarmos a função três vezes para obter três bits aleatórios, poderemos criar números de 3 bits aleatórios (ou seja, um número aleatório entre 0 e 7).</span><span class="sxs-lookup"><span data-stu-id="661e5-135">For example, if we call the function three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>
