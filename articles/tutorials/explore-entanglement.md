---
title: Explore o Entanglement com Q#
description: Saiba como escrever um programa Quantum no Q# . Desenvolver um aplicativo de Estado de Bell usando o QDK (Quantum development kit)
author: geduardo
ms.author: v-edsanc
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
no-loc:
- Q#
- $$v
ms.openlocfilehash: ac9c060c157ba5ee3bc66852c42298ac8adcb3b3
ms.sourcegitcommit: 685a8ab16d7e6a25e63a168d6e7c385fa6e876cc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/29/2020
ms.locfileid: "91492329"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="24d46-104">Tutorial: Explorar o emaranhamento com o Q\#</span><span class="sxs-lookup"><span data-stu-id="24d46-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="24d46-105">Neste tutorial, mostramos como escrever um Q# programa que manipula e mede o qubits e demonstra os efeitos de superposição e Entanglement.</span><span class="sxs-lookup"><span data-stu-id="24d46-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>

<span data-ttu-id="24d46-106">Você escreverá um aplicativo chamado Bell para demonstrar o entrelaçamento quântico.</span><span class="sxs-lookup"><span data-stu-id="24d46-106">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="24d46-107">O nome Bell foi criado em referência aos estados Bell, que são estados quânticos específicos de dois qubits usados para representar os exemplos mais simples de sobreposição e entrelaçamento quântico.</span><span class="sxs-lookup"><span data-stu-id="24d46-107">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="24d46-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="24d46-108">Pre-requisites</span></span>

<span data-ttu-id="24d46-109">Se estiver pronto para começar a codificação, siga estas etapas antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="24d46-109">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="24d46-110">[Instale](xref:microsoft.quantum.install) o kit de desenvolvimento Quantum usando o ambiente de desenvolvimento e a linguagem preferencial.</span><span class="sxs-lookup"><span data-stu-id="24d46-110">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your  preferred language and development environment.</span></span>
* <span data-ttu-id="24d46-111">Caso já tenha o QDK instalado, verifique se você o [atualizou](xref:microsoft.quantum.update) para a última versão</span><span class="sxs-lookup"><span data-stu-id="24d46-111">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="24d46-112">Você também pode acompanhar a narração sem instalar o QDK, revisando as visões gerais da Q# linguagem de programação e os primeiros conceitos da computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="24d46-112">You can also follow along with the narrative without installing the QDK, reviewing  the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="24d46-113">Neste tutorial, você aprenderá como:</span><span class="sxs-lookup"><span data-stu-id="24d46-113">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="24d46-114">Criar e combinar operações em p\#</span><span class="sxs-lookup"><span data-stu-id="24d46-114">Create and combine operations in Q\#</span></span>
> * <span data-ttu-id="24d46-115">Crie operações para colocar qubits em superposição, entangle e meça-las.</span><span class="sxs-lookup"><span data-stu-id="24d46-115">Create operations to put qubits in superposition, entangle and measure them.</span></span>
> * <span data-ttu-id="24d46-116">Demonstre o Quantum Entanglement com um Q# programa executado em um simulador.</span><span class="sxs-lookup"><span data-stu-id="24d46-116">Demonstrate quantum entanglement with a Q# program run in a simulator.</span></span> 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a><span data-ttu-id="24d46-117">Demonstrando o comportamento do qubit com o QDK</span><span class="sxs-lookup"><span data-stu-id="24d46-117">Demonstrating qubit behavior with the QDK</span></span>

