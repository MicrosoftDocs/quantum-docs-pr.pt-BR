---
title: Criar um Gerador de Número Quântico Aleatório
description: Crie um projeto em Q# que demonstra conceitos quânticos fundamentais, como sobreposição, criando um gerador de número quântico aleatório.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: d1ad2c1153814e2fa19a38307b2c668c77eae4e3
ms.sourcegitcommit: b7e205aaa7fa1ca9f0daa163e46154945f4bc965
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/18/2020
ms.locfileid: "77441066"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="dd2e7-103">Início Rápido: Implementar um Gerador de Número Quântico Aleatório em Q#</span><span class="sxs-lookup"><span data-stu-id="dd2e7-103">Quickstart: Implement a Quantum Random Number Generator in Q#</span></span>
<span data-ttu-id="dd2e7-104">Um exemplo simples de um algoritmo quântico escrito em Q# é um gerador de número quântico aleatório.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="dd2e7-105">Esse algoritmo usa a natureza da mecânica quântica para produzir um número aleatório.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="dd2e7-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="dd2e7-106">Prerequisites</span></span>

- <span data-ttu-id="dd2e7-107">O Microsoft [Quantum development kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="dd2e7-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="dd2e7-108">Criar um projeto Q#</span><span class="sxs-lookup"><span data-stu-id="dd2e7-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a><span data-ttu-id="dd2e7-109">Escrever uma operação Q#</span><span class="sxs-lookup"><span data-stu-id="dd2e7-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="dd2e7-110">Código de operação Q#</span><span class="sxs-lookup"><span data-stu-id="dd2e7-110">Q# operation code</span></span>

1. <span data-ttu-id="dd2e7-111">Substitua o conteúdo do arquivo Operations.qs pelo seguinte código:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-111">Replace the contents of the Operation.qs file with the following code:</span></span>

 :::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-14":::

<span data-ttu-id="dd2e7-112">Conforme mencionado em nosso artigo [O que é Computação Quântica?](xref:microsoft.quantum.overview.what), um qubit é uma unidade de informações quânticas que podem estar em sobreposição.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-112">As mentioned in our [What is Quantum Computing?](xref:microsoft.quantum.overview.what) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="dd2e7-113">Quando medido, um qubit pode ser apenas 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="dd2e7-114">No entanto, durante a execução, o estado do qubit representa a probabilidade de ler 0 ou 1 com uma medida.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="dd2e7-115">Esse estado probabilístico é conhecido como sobreposição.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="dd2e7-116">Podemos usar essa probabilidade para gerar números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="dd2e7-117">Em nossa operação de Q#, apresentamos o tipo de dados `Qubit`, nativo para Q#.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="dd2e7-118">Podemos alocar apenas um `Qubit` com uma instrução `using`.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="dd2e7-119">Quando é alocado, um qubit está sempre no estado `Zero`.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-119">When it gets allocated, a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="dd2e7-120">Usando a operação `H`, podemos colocar nosso `Qubit` em sobreposição.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="dd2e7-121">Para medir um qubit e ler seu valor, use a operação intrínseca `M`.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="dd2e7-122">Ao colocar nosso `Qubit` em sobreposição e medi-lo, nosso resultado será um valor diferente cada vez que o código for invocado.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span> 

<span data-ttu-id="dd2e7-123">Quando um `Qubit` for desalocado, ele deverá ser explicitamente definido de volta para o estado `Zero`; caso contrário, o simulador relatará um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-123">When a `Qubit` is de-allocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="dd2e7-124">Uma maneira fácil de alcançar isso é invocar `Reset`.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="dd2e7-125">Visualizar o código com a esfera Bloch</span><span class="sxs-lookup"><span data-stu-id="dd2e7-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="dd2e7-126">Na esfera Bloch, o polo norte representa o valor clássico **0** e o polo sul representa o valor clássico **1**.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-126">In the Bloch sphere, the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="dd2e7-127">Qualquer sobreposição pode ser representada por um ponto na esfera (representada por uma seta).</span><span class="sxs-lookup"><span data-stu-id="dd2e7-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="dd2e7-128">Quanto mais próxima a extremidade da seta estiver de um polo, maior a probabilidade de o qubit recolher o valor clássico atribuído a esse polo quando medido.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-128">The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="dd2e7-129">Por exemplo, o estado do qubit representado pela seta vermelha abaixo terá uma probabilidade mais alta de dar o valor **0** se medirmos isso.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="~/media/qrng-Bloch.png" width="175">

<span data-ttu-id="dd2e7-130">Podemos usar essa representação para visualizar o que o código está fazendo:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="dd2e7-131">Primeiro, começamos com um qubit inicializado no estado **0** e aplicamos `H` para criar uma sobreposição na qual as probabilidades de **0** e **1** são as mesmas.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-131">First we start with a qubit initalizated in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="~/media/qrng-H.png" width="450">

* <span data-ttu-id="dd2e7-132">Em seguida, medimos o qubit e salvamos a saída:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-132">Then we measure the qubit and save the output:</span></span>

<img src="~/media/qrng-meas.png" width="450">

<span data-ttu-id="dd2e7-133">Como o resultado da medição é completamente aleatório, obtivemos um bit aleatório.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="dd2e7-134">Podemos chamar essa operação várias vezes para criar inteiros.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="dd2e7-135">Por exemplo, se chamarmos a operação três vezes para obter três bits aleatórios, poderemos criar números aleatórios de 3 bits (ou seja, um número aleatório entre 0 e 7).</span><span class="sxs-lookup"><span data-stu-id="dd2e7-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>

## <a name="creating-a-complete-random-number-generator-using-a-host-program"></a><span data-ttu-id="dd2e7-136">Criar um gerador de número aleatório completo usando um programa de host</span><span class="sxs-lookup"><span data-stu-id="dd2e7-136">Creating a complete random number generator using a host program</span></span>

<span data-ttu-id="dd2e7-137">Agora que temos uma operação em Q# que gera bits aleatórios, podemos usá-la para criar um gerador de número quântico aleatório completo com um programa de host.</span><span class="sxs-lookup"><span data-stu-id="dd2e7-137">Now that we have a Q# operation that generates random bits, we can use it to build a complete quantum random number generator with a host program.</span></span>

 ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="dd2e7-138">Python com Visual Studio Code ou a linha de comando</span><span class="sxs-lookup"><span data-stu-id="dd2e7-138">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)
 
 <span data-ttu-id="dd2e7-139">Para executar o novo programa Q# no Python, salve o seguinte código como `host.py`:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-139">To run your new Q# program from Python, save the following code as `host.py`:</span></span>
 
