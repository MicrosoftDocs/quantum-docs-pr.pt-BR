---
title: Explorar o entrelaçamento com Q#
description: Saiba como escrever um programa quântico em Q#. Desenvolver um aplicativo de Estado de Bell usando o QDK (Quantum development kit)
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 294366b884da93f11c60cfdbdce9b40cf5202b0d
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274226"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="da108-104">Tutorial: Explorar o emaranhamento com o Q\#</span><span class="sxs-lookup"><span data-stu-id="da108-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="da108-105">Neste tutorial, mostraremos como escrever um programa Q# que processa e mede qubits e demonstra os efeitos da superposição e do emaranhamento.</span><span class="sxs-lookup"><span data-stu-id="da108-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>
<span data-ttu-id="da108-106">Isso orientará você na instalação do QDK, na criação e na execução do programa em um simulador quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-106">This guides you on installing the QDK, building the program and executing that program on a quantum simulator.</span></span>  

<span data-ttu-id="da108-107">Você escreverá um aplicativo chamado Bell para demonstrar o entrelaçamento quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-107">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="da108-108">O nome Bell foi criado em referência aos estados Bell, que são estados quânticos específicos de dois qubits usados para representar os exemplos mais simples de sobreposição e entrelaçamento quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-108">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="da108-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="da108-109">Prerequisites</span></span>