<span data-ttu-id="24d46-118">Onde os bits clássicos contêm apenas um valor binário, como 0 ou 1, o estado de um [qubit](xref:microsoft.quantum.glossary#qubit) pode estar em uma **sobreposição** de 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="24d46-118">Where classical bits hold a single binary value such as a 0 or 1, the state of a [qubit](xref:microsoft.quantum.glossary#qubit) can be in a **superposition** of 0 and 1.</span></span>  <span data-ttu-id="24d46-119">Conceitualmente, o estado de um qubit pode ser pensado como uma direção em um espaço abstrato (também conhecido como um vetor).</span><span class="sxs-lookup"><span data-stu-id="24d46-119">Conceptually, the state of a qubit can be thought of as a direction in an abstract space (also known as a vector).</span></span>  <span data-ttu-id="24d46-120">Um estado qubit pode estar em qualquer uma das possíveis direções.</span><span class="sxs-lookup"><span data-stu-id="24d46-120">A qubit state can be in any of the possible directions.</span></span> <span data-ttu-id="24d46-121">Os dois **estados clássicos** são as duas direções, que representam 100% de chance de medir 0 e 100% de chance de medir 1.</span><span class="sxs-lookup"><span data-stu-id="24d46-121">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>

<span data-ttu-id="24d46-122">O ato de medição produz um resultado binário e altera um estado do qubit.</span><span class="sxs-lookup"><span data-stu-id="24d46-122">The act of measurement produces a binary result and changes a qubit state.</span></span>
<span data-ttu-id="24d46-123">A medida produz um valor binário, 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="24d46-123">Measurement  produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="24d46-124">O qubit passa de estar em sobreposição (qualquer direção) para um dos estados clássicos.</span><span class="sxs-lookup"><span data-stu-id="24d46-124">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="24d46-125">Depois disso, repetir a mesma medição sem nenhuma operação intermediária produz o mesmo resultado binário.</span><span class="sxs-lookup"><span data-stu-id="24d46-125">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="24d46-126">Vários qubits podem ser [**entrelaçados**](xref:microsoft.quantum.glossary#entanglement).</span><span class="sxs-lookup"><span data-stu-id="24d46-126">Multiple qubits can be [**entangled**](xref:microsoft.quantum.glossary#entanglement).</span></span>  <span data-ttu-id="24d46-127">Quando fazemos uma medição de um qubit entrelaçado, nosso conhecimento do estado dos outros é atualizado também.</span><span class="sxs-lookup"><span data-stu-id="24d46-127">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="24d46-128">Agora, estamos prontos para demonstrar como Q# o expressa esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="24d46-128">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="24d46-129">Você começará com o programa mais simples possível e o desenvolverá para demonstrar a sobreposição quântica e o entrelaçamento quântico.</span><span class="sxs-lookup"><span data-stu-id="24d46-129">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="creating-a-no-locq-project"></a><span data-ttu-id="24d46-130">Criando um Q# projeto</span><span class="sxs-lookup"><span data-stu-id="24d46-130">Creating a Q# project</span></span>

<span data-ttu-id="24d46-131">A primeira coisa que precisamos fazer é criar um novo Q# projeto.</span><span class="sxs-lookup"><span data-stu-id="24d46-131">The first thing we have to do is to create a new Q# project.</span></span> <span data-ttu-id="24d46-132">Neste tutorial, vamos usar o ambiente baseado em [ Q# aplicativos com vs Code](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="24d46-132">In this tutorial we are going to use the environment based on [Q# applications with VS Code](xref:microsoft.quantum.install.standalone).</span></span>

<span data-ttu-id="24d46-133">Para criar um novo projeto, no VS Code:</span><span class="sxs-lookup"><span data-stu-id="24d46-133">To create a new project, in VS Code:</span></span> 

1. <span data-ttu-id="24d46-134">Clique em **Exibir** -> **Paleta de Comandos** e selecione **Q#: Criar Novo Projeto**.</span><span class="sxs-lookup"><span data-stu-id="24d46-134">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="24d46-135">Clique em **Aplicativo de console autônomo**.</span><span class="sxs-lookup"><span data-stu-id="24d46-135">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="24d46-136">Navegue até o local para salvar o projeto e clique em **Criar Projeto**.</span><span class="sxs-lookup"><span data-stu-id="24d46-136">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="24d46-137">Quando o projeto for criado com êxito, clique em **Abrir novo projeto...** no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="24d46-137">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="24d46-138">Nesse caso, chamamos o projeto `Bell` .</span><span class="sxs-lookup"><span data-stu-id="24d46-138">In this case we called the project `Bell`.</span></span> <span data-ttu-id="24d46-139">Isso gera dois arquivos: `Bell.csproj` , o arquivo de projeto e `Program.qs` um modelo de um Q# aplicativo que usaremos para escrever nosso aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24d46-139">This generates two files: `Bell.csproj`, the project file and `Program.qs`, a template of a Q# application that we will use to write our application.</span></span> <span data-ttu-id="24d46-140">O conteúdo de `Program.qs` deve ser:</span><span class="sxs-lookup"><span data-stu-id="24d46-140">The content of `Program.qs` should be:</span></span>

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a><span data-ttu-id="24d46-141">Escrever o \# aplicativo Q</span><span class="sxs-lookup"><span data-stu-id="24d46-141">Write the Q\# application</span></span>
 
<span data-ttu-id="24d46-142">Nosso objetivo é preparar dois qubits em um estado de Quantum específico, demonstrando como operar em qubits com Q# o para alterar seu estado e demonstrar os efeitos de superposição e Entanglement.</span><span class="sxs-lookup"><span data-stu-id="24d46-142">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="24d46-143">Criaremos essa peça por parte para apresentar os Estados, as operações e a medição do qubit.</span><span class="sxs-lookup"><span data-stu-id="24d46-143">We will build this up piece by piece to introduce qubit states, operations, and measurement.</span></span>

### <a name="initialize-qubit-using-measurement"></a><span data-ttu-id="24d46-144">Inicializar qubit usando medição</span><span class="sxs-lookup"><span data-stu-id="24d46-144">Initialize qubit using measurement</span></span>

<span data-ttu-id="24d46-145">No primeiro trecho de código abaixo, mostramos como trabalhar com o qubits no Q# .</span><span class="sxs-lookup"><span data-stu-id="24d46-145">In the first code snippet below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="24d46-146">Apresentaremos duas operações [`M`](xref:microsoft.quantum.intrinsic.m) e [`X`](xref:microsoft.quantum.intrinsic.x) transformaremos o estado de um qubit.</span><span class="sxs-lookup"><span data-stu-id="24d46-146">We’ll introduce two operations, [`M`](xref:microsoft.quantum.intrinsic.m) and [`X`](xref:microsoft.quantum.intrinsic.x) that transform the state of a qubit.</span></span> <span data-ttu-id="24d46-147">Neste snippet de código, uma operação `SetQubitState` é definida que usa como parâmetro um qubit e outro parâmetro, `desired`, que representa o estado no qual gostaríamos que o qubit estivesse.</span><span class="sxs-lookup"><span data-stu-id="24d46-147">In this code snippet, an operation `SetQubitState` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="24d46-148">A operação `SetQubitState` executa uma medida no qubit usando a operação `M`.</span><span class="sxs-lookup"><span data-stu-id="24d46-148">The operation `SetQubitState` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="24d46-149">No Q# , uma medida qubit sempre retorna um `Zero` ou `One` .</span><span class="sxs-lookup"><span data-stu-id="24d46-149">In Q#, a qubit measurement always returns either `Zero` or `One`.</span></span>  <span data-ttu-id="24d46-150">Se a medida retornar um valor diferente do valor desejado, `SetQubitState` "inverte" o qubit; ou seja, ele executa uma `X` operação, que altera o estado de qubit para um novo estado no qual as probabilidades de uma medida retornam `Zero` e `One` são revertidas.</span><span class="sxs-lookup"><span data-stu-id="24d46-150">If the measurement returns a value not equal to the desired value, `SetQubitState` “flips” the qubit; that is, it runs an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span> <span data-ttu-id="24d46-151">Dessa forma, `SetQubitState` o sempre coloca o destino qubit no estado desejado.</span><span class="sxs-lookup"><span data-stu-id="24d46-151">This way, `SetQubitState` always puts the target qubit in the desired state.</span></span>

<span data-ttu-id="24d46-152">Substitua o conteúdo de `Program.qs` pelo código a seguir:</span><span class="sxs-lookup"><span data-stu-id="24d46-152">Replace the contents of `Program.qs` with the following code:</span></span>


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

<span data-ttu-id="24d46-153">Esta operação agora pode ser chamada para definir um qubit como um estado clássico, retornando `Zero` 100% do tempo ou retornando `One` 100% do tempo.</span><span class="sxs-lookup"><span data-stu-id="24d46-153">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>
<span data-ttu-id="24d46-154">`Zero` e `One` são constantes que representam os únicos dois possíveis resultados de uma medição de um qubit.</span><span class="sxs-lookup"><span data-stu-id="24d46-154">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

<span data-ttu-id="24d46-155">A operação `SetQubitState` mede o qubit.</span><span class="sxs-lookup"><span data-stu-id="24d46-155">The operation `SetQubitState` measures the qubit.</span></span> <span data-ttu-id="24d46-156">Se o qubit estiver no estado desejado, `SetQubitState` deixará-o sozinho; caso contrário, executando a `X` operação, alteraremos o estado de qubit para o estado desejado.</span><span class="sxs-lookup"><span data-stu-id="24d46-156">If the qubit is in the state we want, `SetQubitState` leaves it alone; otherwise, by running the `X` operation, we change the qubit state to the desired state.</span></span>

#### <a name="about-no-locq-operations"></a><span data-ttu-id="24d46-157">Sobre Q# as operações</span><span class="sxs-lookup"><span data-stu-id="24d46-157">About Q# operations</span></span>

<span data-ttu-id="24d46-158">Uma Q# operação é uma sub-rotina Quantum.</span><span class="sxs-lookup"><span data-stu-id="24d46-158">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="24d46-159">Ou seja, é uma rotina que possa ser chamada que contém chamadas para outras operações de Quantum.</span><span class="sxs-lookup"><span data-stu-id="24d46-159">That is, it is a callable routine that contains calls to other quantum operations.</span></span>

<span data-ttu-id="24d46-160">Os argumentos de uma operação são especificados como uma tupla, entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="24d46-160">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="24d46-161">O tipo de retorno da operação é especificado após dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="24d46-161">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="24d46-162">Nesse caso, a `SetQubitState` operação não tem nenhum tipo de retorno, portanto, ela está marcada como retornando `Unit` .</span><span class="sxs-lookup"><span data-stu-id="24d46-162">In this case, the `SetQubitState` operation has no return type, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="24d46-163">Esse é o Q# equivalente de `unit` em F #, que é basicamente análogo a `void` em C# e uma tupla vazia em Python ( `()` , representada pela dica de tipo `Tuple[()]` ).</span><span class="sxs-lookup"><span data-stu-id="24d46-163">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple in Python (`()`, represented by the type hint `Tuple[()]`).</span></span>

<span data-ttu-id="24d46-164">Você usou duas operações Quantum em sua primeira Q# operação:</span><span class="sxs-lookup"><span data-stu-id="24d46-164">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="24d46-165">A [`M`](xref:microsoft.quantum.intrinsic.m) operação, que mede o estado do qubit</span><span class="sxs-lookup"><span data-stu-id="24d46-165">The [`M`](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="24d46-166">A [`X`](xref:microsoft.quantum.intrinsic.x) operação, que inverte o estado de um qubit</span><span class="sxs-lookup"><span data-stu-id="24d46-166">The [`X`](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="24d46-167">Uma operação quântica transforma o estado de um qubit.</span><span class="sxs-lookup"><span data-stu-id="24d46-167">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="24d46-168">Algumas vezes, as pessoas falam sobre portões quânticos em vez de operações, em analogia a portões lógicos clássicos.</span><span class="sxs-lookup"><span data-stu-id="24d46-168">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="24d46-169">Isso está enraizado nos primórdios da computação quântica, quando os algoritmos eram meramente um constructo teórico e eram visualizados como diagramas de forma semelhante à dos diagramas de circuito na computação clássica.</span><span class="sxs-lookup"><span data-stu-id="24d46-169">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="counting-measurement-outcomes"></a><span data-ttu-id="24d46-170">Resultados da medição de contagem</span><span class="sxs-lookup"><span data-stu-id="24d46-170">Counting measurement outcomes</span></span>

<span data-ttu-id="24d46-171">Para demonstrar o efeito da operação `SetQubitState`, uma operação `TestBellState` é adicionada.</span><span class="sxs-lookup"><span data-stu-id="24d46-171">To demonstrate the effect of the `SetQubitState` operation, a `TestBellState` operation is then added.</span></span> <span data-ttu-id="24d46-172">Essa operação aceita como entrada um `Zero` ou `One` e chama a operação `SetQubitState` algum número de vezes com essa entrada, além de contar o número de vezes que `Zero` foi retornado da medição do qubit e do número de vezes que `One` foi retornado.</span><span class="sxs-lookup"><span data-stu-id="24d46-172">This operation takes as input a `Zero` or `One`, and calls the `SetQubitState` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="24d46-173">É claro que, nesta primeira simulação da operação `TestBellState`, esperamos que a saída mostre que todas as medições do conjunto de qubits com `Zero` como a entrada do parâmetro retornarão `Zero` e todas as medições de um conjunto de qubits com `One` como a entrada do parâmetro retornarão `One`.</span><span class="sxs-lookup"><span data-stu-id="24d46-173">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span> <span data-ttu-id="24d46-174">Além disso, adicionaremos o código para `TestBellState` demonstrar a superposição e Entanglement.</span><span class="sxs-lookup"><span data-stu-id="24d46-174">Further on, we’ll add code to `TestBellState` to demonstrate superposition and entanglement.</span></span>

<span data-ttu-id="24d46-175">Adicione a seguinte operação ao arquivo `Program.qs`, dentro do namespace, após o final da operação `SetQubitState`:</span><span class="sxs-lookup"><span data-stu-id="24d46-175">Add the following operation to the `Program.qs` file, inside the namespace, after the end of the `SetQubitState` operation:</span></span>

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
<span data-ttu-id="24d46-176">Observe que adicionamos uma linha antes do `return` para imprimir uma mensagem explicativa no console com a função ( `Message` ) [Microsoft. Quantum. intrínseca. Message]</span><span class="sxs-lookup"><span data-stu-id="24d46-176">Note that we added a line before the `return` to print an explanatory message in the console with the function (`Message`)[microsoft.quantum.intrinsic.message]</span></span>

<span data-ttu-id="24d46-177">Essa operação (`TestBellState`) executará um loop para iterações `count`, definirá um valor `initial` especificado em um qubit e, em seguida, medirá (`M`) o resultado.</span><span class="sxs-lookup"><span data-stu-id="24d46-177">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="24d46-178">Ela coletará estatísticas sobre quantos zeros e aqueles medidos e os retornará ao chamador.</span><span class="sxs-lookup"><span data-stu-id="24d46-178">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="24d46-179">Ela executa outra operação necessária.</span><span class="sxs-lookup"><span data-stu-id="24d46-179">It performs one other necessary operation.</span></span> <span data-ttu-id="24d46-180">Ela redefine o qubit para um estado conhecido (`Zero`) antes de retorná-lo, permitindo que outras pessoas aloquem esse qubit em um estado conhecido.</span><span class="sxs-lookup"><span data-stu-id="24d46-180">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="24d46-181">Isso é exigido pela instrução `using`.</span><span class="sxs-lookup"><span data-stu-id="24d46-181">This is required by the `using` statement.</span></span>

#### <a name="about-variables-in-q"></a><span data-ttu-id="24d46-182">Sobre variáveis em Q\#</span><span class="sxs-lookup"><span data-stu-id="24d46-182">About variables in Q\#</span></span>

<span data-ttu-id="24d46-183">Por padrão, as variáveis no Q# são imutáveis; seu valor não pode ser alterado depois que elas são associadas.</span><span class="sxs-lookup"><span data-stu-id="24d46-183">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="24d46-184">A palavra-chave `let` é usada para indicar a associação de uma variável imutável.</span><span class="sxs-lookup"><span data-stu-id="24d46-184">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="24d46-185">Os argumentos da operação são sempre imutáveis.</span><span class="sxs-lookup"><span data-stu-id="24d46-185">Operation arguments are always immutable.</span></span>

<span data-ttu-id="24d46-186">Caso precise de uma variável cujo valor possa ser alterado, como `numOnes` no exemplo, você poderá declarar a variável com a palavra-chave `mutable`.</span><span class="sxs-lookup"><span data-stu-id="24d46-186">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="24d46-187">O valor de uma variável mutável pode ser alterado usando uma instrução `set`.</span><span class="sxs-lookup"><span data-stu-id="24d46-187">A mutable variable's value may be changed using a `set` statement.</span></span>

<span data-ttu-id="24d46-188">Em ambos os casos, o tipo de uma variável é inferido pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="24d46-188">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="24d46-189">Q# Não requer nenhuma anotação de tipo para variáveis.</span><span class="sxs-lookup"><span data-stu-id="24d46-189">Q# doesn't require any type annotations for variables.</span></span>

#### <a name="about-using-statements-in-q"></a><span data-ttu-id="24d46-190">Sobre as `using` instruções em Q\#</span><span class="sxs-lookup"><span data-stu-id="24d46-190">About `using` statements in Q\#</span></span>

<span data-ttu-id="24d46-191">A `using` instrução também é especial para Q# .</span><span class="sxs-lookup"><span data-stu-id="24d46-191">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="24d46-192">Ela é usada para alocar qubits para uso em um bloco de código.</span><span class="sxs-lookup"><span data-stu-id="24d46-192">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="24d46-193">No Q# , todas as qubits são alocadas e liberadas dinamicamente, em vez de serem recursos fixos que estão lá para o tempo de vida inteiro de um algoritmo complexo.</span><span class="sxs-lookup"><span data-stu-id="24d46-193">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="24d46-194">Uma instrução `using` aloca um conjunto de qubits no início e libera esses qubits no final do bloco.</span><span class="sxs-lookup"><span data-stu-id="24d46-194">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="run-the-code-from-the-command-prompt"></a><span data-ttu-id="24d46-195">Executar o código do prompt de comando</span><span class="sxs-lookup"><span data-stu-id="24d46-195">Run the code from the command prompt</span></span>

<span data-ttu-id="24d46-196">Para executar o código, precisamos dizer ao compilador *que* pode ser executado quando fornecemos o `dotnet run` comando.</span><span class="sxs-lookup"><span data-stu-id="24d46-196">In order to run the code we need to tell the compiler *which* callable to run when we provide the `dotnet run` command.</span></span> <span data-ttu-id="24d46-197">Isso é feito com uma simples alteração no Q# arquivo, adicionando uma linha com `@EntryPoint()` diretamente antes do callable: a `TestBellState` operação nesse caso.</span><span class="sxs-lookup"><span data-stu-id="24d46-197">This is done with a simple change in the Q# file by adding a line with `@EntryPoint()` directly preceding the callable: the `TestBellState` operation in this case.</span></span> <span data-ttu-id="24d46-198">O código completo deve ser:</span><span class="sxs-lookup"><span data-stu-id="24d46-198">The full code should be:</span></span>

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

<span data-ttu-id="24d46-199">Para executar o programa, precisamos especificar `count` e `initial` argumentos no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="24d46-199">To run the program we need to specify `count` and `initial` arguments from the command prompt.</span></span> <span data-ttu-id="24d46-200">Vamos escolher por exemplo `count = 1000` e `initial = One` .</span><span class="sxs-lookup"><span data-stu-id="24d46-200">Let's choose for example `count = 1000` and `initial = One`.</span></span> <span data-ttu-id="24d46-201">Digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="24d46-201">Enter the following command:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

<span data-ttu-id="24d46-202">E você deve observar a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="24d46-202">And you should observe the following output:</span></span>

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="24d46-203">Se você tentar com `initial = Zero` , deverá observar:</span><span class="sxs-lookup"><span data-stu-id="24d46-203">If you try with `initial = Zero` you should observe:</span></span>

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a><span data-ttu-id="24d46-204">Preparar a superposição</span><span class="sxs-lookup"><span data-stu-id="24d46-204">Prepare superposition</span></span>

<span data-ttu-id="24d46-205">Agora vamos examinar como o Q# expressa as maneiras de colocar qubits em superposição.</span><span class="sxs-lookup"><span data-stu-id="24d46-205">Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="24d46-206">Lembre-se de que o estado de um qubit pode estar em uma sobreposição de 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="24d46-206">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="24d46-207">Usaremos a operação `Hadamard` para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="24d46-207">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="24d46-208">Se o qubit estiver em qualquer um dos estados clássicos (em que uma medição retorna `Zero` sempre ou `One` sempre), a operação `Hadamard` ou `H` colocará o qubit em um estado em que uma medição do qubit retornará `Zero` 50% do tempo e retornará `One` 50% do tempo.</span><span class="sxs-lookup"><span data-stu-id="24d46-208">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="24d46-209">Conceitualmente, o qubit pode ser pensado como a metade entre o `Zero` e o `One`.</span><span class="sxs-lookup"><span data-stu-id="24d46-209">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="24d46-210">Agora, quando simularmos a operação `TestBellState`, veremos que os resultados retornarão aproximadamente um número igual de `Zero` e `One` após a medição.</span><span class="sxs-lookup"><span data-stu-id="24d46-210">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

### <a name="x-flips-qubit-state"></a><span data-ttu-id="24d46-211">`X` inverte o estado qubit</span><span class="sxs-lookup"><span data-stu-id="24d46-211">`X` flips qubit state</span></span>

<span data-ttu-id="24d46-212">Primeiro, vamos tentar virar o qubit (se o qubit estiver em `Zero` estado, ele será invertido para `One` e vice-versa).</span><span class="sxs-lookup"><span data-stu-id="24d46-212">First we'll just try to flip the qubit (if the qubit is in `Zero` state it will flip to `One` and vice versa).</span></span> <span data-ttu-id="24d46-213">Isso é feito com a execução de uma operação `X` antes de medi-lo em `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="24d46-213">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="24d46-214">Agora os resultados são invertidos:</span><span class="sxs-lookup"><span data-stu-id="24d46-214">Now the results are reversed:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="24d46-215">Agora vamos explorar as propriedades Quantum do qubits.</span><span class="sxs-lookup"><span data-stu-id="24d46-215">Now let's explore the quantum properties of the qubits.</span></span>

### <a name="h-prepares-superposition"></a><span data-ttu-id="24d46-216">`H` Prepara a superposição</span><span class="sxs-lookup"><span data-stu-id="24d46-216">`H` prepares superposition</span></span>

<span data-ttu-id="24d46-217">Basta substituir a operação `X` na execução anterior por uma operação `H` ou Hadamard.</span><span class="sxs-lookup"><span data-stu-id="24d46-217">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="24d46-218">Em vez de inverteremos o qubit até o final de 0 a 1, só o inverteremos até a metade.</span><span class="sxs-lookup"><span data-stu-id="24d46-218">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="24d46-219">As linhas substituídas em `TestBellState` agora têm a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="24d46-219">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="24d46-220">Agora os resultados ficam mais interessantes:</span><span class="sxs-lookup"><span data-stu-id="24d46-220">Now the results get more interesting:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

<span data-ttu-id="24d46-221">Sempre que medimos, pedimos um valor clássico, mas como o qubit está na metade entre 0 e 1, obtemos (estatisticamente) 0 na metade do tempo e 1 na metade do tempo.</span><span class="sxs-lookup"><span data-stu-id="24d46-221">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span>
<span data-ttu-id="24d46-222">Isso é conhecido como **superposição** e nos dá nossa primeira visão real de um estado quântico.</span><span class="sxs-lookup"><span data-stu-id="24d46-222">This is known as **superposition** and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="24d46-223">Preparar o entrelaçamento</span><span class="sxs-lookup"><span data-stu-id="24d46-223">Prepare entanglement</span></span>

<span data-ttu-id="24d46-224">Agora, vejamos como o Q# expressa maneiras de entangle qubits.</span><span class="sxs-lookup"><span data-stu-id="24d46-224">Now let’s look at how Q# expresses ways to entangle qubits.</span></span>
<span data-ttu-id="24d46-225">Primeiro, definimos o primeiro qubit como o estado inicial e usamos a operação `H` para colocá-lo em sobreposição.</span><span class="sxs-lookup"><span data-stu-id="24d46-225">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="24d46-226">Em seguida, antes de medirmos o primeiro qubit, usamos uma nova operação ( `CNOT` ), que significa *não ser controlada*.</span><span class="sxs-lookup"><span data-stu-id="24d46-226">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for *Controlled-NOT*.</span></span>  <span data-ttu-id="24d46-227">O resultado da execução dessa operação em dois qubits é inverter o segundo qubit se o primeiro qubit for `One` .</span><span class="sxs-lookup"><span data-stu-id="24d46-227">The result of running this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="24d46-228">Agora, os dois qubits estão entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="24d46-228">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="24d46-229">Nossas estatísticas para o primeiro qubit não mudaram (possibilidade de 50-50 de `Zero` ou `One` após a medição), mas agora, quando medimos o segundo qubit, ele é __sempre__ igual ao que medimos para o primeiro qubit.</span><span class="sxs-lookup"><span data-stu-id="24d46-229">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="24d46-230">Nosso `CNOT` entrelaçou os dois qubits, de modo que o que acontecer com um deles acontecerá com o outro.</span><span class="sxs-lookup"><span data-stu-id="24d46-230">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="24d46-231">Se você inverter as medidas (fizer o segundo qubit antes do primeiro), a mesma coisa acontecerá.</span><span class="sxs-lookup"><span data-stu-id="24d46-231">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="24d46-232">A primeira medida será aleatória e a segunda estará na etapa de bloqueio com tudo o que foi descoberto para o primeiro.</span><span class="sxs-lookup"><span data-stu-id="24d46-232">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="24d46-233">A primeira coisa que precisaremos fazer é alocar dois qubits em vez de um em `TestBellState` :</span><span class="sxs-lookup"><span data-stu-id="24d46-233">The first thing we'll need to do is allocate two qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="24d46-234">Isso nos permitirá adicionar uma nova operação (`CNOT`) antes de medir (`M`) em `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="24d46-234">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="24d46-235">Adicionamos outra operação `SetQubitState` para inicializar o primeiro qubit, a fim de garantir que ele esteja sempre no estado `Zero` quando começarmos.</span><span class="sxs-lookup"><span data-stu-id="24d46-235">We've added another `SetQubitState` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="24d46-236">Também precisamos redefinir o segundo qubit antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="24d46-236">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

<span data-ttu-id="24d46-237">A rotina completa agora tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="24d46-237">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="24d46-238">Se executarmos isso, obteremos exatamente o mesmo resultado 50-50 que obtivemos antes.</span><span class="sxs-lookup"><span data-stu-id="24d46-238">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="24d46-239">No entanto, estamos interessados mesmo em como o segundo qubit reage ao primeiro que está sendo medido.</span><span class="sxs-lookup"><span data-stu-id="24d46-239">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="24d46-240">Adicionaremos essa estatística com uma nova versão da operação `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="24d46-240">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

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
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="24d46-241">O novo valor retornado (`agree`) faz o acompanhamento toda vez que a medida do primeiro qubit corresponde à medida do segundo qubit.</span><span class="sxs-lookup"><span data-stu-id="24d46-241">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span>

<span data-ttu-id="24d46-242">Executando o código que obtemos:</span><span class="sxs-lookup"><span data-stu-id="24d46-242">Running the code we obtain:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

<span data-ttu-id="24d46-243">Conforme indicado na visão geral, nossas estatísticas para o primeiro qubit não foram alteradas (possibilidade de 50-50 de 0 ou 1), mas agora, quando medimos o segundo qubit, ele é __sempre__ igual ao que medimos para o primeiro qubit, porque eles estão entrelaçados!</span><span class="sxs-lookup"><span data-stu-id="24d46-243">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

## <a name="next-steps"></a><span data-ttu-id="24d46-244">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="24d46-244">Next steps</span></span>

<span data-ttu-id="24d46-245">A [pesquisa do tutorial Grover](xref:microsoft.quantum.quickstarts.search) mostra como criar e executar o Grover Search, um dos algoritmos de computação Quantum mais populares e oferece um bom exemplo de um Q# programa que pode ser usado para resolver problemas reais com a computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="24d46-245">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="24d46-246">[A introdução ao kit de desenvolvimento Quantum](xref:microsoft.quantum.welcome) recomenda mais maneiras de aprender Q# e proquantum a programação.</span><span class="sxs-lookup"><span data-stu-id="24d46-246">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>