:::code language="python" source="~/quantum/samples/getting-started/qrng/host.py" range="11-30":::

 <span data-ttu-id="dd2e7-140">Em seguida, execute o programa host do Python na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-140">You can then run your Python host program from the command line:</span></span>
 ```bash
 $ python host.py
 Preparing Q# environment...
 ..The random number generated is 42
 ```
 ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="dd2e7-141">C# com Visual Studio Code ou a linha de comando</span><span class="sxs-lookup"><span data-stu-id="dd2e7-141">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)
 
 <span data-ttu-id="dd2e7-142">Para executar o novo programa Q# no C#, modifique `Driver.cs` para incluir o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-142">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>
 
 :::code language="csharp" source="~/quantum/samples/getting-started/qrng/Host.cs" range="4-39":::
 
 <span data-ttu-id="dd2e7-143">Em seguida, execute o programa host do C# na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-143">You can then run your C# host program from the command line:</span></span>
 
 ```bash
 $ dotnet run
 The random number generated is 42
 ```

 ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="dd2e7-144">C# com Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="dd2e7-144">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

 <span data-ttu-id="dd2e7-145">Para executar seu novo programa em Q# no C# no Visual Studio, modifique `Driver.cs` para incluir o seguinte código C#:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-145">To run your new Q# program from C# in Visual Studio, modify `Driver.cs` to include the following C# code:</span></span>

 :::code language="csharp" source="~/quantum/samples/getting-started/qrng/Host.cs" range="4-39":::

 <span data-ttu-id="dd2e7-146">Em seguida, pressione F5. O programa iniciará a execução e uma nova janela será exibida com o número aleatório gerado:</span><span class="sxs-lookup"><span data-stu-id="dd2e7-146">Then press F5, the program will start execution and a new window will pop up with the random number generated:</span></span> 

 ```bash
 $ dotnet run
 The random number generated is 42
 ```
 ***