<span data-ttu-id="da108-110">Se estiver pronto para começar a codificação, siga estas etapas antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="da108-110">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="da108-111">Instale o Quantum development kit para o [Python](xref:microsoft.quantum.install.python) ou o [.NET](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="da108-111">Install the Quantum Development Kit for [Python](xref:microsoft.quantum.install.python) or [.NET](xref:microsoft.quantum.install.cs).</span></span>
* <span data-ttu-id="da108-112">Caso já tenha o QDK instalado, verifique se você o [atualizou](xref:microsoft.quantum.update) para a última versão</span><span class="sxs-lookup"><span data-stu-id="da108-112">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="da108-113">Você também pode acompanhar a narrativa sem instalar o QDK, examinar as visões gerais da linguagem de programação Q# e os primeiros conceitos da computação quântica.</span><span class="sxs-lookup"><span data-stu-id="da108-113">You can also follow along with the narrative without installing the QDK, reviewing the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="demonstrating-qubit-behavior-with-q"></a><span data-ttu-id="da108-114">Demonstrar o comportamento do qubit com Q#</span><span class="sxs-lookup"><span data-stu-id="da108-114">Demonstrating qubit behavior with Q#</span></span>

<span data-ttu-id="da108-115">Lembre-se de nossa [definição simples de um qubit](xref:microsoft.quantum.overview.understanding).</span><span class="sxs-lookup"><span data-stu-id="da108-115">Recall our simple [definition of a qubit](xref:microsoft.quantum.overview.understanding).</span></span>  <span data-ttu-id="da108-116">Onde os bits clássicos contêm apenas um valor binário, como 0 ou 1, o estado de um [qubit](xref:microsoft.quantum.glossary#qubit) pode estar em uma **sobreposição** de 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="da108-116">Where classical bits hold a single binary value such as a 0 or 1, the state of a [qubit](xref:microsoft.quantum.glossary#qubit) can be in a **superposition** of 0 and 1.</span></span>  <span data-ttu-id="da108-117">Conceitualmente, um qubit pode ser pensado como uma direção no espaço (também conhecido como um vetor).</span><span class="sxs-lookup"><span data-stu-id="da108-117">Conceptually, a qubit can be thought of as a direction in space (also known as a vector).</span></span>  <span data-ttu-id="da108-118">Um qubit pode estar em qualquer uma das possíveis direções.</span><span class="sxs-lookup"><span data-stu-id="da108-118">A qubit can be in any of the possible directions.</span></span> <span data-ttu-id="da108-119">Os dois **estados clássicos** são as duas direções, que representam 100% de chance de medir 0 e 100% de chance de medir 1.</span><span class="sxs-lookup"><span data-stu-id="da108-119">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>  <span data-ttu-id="da108-120">Essa representação também é visualizada mais formalmente pela [esfera Bloch](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span><span class="sxs-lookup"><span data-stu-id="da108-120">This representation is also more formally visualized by the [bloch sphere](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span></span>

<span data-ttu-id="da108-121">O ato de medição produz um resultado binário e altera um estado do qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-121">The act of measurement produces a binary result and changes a qubit state.</span></span> <span data-ttu-id="da108-122">A medida produz um valor binário, 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="da108-122">Measurement produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="da108-123">O qubit passa de estar em sobreposição (qualquer direção) para um dos estados clássicos.</span><span class="sxs-lookup"><span data-stu-id="da108-123">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="da108-124">Depois disso, repetir a mesma medição sem nenhuma operação intermediária produz o mesmo resultado binário.</span><span class="sxs-lookup"><span data-stu-id="da108-124">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="da108-125">Vários qubits podem ser [**entrelaçados**](xref:microsoft.quantum.glossary#entanglement).</span><span class="sxs-lookup"><span data-stu-id="da108-125">Multiple qubits can be [**entangled**](xref:microsoft.quantum.glossary#entanglement).</span></span> <span data-ttu-id="da108-126">Quando fazemos uma medição de um qubit entrelaçado, nosso conhecimento do estado dos outros é atualizado também.</span><span class="sxs-lookup"><span data-stu-id="da108-126">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="da108-127">Agora, estamos prontos para demonstrar como o Q# expressa esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="da108-127">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="da108-128">Você começará com o programa mais simples possível e o desenvolverá para demonstrar a sobreposição quântica e o entrelaçamento quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-128">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="setup"></a><span data-ttu-id="da108-129">Instalação</span><span class="sxs-lookup"><span data-stu-id="da108-129">Setup</span></span>

<span data-ttu-id="da108-130">Este tutorial usa um programa host e consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="da108-130">This tutorial uses a host programs and consists of two parts:</span></span>

1. <span data-ttu-id="da108-131">Uma série de algoritmos quânticos, implementados usando a linguagem de programação quântica Q#.</span><span class="sxs-lookup"><span data-stu-id="da108-131">A series of quantum algorithms, implemented using the Q# quantum programming language.</span></span>
1. <span data-ttu-id="da108-132">Um programa host, implementado em Python ou em C#, que serve como o principal ponto de entrada e invoca operações Q# para executar os algoritmos quânticos.</span><span class="sxs-lookup"><span data-stu-id="da108-132">A host program, implemented in either Python or C#, that serves as the main entry point and invokes Q# operations to execute the quantum algorithms.</span></span>

#### <a name="python"></a>[<span data-ttu-id="da108-133">Python</span><span class="sxs-lookup"><span data-stu-id="da108-133">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="da108-134">Escolha uma localização para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="da108-134">Choose a location for your application</span></span>

1. <span data-ttu-id="da108-135">Crie um arquivo chamado `Bell.qs`.</span><span class="sxs-lookup"><span data-stu-id="da108-135">Create a file called `Bell.qs`.</span></span> <span data-ttu-id="da108-136">Esse arquivo conterá o código Q#.</span><span class="sxs-lookup"><span data-stu-id="da108-136">This file will contain your Q# code.</span></span>

1. <span data-ttu-id="da108-137">Crie um arquivo chamado `host.py`.</span><span class="sxs-lookup"><span data-stu-id="da108-137">Create a file called `host.py`.</span></span> <span data-ttu-id="da108-138">Esse arquivo conterá o código de host do Python.</span><span class="sxs-lookup"><span data-stu-id="da108-138">This file will contain your Python host code.</span></span>

#### <a name="c-command-line"></a>[<span data-ttu-id="da108-139">Linha de comando do C#</span><span class="sxs-lookup"><span data-stu-id="da108-139">C# Command Line</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="da108-140">Crie um projeto Q#:</span><span class="sxs-lookup"><span data-stu-id="da108-140">Create a new Q# project:</span></span>

    ```
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    <span data-ttu-id="da108-141">Você deverá ver um arquivo `.csproj`, um arquivo Q# chamado `Operations.qs` e um arquivo de programa host chamado `Driver.cs`</span><span class="sxs-lookup"><span data-stu-id="da108-141">You should see a `.csproj` file, a Q# file called `Operations.qs`, and a host program file called `Driver.cs`</span></span>

1. <span data-ttu-id="da108-142">Renomear o arquivo Q#</span><span class="sxs-lookup"><span data-stu-id="da108-142">Rename the Q# file</span></span>

    ```
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[<span data-ttu-id="da108-143">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da108-143">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="da108-144">Criar um novo projeto</span><span class="sxs-lookup"><span data-stu-id="da108-144">Create a new project</span></span>

   * <span data-ttu-id="da108-145">Abra o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da108-145">Open Visual Studio</span></span>
   * <span data-ttu-id="da108-146">Acesse o menu **Arquivo** e selecione **Novo** -> **Projeto...**</span><span class="sxs-lookup"><span data-stu-id="da108-146">Go to the **File** menu and select **New** -> **Project...**</span></span>
   * <span data-ttu-id="da108-147">No gerenciador de modelos de projeto, digite `Q#` no campo de pesquisa e selecione o modelo `Q# Application`</span><span class="sxs-lookup"><span data-stu-id="da108-147">In the project template explorer, type `Q#` into the search field and select the `Q# Application` template</span></span>
   * <span data-ttu-id="da108-148">Dê ao projeto o nome `Bell`</span><span class="sxs-lookup"><span data-stu-id="da108-148">Give your project the name `Bell`</span></span>

1. <span data-ttu-id="da108-149">Renomear o arquivo Q#</span><span class="sxs-lookup"><span data-stu-id="da108-149">Rename the Q# file</span></span>

   * <span data-ttu-id="da108-150">Navegue até o **Gerenciador de Soluções**</span><span class="sxs-lookup"><span data-stu-id="da108-150">Navigate to the **Solution Explorer**</span></span>
   * <span data-ttu-id="da108-151">Clique com o botão direito do mouse no arquivo `Operations.qs`</span><span class="sxs-lookup"><span data-stu-id="da108-151">Right click on the `Operations.qs` file</span></span>
   * <span data-ttu-id="da108-152">Renomeie-o como `Bell.qs`</span><span class="sxs-lookup"><span data-stu-id="da108-152">Rename it to `Bell.qs`</span></span>

* * *

## <a name="write-a-q-operation"></a><span data-ttu-id="da108-153">Escrever uma operação Q#</span><span class="sxs-lookup"><span data-stu-id="da108-153">Write a Q# operation</span></span>

<span data-ttu-id="da108-154">Nossa meta é preparar dois qubits em um estado quântico específico, demonstrando como operar em qubits com Q# para alterar seu estado e demonstrar os efeitos da sobreposição e entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="da108-154">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="da108-155">Criaremos isso em partes para demonstrar os estados, as operações e a medida do qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-155">We will build this up piece by piece to demonstrate qubit states, operations, and measurement.</span></span>

<span data-ttu-id="da108-156">**Visão geral:**  no primeiro código abaixo, mostramos como trabalhar com qubits no Q#.</span><span class="sxs-lookup"><span data-stu-id="da108-156">**Overview:**  In the first code below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="da108-157">Apresentaremos duas operações, `M` e `X`, que transformam o estado de um qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-157">We’ll introduce two operations, `M` and `X` that transform the state of a qubit.</span></span> 

<span data-ttu-id="da108-158">Neste snippet de código, uma operação `Set` é definida que usa como parâmetro um qubit e outro parâmetro, `desired`, que representa o estado no qual gostaríamos que o qubit estivesse.</span><span class="sxs-lookup"><span data-stu-id="da108-158">In this code snippet, an operation `Set` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="da108-159">A operação `Set` executa uma medida no qubit usando a operação `M`.</span><span class="sxs-lookup"><span data-stu-id="da108-159">The operation `Set` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="da108-160">Em Q#, uma medição de qubit sempre retorna `Zero` ou `One`.</span><span class="sxs-lookup"><span data-stu-id="da108-160">In Q#, a qubit measurement always returns either  `Zero` or `One`.</span></span>  <span data-ttu-id="da108-161">Se a medição retornar um valor não igual a um valor desejado, Set “inverterá” o qubit; ou seja, executará uma operação `X`, que altera o estado do qubit para um novo estado no qual as probabilidades de uma medição retornar `Zero` e `One` são invertidas.</span><span class="sxs-lookup"><span data-stu-id="da108-161">If the measurement returns a value not equal to a desired value, Set “flips” the qubit; that is, it executes an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span>  <span data-ttu-id="da108-162">Para demonstrar o efeito da operação `Set`, uma operação `TestBellState` é adicionada.</span><span class="sxs-lookup"><span data-stu-id="da108-162">To demonstrate the effect of the `Set` operation, a `TestBellState` operation is then added.</span></span>  <span data-ttu-id="da108-163">Essa operação aceita como entrada um `Zero` ou `One` e chama a operação `Set` algum número de vezes com essa entrada, além de contar o número de vezes que `Zero` foi retornado da medição do qubit e do número de vezes que `One` foi retornado.</span><span class="sxs-lookup"><span data-stu-id="da108-163">This operation takes as input a `Zero` or `One`, and calls the `Set` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="da108-164">É claro que, nesta primeira simulação da operação `TestBellState`, esperamos que a saída mostre que todas as medições do conjunto de qubits com `Zero` como a entrada do parâmetro retornarão `Zero` e todas as medições de um conjunto de qubits com `One` como a entrada do parâmetro retornarão `One`.</span><span class="sxs-lookup"><span data-stu-id="da108-164">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span>  <span data-ttu-id="da108-165">Mais adiante, adicionaremos código a `TestBellState` para demonstrar a sobreposição e o entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="da108-165">Further on, we’ll add code to `TestBellState` to demonstrating superposition and entanglement.</span></span>


### <a name="q-operation-code"></a><span data-ttu-id="da108-166">Código de operação Q#</span><span class="sxs-lookup"><span data-stu-id="da108-166">Q# operation code</span></span>

1. <span data-ttu-id="da108-167">Substitua o conteúdo do arquivo Bell.qs pelo seguinte código:</span><span class="sxs-lookup"><span data-stu-id="da108-167">Replace the contents of the Bell.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    <span data-ttu-id="da108-168">Esta operação agora pode ser chamada para definir um qubit como um estado clássico, retornando `Zero` 100% do tempo ou retornando `One` 100% do tempo.</span><span class="sxs-lookup"><span data-stu-id="da108-168">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>  <span data-ttu-id="da108-169">`Zero` e `One` são constantes que representam os únicos dois possíveis resultados de uma medição de um qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-169">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

    <span data-ttu-id="da108-170">A operação `Set` mede o qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-170">The operation `Set` measures the qubit.</span></span>
    <span data-ttu-id="da108-171">Se o qubit estiver no estado que desejamos, `Set` o deixará sozinho; caso contrário, executando a operação `X`, alteraremos o estado do qubit para o desejado.</span><span class="sxs-lookup"><span data-stu-id="da108-171">If the qubit is in the state we want, `Set` leaves it alone; otherwise, by executing the `X` operation, we change the qubit state to the desired state.</span></span>

### <a name="about-q-operations"></a><span data-ttu-id="da108-172">Sobre as operações Q#</span><span class="sxs-lookup"><span data-stu-id="da108-172">About Q# operations</span></span>

<span data-ttu-id="da108-173">Uma operação Q# é uma sub-rotina quântica.</span><span class="sxs-lookup"><span data-stu-id="da108-173">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="da108-174">Ou seja, é uma rotina que pode ser chamada que contém operações quânticas.</span><span class="sxs-lookup"><span data-stu-id="da108-174">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="da108-175">Os argumentos de uma operação são especificados como uma tupla, entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="da108-175">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="da108-176">O tipo de retorno da operação é especificado após dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="da108-176">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="da108-177">Nesse caso, a operação `Set` não tem retorno, sendo, portanto, marcada como retornando `Unit`.</span><span class="sxs-lookup"><span data-stu-id="da108-177">In this case, the `Set` operation has no return, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="da108-178">Em Q#, esse é o equivalente de `unit` em F#, que é aproximadamente análogo a `void` em C# e uma tupla vazia (`Tuple[()]`) no Python.</span><span class="sxs-lookup"><span data-stu-id="da108-178">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple (`Tuple[()]`) in Python.</span></span>

<span data-ttu-id="da108-179">Você usou duas operações quânticas em sua primeira operação Q#:</span><span class="sxs-lookup"><span data-stu-id="da108-179">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="da108-180">A operação [M](xref:microsoft.quantum.intrinsic.m), que mede o estado do qubit</span><span class="sxs-lookup"><span data-stu-id="da108-180">The [M](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="da108-181">A operação [X](xref:microsoft.quantum.intrinsic.x), que inverte o estado de um qubit</span><span class="sxs-lookup"><span data-stu-id="da108-181">The [X](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="da108-182">Uma operação quântica transforma o estado de um qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-182">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="da108-183">Algumas vezes, as pessoas falam sobre portões quânticos em vez de operações, em analogia a portões lógicos clássicos.</span><span class="sxs-lookup"><span data-stu-id="da108-183">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="da108-184">Isso está enraizado nos primórdios da computação quântica, quando os algoritmos eram meramente um constructo teórico e eram visualizados como diagramas de forma semelhante à dos diagramas de circuito na computação clássica.</span><span class="sxs-lookup"><span data-stu-id="da108-184">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="add-q-test-code"></a><span data-ttu-id="da108-185">Adicionar um código de teste Q#</span><span class="sxs-lookup"><span data-stu-id="da108-185">Add Q# test code</span></span>

1. <span data-ttu-id="da108-186">Adicione a seguinte operação ao arquivo `Bell.qs`, dentro do namespace, após o final da operação `Set`:</span><span class="sxs-lookup"><span data-stu-id="da108-186">Add the following operation to the `Bell.qs` file, inside the namespace, after the end of the `Set` operation:</span></span>

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    <span data-ttu-id="da108-187">Essa operação (`TestBellState`) executará um loop para iterações `count`, definirá um valor `initial` especificado em um qubit e, em seguida, medirá (`M`) o resultado.</span><span class="sxs-lookup"><span data-stu-id="da108-187">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="da108-188">Ela coletará estatísticas sobre quantos zeros e aqueles medidos e os retornará ao chamador.</span><span class="sxs-lookup"><span data-stu-id="da108-188">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="da108-189">Ela executa outra operação necessária.</span><span class="sxs-lookup"><span data-stu-id="da108-189">It performs one other necessary operation.</span></span> <span data-ttu-id="da108-190">Ela redefine o qubit para um estado conhecido (`Zero`) antes de retorná-lo, permitindo que outras pessoas aloquem esse qubit em um estado conhecido.</span><span class="sxs-lookup"><span data-stu-id="da108-190">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="da108-191">Isso é exigido pela instrução `using`.</span><span class="sxs-lookup"><span data-stu-id="da108-191">This is required by the `using` statement.</span></span>

### <a name="about-variables-in-q"></a><span data-ttu-id="da108-192">Sobre as variáveis em Q#</span><span class="sxs-lookup"><span data-stu-id="da108-192">About variables in Q#</span></span>

<span data-ttu-id="da108-193">Por padrão, as variáveis em Q# são imutáveis; o valor delas não pode ser alterado depois que elas são associadas.</span><span class="sxs-lookup"><span data-stu-id="da108-193">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="da108-194">A palavra-chave `let` é usada para indicar a associação de uma variável imutável.</span><span class="sxs-lookup"><span data-stu-id="da108-194">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="da108-195">Os argumentos da operação são sempre imutáveis.</span><span class="sxs-lookup"><span data-stu-id="da108-195">Operation arguments are always immutable.</span></span>

<span data-ttu-id="da108-196">Caso precise de uma variável cujo valor possa ser alterado, como `numOnes` no exemplo, você poderá declarar a variável com a palavra-chave `mutable`.</span><span class="sxs-lookup"><span data-stu-id="da108-196">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="da108-197">O valor de uma variável mutável pode ser alterado usando uma instrução `set`.</span><span class="sxs-lookup"><span data-stu-id="da108-197">A mutable variable's value may be changed using a `set` statement.</span></span>

<span data-ttu-id="da108-198">Em ambos os casos, o tipo de uma variável é inferido pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="da108-198">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="da108-199">O Q# não exige nenhuma anotação de tipo para variáveis.</span><span class="sxs-lookup"><span data-stu-id="da108-199">Q# doesn't require any type annotations for variables.</span></span>

### <a name="about-using-statements-in-q"></a><span data-ttu-id="da108-200">Sobre as instruções `using` em Q#</span><span class="sxs-lookup"><span data-stu-id="da108-200">About `using` statements in Q#</span></span>

<span data-ttu-id="da108-201">A instrução `using` também é especial para o Q#.</span><span class="sxs-lookup"><span data-stu-id="da108-201">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="da108-202">Ela é usada para alocar qubits para uso em um bloco de código.</span><span class="sxs-lookup"><span data-stu-id="da108-202">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="da108-203">Em Q#, todos os qubits são alocados e liberados dinamicamente, em vez de serem recursos fixos que existem pelo tempo de vida inteiro de um algoritmo complexo.</span><span class="sxs-lookup"><span data-stu-id="da108-203">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="da108-204">Uma instrução `using` aloca um conjunto de qubits no início e libera esses qubits no final do bloco.</span><span class="sxs-lookup"><span data-stu-id="da108-204">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="create-the-host-application-code"></a><span data-ttu-id="da108-205">Criar o código do aplicativo host</span><span class="sxs-lookup"><span data-stu-id="da108-205">Create the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="da108-206">Python</span><span class="sxs-lookup"><span data-stu-id="da108-206">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="da108-207">Abra o arquivo `host.py`e adicione o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="da108-207">Open the `host.py` file and add the following code:</span></span>

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[<span data-ttu-id="da108-208">C#</span><span class="sxs-lookup"><span data-stu-id="da108-208">C#</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="da108-209">Substitua o conteúdo do arquivo `Driver.cs` pelo seguinte código:</span><span class="sxs-lookup"><span data-stu-id="da108-209">Replace the contents of the `Driver.cs` file with the following code:</span></span>

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a><span data-ttu-id="da108-210">Sobre o código do aplicativo host</span><span class="sxs-lookup"><span data-stu-id="da108-210">About the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="da108-211">Python</span><span class="sxs-lookup"><span data-stu-id="da108-211">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="da108-212">O aplicativo host do Python tem três partes:</span><span class="sxs-lookup"><span data-stu-id="da108-212">The Python host application has three parts:</span></span>

* <span data-ttu-id="da108-213">Calcula os argumentos necessários para o algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-213">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="da108-214">No exemplo, `count` é corrigido em um 1.000 e `initial` é o valor inicial do qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-214">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="da108-215">Executa o algoritmo quântico chamando o método `simulate()` da operação Q# importada.</span><span class="sxs-lookup"><span data-stu-id="da108-215">Run the quantum algorithm by calling the `simulate()` method of the imported Q# operation.</span></span>
* <span data-ttu-id="da108-216">Processa o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="da108-216">Process the result of the operation.</span></span> <span data-ttu-id="da108-217">No exemplo, `res` recebe o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="da108-217">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="da108-218">Aqui, o resultado é uma tupla do número de zeros (`num_zeros`) e do número de uns (`num_ones`) medidos pelo simulador.</span><span class="sxs-lookup"><span data-stu-id="da108-218">Here the result is a tuple of the number of zeros (`num_zeros`) and number of ones (`num_ones`) measured by the simulator.</span></span> <span data-ttu-id="da108-219">Desconstruiremos a tupla para obter os dois campos e imprimiremos os resultados.</span><span class="sxs-lookup"><span data-stu-id="da108-219">We deconstruct the tuple to get the two fields, and print the results.</span></span>

#### <a name="c"></a>[<span data-ttu-id="da108-220">C#</span><span class="sxs-lookup"><span data-stu-id="da108-220">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="da108-221">O aplicativo host C# tem quatro partes:</span><span class="sxs-lookup"><span data-stu-id="da108-221">The C# host application has four parts:</span></span>

* <span data-ttu-id="da108-222">Constrói um simulador quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-222">Construct a quantum simulator.</span></span> <span data-ttu-id="da108-223">No exemplo, `qsim` é o simulador.</span><span class="sxs-lookup"><span data-stu-id="da108-223">In the example, `qsim` is the simulator.</span></span>
* <span data-ttu-id="da108-224">Calcula os argumentos necessários para o algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-224">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="da108-225">No exemplo, `count` é corrigido em um 1.000 e `initial` é o valor inicial do qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-225">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="da108-226">Executa o algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-226">Run the quantum algorithm.</span></span> <span data-ttu-id="da108-227">Cada operação Q# gera uma classe C# com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="da108-227">Each Q# operation generates a C# class with the same name.</span></span> <span data-ttu-id="da108-228">Essa classe tem um método `Run` que executa a operação de **maneira assíncrona**.</span><span class="sxs-lookup"><span data-stu-id="da108-228">This class has a `Run` method that **asynchronously** executes the operation.</span></span> <span data-ttu-id="da108-229">A execução é assíncrona, porque a execução no hardware real será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="da108-229">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> <span data-ttu-id="da108-230">Como o método `Run` é assíncrono, efetuamos fetch da propriedade `Result`; isso bloqueia a execução até que a tarefa seja concluída e retorna o resultado de maneira síncrona.</span><span class="sxs-lookup"><span data-stu-id="da108-230">Because the `Run` method is asynchronous, we fetch the `Result` property; this blocks execution until the task completes and returns the result synchronously.</span></span>
* <span data-ttu-id="da108-231">Processa o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="da108-231">Process the result of the operation.</span></span> <span data-ttu-id="da108-232">No exemplo, `res` recebe o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="da108-232">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="da108-233">Aqui, o resultado é uma tupla do número de zeros (`numZeros`) e do número de uns (`numOnes`) medidos pelo simulador.</span><span class="sxs-lookup"><span data-stu-id="da108-233">Here the result is a tuple of the number of zeros (`numZeros`) and number of ones (`numOnes`) measured by the simulator.</span></span> <span data-ttu-id="da108-234">Isso é retornado como uma ValueTuple em C#.</span><span class="sxs-lookup"><span data-stu-id="da108-234">This is returned as a ValueTuple in C#.</span></span> <span data-ttu-id="da108-235">Desconstruiremos a tupla para obter os dois campos, imprimiremos os resultados e aguardaremos um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="da108-235">We deconstruct the tuple to get the two fields, print the results, and wait for a keypress.</span></span>

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a><span data-ttu-id="da108-236">Criar e executar</span><span class="sxs-lookup"><span data-stu-id="da108-236">Build and run</span></span>

#### <a name="python"></a>[<span data-ttu-id="da108-237">Python</span><span class="sxs-lookup"><span data-stu-id="da108-237">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="da108-238">Execute o seguinte comando no terminal:</span><span class="sxs-lookup"><span data-stu-id="da108-238">Run the following command at your terminal:</span></span>

    ```
    python host.py
    ```

    <span data-ttu-id="da108-239">Esse comando executa o aplicativo host, que simula a operação Q#.</span><span class="sxs-lookup"><span data-stu-id="da108-239">This command runs the host application, which simulates the Q# operation.</span></span>

<span data-ttu-id="da108-240">Os resultados devem ser:</span><span class="sxs-lookup"><span data-stu-id="da108-240">The results should be:</span></span>

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="da108-241">Linha de comando/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="da108-241">Command Line / Visual Studio Code</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="da108-242">Execute o seguinte no terminal:</span><span class="sxs-lookup"><span data-stu-id="da108-242">Run the following at your terminal:</span></span>

    ```dotnetcli
    dotnet run
    ```

    <span data-ttu-id="da108-243">Esse comando baixará automaticamente todos os pacotes necessários, compilará o aplicativo e, em seguida, o executará na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="da108-243">This command will automatically download all required packages, build the application, then run it at the command line.</span></span>

1. <span data-ttu-id="da108-244">Como alternativa, pressione **F1** para abrir a paleta de comandos e selecione **Depurar: Iniciar sem Depuração.**</span><span class="sxs-lookup"><span data-stu-id="da108-244">Alternatively, press **F1** to open the Command Palette and select **Debug: Start Without Debugging.**</span></span>
<span data-ttu-id="da108-245">Talvez você precise criar um arquivo ``launch.json`` descrevendo como iniciar o programa.</span><span class="sxs-lookup"><span data-stu-id="da108-245">You may be prompted to create a new ``launch.json`` file describing how to start the program.</span></span>
<span data-ttu-id="da108-246">O ``launch.json`` padrão deve funcionar bem para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="da108-246">The default ``launch.json`` should work well for most applications.</span></span>

<span data-ttu-id="da108-247">Os resultados devem ser:</span><span class="sxs-lookup"><span data-stu-id="da108-247">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[<span data-ttu-id="da108-248">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da108-248">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="da108-249">Basta clicar em `F5` e o programa deverá ser compilado e executado.</span><span class="sxs-lookup"><span data-stu-id="da108-249">Just hit `F5`, and your program should build and run!</span></span>

<span data-ttu-id="da108-250">Os resultados devem ser:</span><span class="sxs-lookup"><span data-stu-id="da108-250">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

<span data-ttu-id="da108-251">O programa será encerrado depois que você pressionar uma tecla.</span><span class="sxs-lookup"><span data-stu-id="da108-251">The program will exit after you press a key.</span></span>

* * *

## <a name="prepare-superposition"></a><span data-ttu-id="da108-252">Preparar a superposição</span><span class="sxs-lookup"><span data-stu-id="da108-252">Prepare superposition</span></span>

<span data-ttu-id="da108-253">**Visão geral** Agora vamos examinar como o Q# expressa maneiras de colocar qubits em sobreposição.</span><span class="sxs-lookup"><span data-stu-id="da108-253">**Overview** Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="da108-254">Lembre-se de que o estado de um qubit pode estar em uma sobreposição de 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="da108-254">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="da108-255">Usaremos a operação `Hadamard` para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="da108-255">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="da108-256">Se o qubit estiver em qualquer um dos estados clássicos (em que uma medição retorna `Zero` sempre ou `One` sempre), a operação `Hadamard` ou `H` colocará o qubit em um estado em que uma medição do qubit retornará `Zero` 50% do tempo e retornará `One` 50% do tempo.</span><span class="sxs-lookup"><span data-stu-id="da108-256">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="da108-257">Conceitualmente, o qubit pode ser pensado como a metade entre o `Zero` e o `One`.</span><span class="sxs-lookup"><span data-stu-id="da108-257">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="da108-258">Agora, quando simularmos a operação `TestBellState`, veremos que os resultados retornarão aproximadamente um número igual de `Zero` e `One` após a medição.</span><span class="sxs-lookup"><span data-stu-id="da108-258">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

<span data-ttu-id="da108-259">Primeiro, tentaremos inverter o qubit (se o qubit estiver no `Zero`, o estado será invertido para `One` e vice-versa).</span><span class="sxs-lookup"><span data-stu-id="da108-259">First we'll just try to flip the qubit (if the qubit is in `Zero` state will flip to `One` and vice versa).</span></span> <span data-ttu-id="da108-260">Isso é feito com a execução de uma operação `X` antes de medi-lo em `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="da108-260">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="da108-261">Agora os resultados (depois de pressionar `F5`) são invertidos:</span><span class="sxs-lookup"><span data-stu-id="da108-261">Now the results (after pressing `F5`) are reversed:</span></span>

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

<span data-ttu-id="da108-262">No entanto, tudo o que vimos até agora é clássico.</span><span class="sxs-lookup"><span data-stu-id="da108-262">However, everything we've seen so far is classical.</span></span> <span data-ttu-id="da108-263">Vamos obter um resultado quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-263">Let's get a quantum result.</span></span> <span data-ttu-id="da108-264">Basta substituir a operação `X` na execução anterior por uma operação `H` ou Hadamard.</span><span class="sxs-lookup"><span data-stu-id="da108-264">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="da108-265">Em vez de inverteremos o qubit até o final de 0 a 1, só o inverteremos até a metade.</span><span class="sxs-lookup"><span data-stu-id="da108-265">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="da108-266">As linhas substituídas em `TestBellState` agora têm a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="da108-266">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="da108-267">Agora os resultados ficam mais interessantes:</span><span class="sxs-lookup"><span data-stu-id="da108-267">Now the results get more interesting:</span></span>

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

<span data-ttu-id="da108-268">Sempre que medimos, pedimos um valor clássico, mas como o qubit está na metade entre 0 e 1, obtemos (estatisticamente) 0 na metade do tempo e 1 na metade do tempo.</span><span class="sxs-lookup"><span data-stu-id="da108-268">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span> <span data-ttu-id="da108-269">Isso é conhecido como __superposição__ e nos dá nossa primeira visão real de um estado quântico.</span><span class="sxs-lookup"><span data-stu-id="da108-269">This is known as __superposition__ and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="da108-270">Preparar o entrelaçamento</span><span class="sxs-lookup"><span data-stu-id="da108-270">Prepare entanglement</span></span>

<span data-ttu-id="da108-271">**Visão geral:**  Agora vamos examinar como o Q# expressa maneiras de entrelaçar qubits.</span><span class="sxs-lookup"><span data-stu-id="da108-271">**Overview:**  Now let’s look at how Q# expresses ways to entangle qubits.</span></span>  <span data-ttu-id="da108-272">Primeiro, definimos o primeiro qubit como o estado inicial e usamos a operação `H` para colocá-lo em sobreposição.</span><span class="sxs-lookup"><span data-stu-id="da108-272">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="da108-273">Em seguida, antes de medirmos o primeiro qubit, usamos uma nova operação (`CNOT`), que significa Não-Controlada.</span><span class="sxs-lookup"><span data-stu-id="da108-273">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for Controlled-Not.</span></span>  <span data-ttu-id="da108-274">O resultado da execução dessa operação em dois qubits será inverter o segundo qubit se o primeiro qubit for `One`.</span><span class="sxs-lookup"><span data-stu-id="da108-274">The result of executing this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="da108-275">Agora, os dois qubits estão entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="da108-275">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="da108-276">Nossas estatísticas para o primeiro qubit não mudaram (possibilidade de 50-50 de `Zero` ou `One` após a medição), mas agora, quando medimos o segundo qubit, ele é __sempre__ igual ao que medimos para o primeiro qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-276">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="da108-277">Nosso `CNOT` entrelaçou os dois qubits, de modo que o que acontecer com um deles acontecerá com o outro.</span><span class="sxs-lookup"><span data-stu-id="da108-277">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="da108-278">Se você inverter as medidas (fizer o segundo qubit antes do primeiro), a mesma coisa acontecerá.</span><span class="sxs-lookup"><span data-stu-id="da108-278">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="da108-279">A primeira medida será aleatória e a segunda estará na etapa de bloqueio com tudo o que foi descoberto para o primeiro.</span><span class="sxs-lookup"><span data-stu-id="da108-279">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="da108-280">A primeira coisa que precisaremos fazer é alocar dois qubits em vez de um em `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="da108-280">The first thing we'll need to do is allocate 2 qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="da108-281">Isso nos permitirá adicionar uma nova operação (`CNOT`) antes de medir (`M`) em `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="da108-281">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="da108-282">Adicionamos outra operação `Set` para inicializar o primeiro qubit, a fim de garantir que ele esteja sempre no estado `Zero` quando começarmos.</span><span class="sxs-lookup"><span data-stu-id="da108-282">We've added another `Set` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="da108-283">Também precisamos redefinir o segundo qubit antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="da108-283">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

<span data-ttu-id="da108-284">A rotina completa agora tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="da108-284">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="da108-285">Se executarmos isso, obteremos exatamente o mesmo resultado 50-50 que obtivemos antes.</span><span class="sxs-lookup"><span data-stu-id="da108-285">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="da108-286">No entanto, estamos interessados mesmo em como o segundo qubit reage ao primeiro que está sendo medido.</span><span class="sxs-lookup"><span data-stu-id="da108-286">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="da108-287">Adicionaremos essa estatística com uma nova versão da operação `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="da108-287">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set(initial, q0);
                Set(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="da108-288">O novo valor retornado (`agree`) faz o acompanhamento toda vez que a medida do primeiro qubit corresponde à medida do segundo qubit.</span><span class="sxs-lookup"><span data-stu-id="da108-288">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span> <span data-ttu-id="da108-289">Também precisamos atualizar o aplicativo host de acordo:</span><span class="sxs-lookup"><span data-stu-id="da108-289">We also have to update the host application accordingly:</span></span>

#### <a name="python"></a>[<span data-ttu-id="da108-290">Python</span><span class="sxs-lookup"><span data-stu-id="da108-290">Python</span></span>](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[<span data-ttu-id="da108-291">C#</span><span class="sxs-lookup"><span data-stu-id="da108-291">C#</span></span>](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

<span data-ttu-id="da108-292">Agora, na execução, obtemos algo incrível:</span><span class="sxs-lookup"><span data-stu-id="da108-292">Now when we run, we get something pretty amazing:</span></span>

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

<span data-ttu-id="da108-293">Conforme indicado na visão geral, nossas estatísticas para o primeiro qubit não foram alteradas (possibilidade de 50-50 de 0 ou 1), mas agora, quando medimos o segundo qubit, ele é __sempre__ igual ao que medimos para o primeiro qubit, porque eles estão entrelaçados!</span><span class="sxs-lookup"><span data-stu-id="da108-293">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

<span data-ttu-id="da108-294">Parabéns, você escreveu seu primeiro programa quântico!</span><span class="sxs-lookup"><span data-stu-id="da108-294">Congratulations, you've written your first quantum program!</span></span>

## <a name="next-steps"></a><span data-ttu-id="da108-295">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="da108-295">Next steps</span></span>

<span data-ttu-id="da108-296">O tutorial [Pesquisa de Grover](xref:microsoft.quantum.quickstarts.search) mostrará como criar e executar a pesquisa de Grover, um dos algoritmos mais populares da computação quântica, além de apresentar um bom exemplo de programa Q# que pode ser usado para resolver problemas reais com a computação quântica.</span><span class="sxs-lookup"><span data-stu-id="da108-296">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="da108-297">A [Introdução ao Quantum Development Kit](xref:microsoft.quantum.welcome) recomenda mais maneiras de aprender o Q# e a programação quântica.</span><span class="sxs-lookup"><span data-stu-id="da108-297">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>
