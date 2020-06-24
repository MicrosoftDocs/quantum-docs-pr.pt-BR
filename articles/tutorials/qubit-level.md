---
title: 'Escreva e simule programas de nível qubit em Q #'
description: Tutorial passo a passo sobre como escrever e simular um programa Quantum que opera no nível de qubit individual
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
ms.openlocfilehash: e7ebdec4cd1aa201030d82759a3aa56473b26417
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274231"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a><span data-ttu-id="604d6-103">Tutorial: escrever e simular programas de nível qubit em Q\#</span><span class="sxs-lookup"><span data-stu-id="604d6-103">Tutorial: Write and simulate qubit-level programs in Q\#</span></span>

<span data-ttu-id="604d6-104">Bem-vindo ao tutorial do kit de desenvolvimento do Quantum sobre como escrever e simular um programa Quantum básico que opera em qubits individuais.</span><span class="sxs-lookup"><span data-stu-id="604d6-104">Welcome to the Quantum Development Kit tutorial on writing and simulating a basic quantum program that operates on individual qubits.</span></span> 

<span data-ttu-id="604d6-105">Embora o Q # tenha sido criado principalmente como uma linguagem de programação de alto nível para programas Quantum de grande escala, ele pode ser facilmente usado para explorar o nível inferior dos programas Quantum: endereçando diretamente qubits específico.</span><span class="sxs-lookup"><span data-stu-id="604d6-105">Although Q# was primarily created as a high-level programming language for large-scale quantum programs, it can just as easily be used to explore the lower level of quantum programs: directly addressing specific qubits.</span></span>
<span data-ttu-id="604d6-106">A flexibilidade do Q # permite aos usuários abordar sistemas Quantum de qualquer nível de abstração e, neste tutorial, nos aprofundamos no próprio qubits.</span><span class="sxs-lookup"><span data-stu-id="604d6-106">The flexibility of Q# allows users to approach quantum systems from any such level of abstraction, and in this tutorial we dive into the qubits themselves.</span></span>
<span data-ttu-id="604d6-107">Especificamente, examinamos os bastidores da [transformação de Fourier do Quantum](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), uma sub-rotina que é integral para muitos algoritmos maiores do Quantum.</span><span class="sxs-lookup"><span data-stu-id="604d6-107">Specifically, we take a look under the hood of the [quantum Fourier transform](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), a subroutine that is integral to many larger quantum algorithms.</span></span>

<span data-ttu-id="604d6-108">Observe que essa exibição de nível baixo do processamento de informações Quantum geralmente é descrita em termos de "[circuitos Quantum](xref:microsoft.quantum.concepts.circuits)", que representam a aplicação sequencial de Gates a qubits específicas de um sistema.</span><span class="sxs-lookup"><span data-stu-id="604d6-108">Note that this low-level view of quantum information processing is often described in terms of "[quantum circuits](xref:microsoft.quantum.concepts.circuits)," which represent the sequential application of gates to specific qubits of a system.</span></span>

<span data-ttu-id="604d6-109">Assim, as operações únicas e qubit que aplicamos sequencialmente podem ser prontamente representadas em um "diagrama de circuito".</span><span class="sxs-lookup"><span data-stu-id="604d6-109">Thus, the single- and multi-qubit operations we sequentially apply can be readily represented in a "circuit diagram."</span></span>
<span data-ttu-id="604d6-110">Em nosso caso, definiremos uma operação Q # para executar a transformação de Fourier do quantum de três qubit completa, que tem a seguinte representação como um circuito:</span><span class="sxs-lookup"><span data-stu-id="604d6-110">In our case, we will define a Q# operation to perform the full three-qubit quantum Fourier transform, which has the following representation as a circuit:</span></span>

<br/>
<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a><span data-ttu-id="604d6-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="604d6-111">Prerequisites</span></span>

* <span data-ttu-id="604d6-112">[Instale](xref:microsoft.quantum.install) o kit de desenvolvimento Quantum usando o ambiente de desenvolvimento e a linguagem preferencial.</span><span class="sxs-lookup"><span data-stu-id="604d6-112">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your preferred language and development environment.</span></span>
* <span data-ttu-id="604d6-113">Caso já tenha o QDK instalado, verifique se você o [atualizou](xref:microsoft.quantum.update) para a última versão</span><span class="sxs-lookup"><span data-stu-id="604d6-113">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>


## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="604d6-114">Neste tutorial, você aprenderá como:</span><span class="sxs-lookup"><span data-stu-id="604d6-114">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="604d6-115">Definir operações de Quantum em p #</span><span class="sxs-lookup"><span data-stu-id="604d6-115">Define quantum operations in Q#</span></span>
> * <span data-ttu-id="604d6-116">Chamar Q # operações diretamente da linha de comando ou usando um programa de host clássico</span><span class="sxs-lookup"><span data-stu-id="604d6-116">Call Q# operations directly from the command line or using a classical host program</span></span>
> * <span data-ttu-id="604d6-117">Simular uma operação Quantum de alocação qubit para saída de medida</span><span class="sxs-lookup"><span data-stu-id="604d6-117">Simulate a quantum operation from qubit allocation to measurement output</span></span>
> * <span data-ttu-id="604d6-118">Observe como o wavefunction simulado do sistema Quantum evolui em toda a operação</span><span class="sxs-lookup"><span data-stu-id="604d6-118">Observe how the quantum system's simulated wavefunction evolves throughout the operation</span></span>

<span data-ttu-id="604d6-119">A execução de um programa Quantum com o kit de desenvolvimento Quantum da Microsoft normalmente consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="604d6-119">Running a quantum program with Microsoft's Quantum Development Kit typically consists of two parts:</span></span>
1. <span data-ttu-id="604d6-120">O próprio programa, que é implementado usando a linguagem de programação do Quantum Q # e, em seguida, é chamado para ser executado em um computador Quantum ou simulador Quantum.</span><span class="sxs-lookup"><span data-stu-id="604d6-120">The program itself, which is implemented using the Q# quantum programming language, and then invoked to run on a quantum computer or quantum simulator.</span></span> <span data-ttu-id="604d6-121">Consistem em</span><span class="sxs-lookup"><span data-stu-id="604d6-121">These consist of</span></span> 
    - <span data-ttu-id="604d6-122">Q # operações: as sub-rotinas que atuam em registros de Quantum e</span><span class="sxs-lookup"><span data-stu-id="604d6-122">Q# operations: subroutines acting on quantum registers, and</span></span> 
    - <span data-ttu-id="604d6-123">Funções Q #: sub-rotinas clássicas usadas dentro do algoritmo Quantum.</span><span class="sxs-lookup"><span data-stu-id="604d6-123">Q# functions: classical subroutines used within the quantum algorithm.</span></span>
2. <span data-ttu-id="604d6-124">O ponto de entrada usado para chamar o programa Quantum e especificar o computador de destino no qual ele deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="604d6-124">The entry point used to call the quantum program and specify the target machine on which it should be run.</span></span>
    <span data-ttu-id="604d6-125">Isso pode ser feito diretamente da linha de comando ou por meio de um programa de host escrito em uma linguagem de programação clássica, como Python ou C#.</span><span class="sxs-lookup"><span data-stu-id="604d6-125">This can be done directly from the command line, or through a host program written in a classical programming language like Python or C#.</span></span>
    <span data-ttu-id="604d6-126">Este tutorial inclui instruções para qualquer método que você preferir.</span><span class="sxs-lookup"><span data-stu-id="604d6-126">This tutorial includes instructions for whichever method you prefer.</span></span>

## <a name="allocate-qubits-and-define-quantum-operations"></a><span data-ttu-id="604d6-127">Alocar qubits e definir operações Quantum</span><span class="sxs-lookup"><span data-stu-id="604d6-127">Allocate qubits and define quantum operations</span></span>

<span data-ttu-id="604d6-128">A primeira parte deste tutorial consiste em definir a operação Q # `Perform3qubitQFT` , que executa a transformação de Fourier do Quantum em três qubits.</span><span class="sxs-lookup"><span data-stu-id="604d6-128">The first part of this tutorial consists of defining the Q# operation `Perform3qubitQFT`, which performs the quantum Fourier transform on three qubits.</span></span> 

<span data-ttu-id="604d6-129">Além disso, usaremos a [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) função para observar como o wavefunction simulado de nosso sistema de três qubit evolui na operação.</span><span class="sxs-lookup"><span data-stu-id="604d6-129">In addition, we will use the [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) function to observe how the simulated wavefunction of our three qubit system evolves across the operation.</span></span>

<span data-ttu-id="604d6-130">A primeira etapa é criar seu projeto e arquivo do Q #.</span><span class="sxs-lookup"><span data-stu-id="604d6-130">The first step is creating your Q# project and file.</span></span>
<span data-ttu-id="604d6-131">As etapas para isso dependem do ambiente que você usará para chamar o programa e pode encontrar os detalhes nos respectivos [guias de instalação](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="604d6-131">The steps for this depend on the environment you will use to call the program, and you can find the details in the respective [installation guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="604d6-132">Descreveremos os componentes do arquivo passo a passo, mas o código também está disponível como um bloco completo abaixo.</span><span class="sxs-lookup"><span data-stu-id="604d6-132">We will walk you through the components of the file step-by-step, but the code is also available as a full block below.</span></span>

### <a name="namespaces-to-access-other-q-operations"></a><span data-ttu-id="604d6-133">Namespaces para acessar outras operações Q #</span><span class="sxs-lookup"><span data-stu-id="604d6-133">Namespaces to access other Q# operations</span></span>
<span data-ttu-id="604d6-134">Dentro do arquivo, primeiro definimos o namespace `NamespaceQFT` que será acessado pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="604d6-134">Inside the file, we first define the namespace `NamespaceQFT` which will be accessed by the compiler.</span></span>
<span data-ttu-id="604d6-135">Para que nossa operação faça uso de operações Q # existentes, abrimos os `Microsoft.Quantum.<>` namespaces relevantes.</span><span class="sxs-lookup"><span data-stu-id="604d6-135">For our operation to make use of existing Q# operations, we open the relevant `Microsoft.Quantum.<>` namespaces.</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a><span data-ttu-id="604d6-136">Definir operações com argumentos e Devoluções</span><span class="sxs-lookup"><span data-stu-id="604d6-136">Define operations with arguments and returns</span></span>
<span data-ttu-id="604d6-137">Em seguida, definimos a `Perform3qubitQFT` operação:</span><span class="sxs-lookup"><span data-stu-id="604d6-137">Next, we define the `Perform3qubitQFT` operation:</span></span>

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

<span data-ttu-id="604d6-138">Por enquanto, a operação não usa argumentos e não retorna nada---, nesse caso, escrevemos que ele retorna um `Unit` objeto, que é semelhante a `void` em C# ou uma tupla vazia, `Tuple[()]` em Python.</span><span class="sxs-lookup"><span data-stu-id="604d6-138">For now, the operation takes no arguments and does not return anything---in this case we write that it returns a `Unit` object, which is akin to `void` in C# or an empty tuple, `Tuple[()]`, in Python.</span></span>
<span data-ttu-id="604d6-139">Posteriormente, iremos modificá-lo para retornar uma matriz de resultados de medição, em que ponto `Unit` será substituído por `Result[]` .</span><span class="sxs-lookup"><span data-stu-id="604d6-139">Later, we will modify it to return an array of measurement results, at which point `Unit` will be replaced by `Result[]`.</span></span> 

### <a name="allocate-qubits-with-using"></a><span data-ttu-id="604d6-140">Alocar qubits com`using`</span><span class="sxs-lookup"><span data-stu-id="604d6-140">Allocate qubits with `using`</span></span>
<span data-ttu-id="604d6-141">Em nossa operação Q #, primeiro alocamos um registro de três qubits com a `using` instrução:</span><span class="sxs-lookup"><span data-stu-id="604d6-141">Within our Q# operation, we first allocate a register of three qubits with the `using` statement:</span></span>

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

<span data-ttu-id="604d6-142">Com `using` o, os qubits são alocados automaticamente no estado $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="604d6-142">With `using`, the qubits are automatically allocated in the $\ket{0}$ state.</span></span> <span data-ttu-id="604d6-143">Podemos verificar isso usando [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) e [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) , que imprime uma cadeia de caracteres e o estado atual do sistema para o console.</span><span class="sxs-lookup"><span data-stu-id="604d6-143">We can verify this by using [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) and [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine), which print a string and the system's current state to the console.</span></span>

> [!NOTE]
> <span data-ttu-id="604d6-144">As `Message(<string>)` `DumpMachine()` funções e (de [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) e [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) , respectivamente) são impressas diretamente no console.</span><span class="sxs-lookup"><span data-stu-id="604d6-144">The `Message(<string>)` and `DumpMachine()` functions (from [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics), respectively) both print directly to the console.</span></span> <span data-ttu-id="604d6-145">Assim como uma computação Quantum real, Q # não nos permite acessar diretamente os Estados de qubit.</span><span class="sxs-lookup"><span data-stu-id="604d6-145">Just like a real quantum computation, Q# does not allow us to directly access qubit states.</span></span>
> <span data-ttu-id="604d6-146">No entanto, como `DumpMachine` imprime o estado atual do computador de destino, ele pode fornecer Insight valioso para depuração e aprendizagem quando usado em conjunto com o simulador de estado completo.</span><span class="sxs-lookup"><span data-stu-id="604d6-146">However, as `DumpMachine` prints the target machine's current state, it can provide valuable insight for debugging and learning when used in conjunction with the full state simulator.</span></span>


### <a name="applying-single-qubit-and-controlled-gates"></a><span data-ttu-id="604d6-147">Aplicando Gates qubit e controlado</span><span class="sxs-lookup"><span data-stu-id="604d6-147">Applying single-qubit and controlled gates</span></span>

<span data-ttu-id="604d6-148">Em seguida, aplicamos as Gates que compõem a própria operação.</span><span class="sxs-lookup"><span data-stu-id="604d6-148">Next, we apply the gates which comprise the operation itself.</span></span>
<span data-ttu-id="604d6-149">O Q # já contém muitas Gates básicas de Quantum como operações no [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) namespace, e elas não são exceção.</span><span class="sxs-lookup"><span data-stu-id="604d6-149">Q# already contains many basic quantum gates as operations in the [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) namespace, and these are no exception.</span></span> 

<span data-ttu-id="604d6-150">Em uma operação Q #, as instruções que chamam o callablefiles certamente serão executadas em ordem sequencial.</span><span class="sxs-lookup"><span data-stu-id="604d6-150">Within a Q# operation, the statements invoking callables will of course be executed in sequential order.</span></span>
<span data-ttu-id="604d6-151">Portanto, o primeiro portão a ser aplicado é o [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) para o primeiro qubit:</span><span class="sxs-lookup"><span data-stu-id="604d6-151">Hence, the first gate to apply is the [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) to the first qubit:</span></span>

<br/>
<img src="../media/qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

<span data-ttu-id="604d6-152">Para aplicar uma operação a um qubit específico de um registro (ou seja, um único `Qubit` de uma matriz `Qubit[]` ), usamos a notação de índice padrão.</span><span class="sxs-lookup"><span data-stu-id="604d6-152">To apply an operation to a specific qubit from a register (i.e. a single `Qubit` from an array `Qubit[]`) we use standard index notation.</span></span>
<span data-ttu-id="604d6-153">Portanto, aplicar o [`H`](xref:microsoft.quantum.intrinsic.h) à primeira qubit do nosso registro `qs` assume a forma:</span><span class="sxs-lookup"><span data-stu-id="604d6-153">So, applying the [`H`](xref:microsoft.quantum.intrinsic.h) to the first qubit of our register `qs` takes the form:</span></span>

```qsharp
            H(qs[0]);
```

<span data-ttu-id="604d6-154">Além de aplicar o `H` portão (Hadamard) a qubits individuais, o circuito QFT consiste principalmente em [`R1`](xref:microsoft.quantum.intrinsic.r1) rotações controladas.</span><span class="sxs-lookup"><span data-stu-id="604d6-154">Besides applying the `H` (Hadamard) gate to individual qubits, the QFT circuit consists primarily of controlled [`R1`](xref:microsoft.quantum.intrinsic.r1) rotations.</span></span>
<span data-ttu-id="604d6-155">Uma `R1(θ, <qubit>)` operação em geral deixa o componente $ \ket {0} $ do qubit inalterado, ao mesmo tempo em que aplica uma rotação de $e ^ {i\theta} $ ao componente $ \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="604d6-155">An `R1(θ, <qubit>)` operation in general leaves the $\ket{0}$ component of the qubit unchanged, while applying a rotation of $e^{i\theta}$ to the $\ket{1}$ component.</span></span>

#### <a name="controlled-operations"></a><span data-ttu-id="604d6-156">Operações controladas</span><span class="sxs-lookup"><span data-stu-id="604d6-156">Controlled operations</span></span>

<span data-ttu-id="604d6-157">O Q # torna extremamente fácil a condição da execução de uma operação em um ou vários qubits de controle.</span><span class="sxs-lookup"><span data-stu-id="604d6-157">Q# makes it extremely easy to condition the execution of an operation upon one or multiple control qubits.</span></span>
<span data-ttu-id="604d6-158">Em geral, simplesmente precedemos a chamada com `Controlled` e os argumentos da operação são alterados como:</span><span class="sxs-lookup"><span data-stu-id="604d6-158">In general, we merely preface the call with `Controlled`, and the operation arguments change as:</span></span>

 <span data-ttu-id="604d6-159">`Op(<normal args>)`$ \tO $ `Controlled Op([<control qubits>], (<normal args>))` .</span><span class="sxs-lookup"><span data-stu-id="604d6-159">`Op(<normal args>)` $\to$ `Controlled Op([<control qubits>], (<normal args>))`.</span></span>

<span data-ttu-id="604d6-160">Observe que o qubits de controle deve ser fornecido como uma matriz, mesmo se for um único qubit.</span><span class="sxs-lookup"><span data-stu-id="604d6-160">Note that the control qubits must be provided as an array, even if it is a single qubit.</span></span>

<span data-ttu-id="604d6-161">Após o `H` , vemos que as próximas Gates são as `R1` Gates que atuam na primeira qubit (e controladas pela segunda/terceira):</span><span class="sxs-lookup"><span data-stu-id="604d6-161">After the `H`, we see that the next gates are the `R1` gates acting on the first qubit (and controlled by the second/third):</span></span>

<br/>
<img src="../media/qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

<span data-ttu-id="604d6-162">Chamamos isso de</span><span class="sxs-lookup"><span data-stu-id="604d6-162">We call these with</span></span>

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

<span data-ttu-id="604d6-163">Observe que usamos a [`PI()`](xref:microsoft.quantum.math.pi) função do [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) namespace para definir as rotações em termos de pi radianos.</span><span class="sxs-lookup"><span data-stu-id="604d6-163">Note that we use the [`PI()`](xref:microsoft.quantum.math.pi) function from the [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) namespace to define the rotations in terms of pi radians.</span></span>
<span data-ttu-id="604d6-164">Além disso, dividimos por um `Double` (por exemplo, `2.0` ) porque dividir por um inteiro `2` geraria um erro de tipo.</span><span class="sxs-lookup"><span data-stu-id="604d6-164">Additionally, we divide by a `Double` (e.g. `2.0`) because dividing by an integer `2` would throw a type error.</span></span> 

> [!TIP]
> <span data-ttu-id="604d6-165">`R1(π/2)`e `R1(π/4)` são equivalentes às `S` `T` operações e (também em `Microsoft.Quantum.Intrinsic` ).</span><span class="sxs-lookup"><span data-stu-id="604d6-165">`R1(π/2)` and `R1(π/4)` are equivalent to the `S` and `T` operations (also in `Microsoft.Quantum.Intrinsic`).</span></span>


<span data-ttu-id="604d6-166">Depois de aplicar as `H` operações relevantes e as rotações controladas à segunda e terceira qubits:</span><span class="sxs-lookup"><span data-stu-id="604d6-166">After applying the relevant `H` operations and controlled rotations to the second and third qubits:</span></span>

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

<span data-ttu-id="604d6-167">Precisamos aplicar um portão apenas [`SWAP`](xref:microsoft.quantum.intrinsic.swap) para concluir o circuito:</span><span class="sxs-lookup"><span data-stu-id="604d6-167">we need only apply a [`SWAP`](xref:microsoft.quantum.intrinsic.swap) gate to complete the circuit:</span></span>

```qsharp
            SWAP(qs[2], qs[0]);
```

<span data-ttu-id="604d6-168">Isso é necessário porque a natureza da transformação de Fourier do Quantum gera o qubits na ordem inversa, portanto, as trocas permitem a integração direta da sub-rotina em algoritmos maiores.</span><span class="sxs-lookup"><span data-stu-id="604d6-168">This is necessary because the nature of the quantum Fourier transform outputs the qubits in reverse order, so the swaps allow for seamless integration of the subroutine into larger algorithms.</span></span>

<span data-ttu-id="604d6-169">Portanto, terminamos de escrever as operações de nível qubit da transformação de Fourier do Quantum em nossa operação Q #:</span><span class="sxs-lookup"><span data-stu-id="604d6-169">Hence we have finished writing the qubit-level operations of the quantum Fourier transform into our Q# operation:</span></span>

<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

<span data-ttu-id="604d6-170">No entanto, não podemos chamá-lo um dia mesmo.</span><span class="sxs-lookup"><span data-stu-id="604d6-170">However, we can't call it a day just yet.</span></span>
<span data-ttu-id="604d6-171">Nosso qubits estava no estado $ \ket {0} $ quando os alocamos, e muito parecido com a vida, em Q # devemos deixar coisas da mesma forma que as encontramos (ou melhor!).</span><span class="sxs-lookup"><span data-stu-id="604d6-171">Our qubits were in state $\ket{0}$ when we allocated them, and much like in life, in Q# we should leave things the same way we found them (or better!).</span></span>

### <a name="deallocate-qubits"></a><span data-ttu-id="604d6-172">Desalocar qubits</span><span class="sxs-lookup"><span data-stu-id="604d6-172">Deallocate qubits</span></span>

<span data-ttu-id="604d6-173">Chamamos [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) novamente para ver o estado de pós-operação e, por fim, aplicam [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) -se ao registro qubit para redefinir nosso qubits para $ \ket {0} $ antes de concluir a operação:</span><span class="sxs-lookup"><span data-stu-id="604d6-173">We call [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) again to see the post-operation state, and finally apply [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) to the qubit register to reset our qubits to $\ket{0}$ before completing the operation:</span></span>

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

<span data-ttu-id="604d6-174">Exigir que todos os qubits desalocados sejam explicitamente definidos como $ \ket {0} $ é um recurso básico de Q #, pois ele permite que outras operações saibam seu estado precisamente quando começam a usar esses mesmos qubits (um recurso escasso).</span><span class="sxs-lookup"><span data-stu-id="604d6-174">Requiring that all deallocated qubits be explicitly set to $\ket{0}$ is a basic feature of Q#, as it allows other operations to know their state precisely when they begin using those same qubits (a scarce resource).</span></span>
<span data-ttu-id="604d6-175">Além disso, isso garante que eles não sejam confusas com nenhum outro qubits no sistema.</span><span class="sxs-lookup"><span data-stu-id="604d6-175">Additionally, this assures that they not be entangled with any other qubits in the system.</span></span>
<span data-ttu-id="604d6-176">Se a redefinição não for executada no final de um `using` bloco de alocação, um erro de tempo de execução será gerado.</span><span class="sxs-lookup"><span data-stu-id="604d6-176">If the reset is not performed at the end of a `using` allocation block, a runtime error will be thrown.</span></span>

<span data-ttu-id="604d6-177">O arquivo completo de Q # agora deve ser assim:</span><span class="sxs-lookup"><span data-stu-id="604d6-177">Your full Q# file should now look like this:</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


<span data-ttu-id="604d6-178">Com o arquivo e a operação de Q # concluídos, nosso programa Quantum está pronto para ser chamado e simulado.</span><span class="sxs-lookup"><span data-stu-id="604d6-178">With the Q# file and operation complete, our quantum program is ready to be called and simulated.</span></span>

## <a name="execute-the-program"></a><span data-ttu-id="604d6-179">Executar o programa</span><span class="sxs-lookup"><span data-stu-id="604d6-179">Execute the program</span></span>

<span data-ttu-id="604d6-180">Depois de ter definido nossa operação Q # em um `.qs` arquivo, agora precisamos chamar essa operação e observar os dados clássicos retornados.</span><span class="sxs-lookup"><span data-stu-id="604d6-180">Having defined our Q# operation in a `.qs` file, we now need to call that operation and observe any returned classical data.</span></span>
<span data-ttu-id="604d6-181">Por enquanto, não há nada retornado (Lembre-se de que nossa operação definida acima retorna `Unit` ), mas quando depois modificamos a operação Q # para retornar uma matriz de resultados de medida ( `Result[]` ), abordaremos isso.</span><span class="sxs-lookup"><span data-stu-id="604d6-181">For now, there isn't anything returned (recall that our operation defined above returns `Unit`), but when we later modify the Q# operation to return an array of measurement results (`Result[]`), we will address this.</span></span>

<span data-ttu-id="604d6-182">Embora o programa Q # seja onipresente em todos os ambientes usados para chamá-lo, a maneira de fazer isso é, certamente, diferente.</span><span class="sxs-lookup"><span data-stu-id="604d6-182">While the Q# program is ubiquitous across the environments used to call it, the manner of doing so will of course vary.</span></span> <span data-ttu-id="604d6-183">Como tal, basta seguir as instruções na guia correspondente à sua configuração: trabalhando no aplicativo de linha de comando Q # ou usando um programa de host em Python ou C#.</span><span class="sxs-lookup"><span data-stu-id="604d6-183">As such, simply follow the instructions in the tab corresponding to your setup: working from the Q# command line application or using a host program in Python or C#.</span></span>

#### <a name="command-line"></a>[<span data-ttu-id="604d6-184">Linha de comando</span><span class="sxs-lookup"><span data-stu-id="604d6-184">Command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="604d6-185">A execução do programa Q # da linha de comando requer apenas uma pequena alteração no arquivo Q #.</span><span class="sxs-lookup"><span data-stu-id="604d6-185">Running the Q# program from the command line requires only a small change to the Q# file.</span></span>

<span data-ttu-id="604d6-186">Basta adicionar `@EntryPoint()` a uma linha anterior à definição da operação:</span><span class="sxs-lookup"><span data-stu-id="604d6-186">Simply add `@EntryPoint()` to a line preceding the operation definition:</span></span>

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

<span data-ttu-id="604d6-187">Para executar o programa, abra o terminal na pasta do seu projeto e insira</span><span class="sxs-lookup"><span data-stu-id="604d6-187">To run the program, open the terminal in the folder of your project and enter</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="604d6-188">Após a execução, você deverá ver `Message` as `DumpMachine` saídas e abaixo impressas em seu console.</span><span class="sxs-lookup"><span data-stu-id="604d6-188">Upon execution, you should see the `Message` and `DumpMachine` outputs below printed in your console.</span></span>


#### <a name="python"></a>[<span data-ttu-id="604d6-189">Python</span><span class="sxs-lookup"><span data-stu-id="604d6-189">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="604d6-190">Criar um arquivo de host do Python: `host.py` .</span><span class="sxs-lookup"><span data-stu-id="604d6-190">Create a Python host file: `host.py`.</span></span>

<span data-ttu-id="604d6-191">O arquivo de host é construído da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="604d6-191">The host file is constructed as follows:</span></span> 
1. <span data-ttu-id="604d6-192">Primeiro, importamos o `qsharp` módulo, que registra o carregador de módulo para interoperabilidade do Q #.</span><span class="sxs-lookup"><span data-stu-id="604d6-192">First, we import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="604d6-193">Isso permite que os namespaces Q # (por exemplo `NamespaceQFT` , que definimos em nosso arquivo q #) apareçam como módulos Python, dos quais podemos importar as operações Q #.</span><span class="sxs-lookup"><span data-stu-id="604d6-193">This allows Q# namespaces (e.g. the `NamespaceQFT` we defined in our Q# file) to appear as Python modules, from which we can import Q# operations.</span></span>
2. <span data-ttu-id="604d6-194">Em seguida, importe as operações Q # que invocaremos diretamente---nesse caso, `Perform3qubitQFT` .</span><span class="sxs-lookup"><span data-stu-id="604d6-194">Then, import the Q# operations which we will directly invoke---in this case, `Perform3qubitQFT`.</span></span>
    <span data-ttu-id="604d6-195">Precisamos importar apenas o ponto de entrada em um programa Q # (ou seja _not_ , operações como `H` e `R1` , que são chamadas por outras operações q #, mas nunca pelo host clássico).</span><span class="sxs-lookup"><span data-stu-id="604d6-195">We need only import the entry point into a Q# program (i.e. _not_ operations like `H` and `R1`, which are called by other Q# operations but never by the classical host).</span></span>
3. <span data-ttu-id="604d6-196">Na simulação de operações ou funções do Q #, use o formulário `<Q#callable>.simulate(<args>)` para executá-las no `QuantumSimulator()` computador de destino.</span><span class="sxs-lookup"><span data-stu-id="604d6-196">In simulating Q# operations or functions, use the form `<Q#callable>.simulate(<args>)` to run them on the `QuantumSimulator()` target machine.</span></span> 

> [!NOTE]
> <span data-ttu-id="604d6-197">Se quiséssemos chamar a operação em um computador diferente, por exemplo, o `ResourceEstimator()` , seria simplesmente usado `<Q#callable>.estimate_resources(<args>)` .</span><span class="sxs-lookup"><span data-stu-id="604d6-197">If we wanted to call the operation on a different machine, for example the `ResourceEstimator()`, we would simply use `<Q#callable>.estimate_resources(<args>)`.</span></span>
> <span data-ttu-id="604d6-198">Em geral, as operações de Q # são independentes para os computadores nos quais elas são executadas, mas alguns recursos como `DumpMachine` podem se comportar de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="604d6-198">In general, Q# operations are agnostic to the machines on which they're run, but some features such as `DumpMachine` may behave differently.</span></span>

4. <span data-ttu-id="604d6-199">Após a execução da simulação, a chamada de operação retornará valores conforme definido no arquivo Q #.</span><span class="sxs-lookup"><span data-stu-id="604d6-199">Upon performing the simulation, the operation call will return values as defined in the Q# file.</span></span>
    <span data-ttu-id="604d6-200">Por enquanto, não há nada retornado, mas posteriormente, veremos um exemplo de atribuição e processamento desses valores.</span><span class="sxs-lookup"><span data-stu-id="604d6-200">For now there is nothing returned, but later on we will see an example of assigning and processing these values.</span></span>
    <span data-ttu-id="604d6-201">Com os dados resultantes em nossas mãos e totalmente clássicos, podemos fazer tudo o que gostaríamos com ele.</span><span class="sxs-lookup"><span data-stu-id="604d6-201">With the resultant data in our hands and totally classical, we can do whatever we'd like with it.</span></span>

<span data-ttu-id="604d6-202">O `host.py` arquivo completo deve ser o seguinte:</span><span class="sxs-lookup"><span data-stu-id="604d6-202">Your full `host.py` file should be this:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

<span data-ttu-id="604d6-203">Execute o arquivo Python e, em seu console, você verá as `Message` saídas e `DumpMachine` abaixo.</span><span class="sxs-lookup"><span data-stu-id="604d6-203">Run the Python file, and printed in your console you should see the `Message` and `DumpMachine` outputs below.</span></span> 


#### <a name="c"></a>[<span data-ttu-id="604d6-204">C#</span><span class="sxs-lookup"><span data-stu-id="604d6-204">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="604d6-205">Seguindo as mesmas instruções do guia de [instalação](xref:microsoft.quantum.install.cs)do, crie um arquivo de host C# e renomeie-o como `host.cs` .</span><span class="sxs-lookup"><span data-stu-id="604d6-205">Following the same instructions as in the [install guide](xref:microsoft.quantum.install.cs), create a C# host file, and rename it to `host.cs`.</span></span>

<span data-ttu-id="604d6-206">O host C# tem quatro partes:</span><span class="sxs-lookup"><span data-stu-id="604d6-206">The C# host has four parts:</span></span>
1. <span data-ttu-id="604d6-207">Constrói um simulador quântico.</span><span class="sxs-lookup"><span data-stu-id="604d6-207">Construct a quantum simulator.</span></span>
    <span data-ttu-id="604d6-208">No código abaixo, essa é a variável `qsim` .</span><span class="sxs-lookup"><span data-stu-id="604d6-208">In the code below, this is the variable `qsim`.</span></span>
2. <span data-ttu-id="604d6-209">Calcula os argumentos necessários para o algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="604d6-209">Compute any arguments required for the quantum algorithm.</span></span>
    <span data-ttu-id="604d6-210">Não há nenhum neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="604d6-210">There are none in this example.</span></span>
3. <span data-ttu-id="604d6-211">Executa o algoritmo quântico.</span><span class="sxs-lookup"><span data-stu-id="604d6-211">Run the quantum algorithm.</span></span> 
    <span data-ttu-id="604d6-212">Cada operação Q# gera uma classe C# com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="604d6-212">Each Q# operation generates a C# class with the same name.</span></span> 
    <span data-ttu-id="604d6-213">Essa classe tem um método `Run` que executa a operação de **maneira assíncrona**.</span><span class="sxs-lookup"><span data-stu-id="604d6-213">This class has a `Run` method that **asynchronously** executes the operation.</span></span>
    <span data-ttu-id="604d6-214">A execução é assíncrona, porque a execução no hardware real será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="604d6-214">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> 
    <span data-ttu-id="604d6-215">Como o `Run` método é assíncrono, chamamos o `Wait()` método; isso bloqueia a execução até que a tarefa seja concluída e retorna o resultado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="604d6-215">Because the `Run` method is asynchronous, we call the `Wait()` method; this blocks execution until the task completes and returns the result synchronously.</span></span> 
4. <span data-ttu-id="604d6-216">Processar o resultado retornado da operação.</span><span class="sxs-lookup"><span data-stu-id="604d6-216">Process the returned result of the operation.</span></span>
    <span data-ttu-id="604d6-217">Por enquanto, a operação não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="604d6-217">For now, the operation returns nothing.</span></span>


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
<span data-ttu-id="604d6-218">Execute o aplicativo e a saída deve corresponder à seguinte.</span><span class="sxs-lookup"><span data-stu-id="604d6-218">Run the application, and your output should match that below.</span></span>
<span data-ttu-id="604d6-219">O programa será encerrado depois que você pressionar uma tecla.</span><span class="sxs-lookup"><span data-stu-id="604d6-219">The program will exit after you press a key.</span></span>
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

<span data-ttu-id="604d6-220">Quando chamado no simulador de estado completo, `DumpMachine()` fornece essas representações de vários do wavefunction do estado do Quantum.</span><span class="sxs-lookup"><span data-stu-id="604d6-220">When called on the full-state simulator, `DumpMachine()` provides these mutliple representations of the quantum state's wavefunction.</span></span> <span data-ttu-id="604d6-221">Os possíveis estados de um sistema $n $-qubit podem ser representados por Estados de base computacional $2 ^ n $, cada um com um coeficiente complexo correspondente (simplesmente uma amplitude e uma fase).</span><span class="sxs-lookup"><span data-stu-id="604d6-221">The possible states of an $n$-qubit system can be represented by $2^n$ computational basis states, each with a corresponding complex coefficient (simply an amplitude and a phase).</span></span>
<span data-ttu-id="604d6-222">Os Estados de base computacional correspondem a todas as possíveis cadeias de caracteres binárias de comprimento $n $---ou seja, todas as combinações possíveis de Estados qubit $ \ket {0} $ e $ \ket {1} $, em que cada dígito binário corresponde a um qubit individual.</span><span class="sxs-lookup"><span data-stu-id="604d6-222">The computational basis states correspond to all the possible binary strings of length $n$---that is, all the possible combinations of qubit states $\ket{0}$ and $\ket{1}$, where each binary digit corresponds to an individual qubit.</span></span>

<span data-ttu-id="604d6-223">A primeira linha fornece um comentário com as IDs do qubits correspondente em sua ordem significativa.</span><span class="sxs-lookup"><span data-stu-id="604d6-223">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="604d6-224">Qubit `2` ser o "mais significativo" significa simplesmente que na representação binária do vetor de estado base $ \ket{i} $, o estado de qubit `2` corresponde ao dígito mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="604d6-224">Qubit `2` being the "most significant" simply means that in the binary representation of basis state vector $\ket{i}$, the state of qubit `2` corresponds to the left-most digit.</span></span> <span data-ttu-id="604d6-225">Por exemplo, $ \ket {6} = \ket {110} $ compreende qubits `2` e `1` ambos em $ \ket {1} $ e qubit `0` em $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="604d6-225">For example, $\ket{6} = \ket{110}$ comprises qubits `2` and `1` both in $\ket{1}$ and qubit `0` in $\ket{0}$.</span></span>


<span data-ttu-id="604d6-226">O restante das linhas descreve a amplitude de probabilidade de medir o vetor de estado base $ \ket{i} $ nos formatos cartesianas e polar.</span><span class="sxs-lookup"><span data-stu-id="604d6-226">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{i}$ in both Cartesian and polar formats.</span></span>
<span data-ttu-id="604d6-227">Em detalhes para a primeira linha do nosso estado de entrada $ \ket {000} $:</span><span class="sxs-lookup"><span data-stu-id="604d6-227">In detail for the first row of our input state $\ket{000}$:</span></span>
* <span data-ttu-id="604d6-228">**`|0>:`** Essa linha corresponde ao `0` estado de base computacional (Considerando que nossa pós-alocação de estado inicial era $ \ket {000} $, esperamos que esse seja o único estado com amplitude de probabilidade neste ponto).</span><span class="sxs-lookup"><span data-stu-id="604d6-228">**`|0>:`** this row corresponds to the `0` computational basis state (given that our initial state post-allocation was $\ket{000}$, we would expect this to be the only state with probability amplitude at this point).</span></span>
* <span data-ttu-id="604d6-229">**`1.000000 +  0.000000 i`**: a amplitude de probabilidade no formato cartesiano.</span><span class="sxs-lookup"><span data-stu-id="604d6-229">**`1.000000 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="604d6-230">**` == `**: o `equal` sinal separa as representações equivalentes.</span><span class="sxs-lookup"><span data-stu-id="604d6-230">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="604d6-231">**`********************`**: Uma representação gráfica da magnitude, o número de `*` é proporcional à probabilidade de medir esse vetor de estado.</span><span class="sxs-lookup"><span data-stu-id="604d6-231">**`********************`**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span> 
* <span data-ttu-id="604d6-232">**`[ 1.000000 ]`**: o valor numérico da magnitude</span><span class="sxs-lookup"><span data-stu-id="604d6-232">**`[ 1.000000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="604d6-233">**`    ---`**: Uma representação gráfica da fase de amplitude.</span><span class="sxs-lookup"><span data-stu-id="604d6-233">**`    ---`**: A graphical representation of the amplitude's phase.</span></span>
* <span data-ttu-id="604d6-234">**`[ 0.0000 rad ]`**: o valor numérico da fase (em radianos).</span><span class="sxs-lookup"><span data-stu-id="604d6-234">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="604d6-235">A magnitude e a fase são exibidas com uma representação gráfica.</span><span class="sxs-lookup"><span data-stu-id="604d6-235">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="604d6-236">A representação de magnitude é simples: ela mostra uma barra de `*` e quanto maior a probabilidade, maior será a barra.</span><span class="sxs-lookup"><span data-stu-id="604d6-236">The magnitude representation is straightforward: it shows a bar of `*`, and the higher the probability, the larger the bar will be.</span></span> <span data-ttu-id="604d6-237">Para a fase, consulte [testando e Depurando: despejar funções](xref:microsoft.quantum.guide.testingdebugging#dump-functions) para as possíveis representações de símbolo com base em intervalos de ângulo.</span><span class="sxs-lookup"><span data-stu-id="604d6-237">For the phase, see [Testing and debugging: dump functions](xref:microsoft.quantum.guide.testingdebugging#dump-functions) for the possible symbol representations based on angle ranges.</span></span>


<span data-ttu-id="604d6-238">Portanto, a saída impressa está ilustrando que nossas Gates programadas transformaram nosso estado de</span><span class="sxs-lookup"><span data-stu-id="604d6-238">So, the printed output is illustrating that our programmed gates transformed our state from</span></span>

<span data-ttu-id="604d6-239">$ $ \ket{\psi} \_ {Initial} = \ket {000} $ $</span><span class="sxs-lookup"><span data-stu-id="604d6-239">$$ \ket{\psi}\_{initial} = \ket{000} $$</span></span>

<span data-ttu-id="604d6-240">para</span><span class="sxs-lookup"><span data-stu-id="604d6-240">to</span></span> 

<span data-ttu-id="604d6-241">$ $ \begin{align} \ket{\psi} \_ {final} &= \frac {1} {\sqrt {8} } \left (\ket {000} + \ket {001} + \ket {010} + \ket {011} + \ket {100} + \ket {101} + \ket {110} + \ket {111} \right) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="604d6-241">$$ \begin{align} \ket{\psi}\_{final} &= \frac{1}{\sqrt{8}} \left( \ket{000} + \ket{001} + \ket{010} + \ket{011} + \ket{100} + \ket{101} + \ket{110} + \ket{111}  \right) \\\\ &= \frac{1}{\sqrt{2^n}}\sum\_{j=0}^{2^n-1} \ket{j}, \end{align} $$</span></span>

<span data-ttu-id="604d6-242">que é precisamente o comportamento da transformação de Fourier de 3 qubit.</span><span class="sxs-lookup"><span data-stu-id="604d6-242">which is precisely the behavior of the 3-qubit Fourier transform.</span></span> 

<span data-ttu-id="604d6-243">Se você estiver curioso sobre como outros Estados de entrada são afetados, incentivamos você a brincar com a aplicação de operações qubit antes da transformação.</span><span class="sxs-lookup"><span data-stu-id="604d6-243">If you are curious about how other input states are affected, we encourage you to play around with applying qubit operations before the transform.</span></span>

## <a name="adding-measurements"></a><span data-ttu-id="604d6-244">Adicionando medidas</span><span class="sxs-lookup"><span data-stu-id="604d6-244">Adding measurements</span></span>

<span data-ttu-id="604d6-245">Infelizmente, uma base da mecânica quantum nos informa que um sistema Quantum real não pode ter tal `DumpMachine` função.</span><span class="sxs-lookup"><span data-stu-id="604d6-245">Unfortunately, a cornerstone of quantum mechanics tells us that a real quantum system cannot have such a `DumpMachine` function.</span></span> <span data-ttu-id="604d6-246">Em vez disso, somos forçados a extrair informações por meio de medidas, o que, em geral, não apenas consegue nos fornecer o estado completo do Quantum, mas também pode alterar drasticamente o próprio sistema.</span><span class="sxs-lookup"><span data-stu-id="604d6-246">Instead, we're forced to extract information through measurements, which in general not only fail to provide us the full quantum state, but can also drastically alter the system itself.</span></span>
<span data-ttu-id="604d6-247">Há muitos tipos de medidas de Quantum, mas nos concentraremos nas medidas mais básicas: projetadas em qubits único.</span><span class="sxs-lookup"><span data-stu-id="604d6-247">There are many sorts of quantum measurements, but we will focus on the most basic: projective measurements on single qubits.</span></span>
<span data-ttu-id="604d6-248">Na medida em uma determinada base (por exemplo, a base computacional $ \{ \ket {0} , \ket {1} \} $), o estado de qubit é projetado para qualquer estado base que foi medido---, portanto, destruir qualquer superposição entre os dois.</span><span class="sxs-lookup"><span data-stu-id="604d6-248">Upon measurement in a given basis (e.g. the computational basis $ \{ \ket{0}, \ket{1} \} $), the qubit state is projected onto whichever basis state was measured---hence destroying any superposition between the two.</span></span>

<span data-ttu-id="604d6-249">Para implementar medidas em um programa Q #, usamos a `M` operação (from `Microsoft.Quantum.Intrinsic` ), que retorna um `Result` tipo.</span><span class="sxs-lookup"><span data-stu-id="604d6-249">To implement measurements within a Q# program, we use the `M` operation (from `Microsoft.Quantum.Intrinsic`), which returns a `Result` type.</span></span>

<span data-ttu-id="604d6-250">Primeiro, modificamos nossa `Perform3QubitQFT` operação para retornar uma matriz de resultados de medição, `Result[]` em vez de `Unit` .</span><span class="sxs-lookup"><span data-stu-id="604d6-250">First, we modify our `Perform3QubitQFT` operation to return an array of measurement results, `Result[]`, instead of `Unit`.</span></span>

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a><span data-ttu-id="604d6-251">Definir e inicializar `Result[]` matriz</span><span class="sxs-lookup"><span data-stu-id="604d6-251">Define and initialize `Result[]` array</span></span>

<span data-ttu-id="604d6-252">Antes de alocar qubits (ou seja, antes da `using` instrução), declaramos e ligamos essa matriz de comprimento 3 (uma `Result` para cada qubit):</span><span class="sxs-lookup"><span data-stu-id="604d6-252">Before even allocating qubits (i.e. before the `using` statement), we declare and bind this length-3 array (one `Result` for each qubit):</span></span> 

```qsharp
        mutable resultArray = new Result[3];
```

<span data-ttu-id="604d6-253">A `mutable` palavra-chave Preface `resultArray` permite que a variável seja reassociada posteriormente no código---por exemplo, ao adicionar nossos resultados de medição.</span><span class="sxs-lookup"><span data-stu-id="604d6-253">The `mutable` keyword prefacing `resultArray` allows the variable to be rebound later in the code---for example, when adding our measurement results.</span></span>

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a><span data-ttu-id="604d6-254">Executar medidas em um `for` loop e adicionar resultados à matriz</span><span class="sxs-lookup"><span data-stu-id="604d6-254">Perform measurements in a `for` loop and add results to array</span></span>

<span data-ttu-id="604d6-255">Após as operações de transformação de Fourier dentro do `using` bloco, insira o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="604d6-255">After the Fourier transform operations inside the `using` block, insert the following code:</span></span>

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
<span data-ttu-id="604d6-256">A [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) função chamada em uma matriz (por exemplo, nossa matriz de qubits `qs` ) retorna um intervalo sobre os índices da matriz.</span><span class="sxs-lookup"><span data-stu-id="604d6-256">The [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) function called on an array (e.g. our array of qubits, `qs`) returns a range over the indices of the array.</span></span> <span data-ttu-id="604d6-257">Aqui, usamos-o em nosso `for` loop para medir sequencialmente cada qubit usando a `M(qs[i])` instrução.</span><span class="sxs-lookup"><span data-stu-id="604d6-257">Here, we use it in our `for` loop to sequentially measure each qubit using the `M(qs[i])` statement.</span></span>
<span data-ttu-id="604d6-258">Cada tipo medido `Result` ( `Zero` ou `One` ) é então adicionado à posição de índice correspondente em `resultArray` com uma instrução UPDATE-and-REASSIGN.</span><span class="sxs-lookup"><span data-stu-id="604d6-258">Each measured `Result` type (either `Zero` or `One`) is then added to the corresponding index position in `resultArray` with an update-and-reassign statement.</span></span>

> [!NOTE]
> <span data-ttu-id="604d6-259">A sintaxe dessa instrução é exclusiva para Q #, mas corresponde à reatribuição de variável semelhante `resultArray[i] <- M(qs[i])` vista em outras linguagens, como F # e R.</span><span class="sxs-lookup"><span data-stu-id="604d6-259">The syntax of this statement is unique to Q#, but corresponds to the similar variable reassignment `resultArray[i] <- M(qs[i])` seen in other languages such as F# and R.</span></span>

<span data-ttu-id="604d6-260">A palavra-chave `set` é sempre usada para reatribuir variáveis vinculadas usando `mutable` .</span><span class="sxs-lookup"><span data-stu-id="604d6-260">The keyword `set` is always used to reassign variables bound using `mutable`.</span></span>

#### <a name="return-resultarray"></a><span data-ttu-id="604d6-261">Exibir`resultArray`</span><span class="sxs-lookup"><span data-stu-id="604d6-261">Return `resultArray`</span></span>

<span data-ttu-id="604d6-262">Com todos os três qubits medidos e os resultados adicionados ao `resultArray` , somos seguros para redefinir e desalocar os qubits como antes.</span><span class="sxs-lookup"><span data-stu-id="604d6-262">With all three qubits measured and the results added to `resultArray`, we are safe to reset and deallocate the qubits as before.</span></span>
<span data-ttu-id="604d6-263">Após o `using` fechamento do bloco, insira</span><span class="sxs-lookup"><span data-stu-id="604d6-263">After the `using` block's close, insert</span></span>

```qsharp
        return resultArray;
```
<span data-ttu-id="604d6-264">para retornar, por fim, a saída de nossa operação.</span><span class="sxs-lookup"><span data-stu-id="604d6-264">to ultimately return the output of our operation.</span></span> 

### <a name="understanding-the-effects-of-measurement"></a><span data-ttu-id="604d6-265">Compreendendo os efeitos da medição</span><span class="sxs-lookup"><span data-stu-id="604d6-265">Understanding the effects of measurement</span></span>

<span data-ttu-id="604d6-266">Vamos alterar o posicionamento de nossas `DumpMachine` funções para gerar o estado antes e depois das medições.</span><span class="sxs-lookup"><span data-stu-id="604d6-266">Let's change the placement of our `DumpMachine` functions to output the state before and after the measurements.</span></span>
<span data-ttu-id="604d6-267">O código final da operação deve ser semelhante a:</span><span class="sxs-lookup"><span data-stu-id="604d6-267">The final operation code should look like:</span></span> 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

<span data-ttu-id="604d6-268">Se você estiver trabalhando na linha de comando, a matriz retornada será simplesmente impressa diretamente no console no final da execução.</span><span class="sxs-lookup"><span data-stu-id="604d6-268">If you are working from the command line, the returned array will simply be printed directly to the console at the end of the execution.</span></span>
<span data-ttu-id="604d6-269">Caso contrário, atualize o programa de host para processar a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="604d6-269">Otherwise, update your host program to process the returned array.</span></span>

#### <a name="command-line"></a>[<span data-ttu-id="604d6-270">Linha de comando</span><span class="sxs-lookup"><span data-stu-id="604d6-270">Command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="604d6-271">Para ter mais conhecimento da matriz retornada que será impressa no console, podemos adicionar outro `Message` no arquivo Q # antes da `return` instrução:</span><span class="sxs-lookup"><span data-stu-id="604d6-271">To have more understanding of the returned array which will be printed in the console, we can add another `Message` in the Q# file just before the `return` statement:</span></span>

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

<span data-ttu-id="604d6-272">Execute o projeto e a saída deverá ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="604d6-272">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[<span data-ttu-id="604d6-273">Python</span><span class="sxs-lookup"><span data-stu-id="604d6-273">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="604d6-274">Atualize seu programa Python para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="604d6-274">Update your Python program to the following:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

<span data-ttu-id="604d6-275">Execute o arquivo e a saída deverá ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="604d6-275">Run the file, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[<span data-ttu-id="604d6-276">C#</span><span class="sxs-lookup"><span data-stu-id="604d6-276">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="604d6-277">Agora que nossa operação está retornando um resultado, substitua a chamada de método `Wait()` pela busca da `Result` propriedade.</span><span class="sxs-lookup"><span data-stu-id="604d6-277">Now that our operation is returning a result, replace the method call `Wait()` with fetching the `Result` property.</span></span> <span data-ttu-id="604d6-278">Isso ainda realiza o mesmo Synchronicity discutido anteriormente, e podemos associar diretamente esse valor à variável `measurementResult` .</span><span class="sxs-lookup"><span data-stu-id="604d6-278">This still accomplishes the same synchronicity discussed earlier, and we can directly bind this value to the variable `measurementResult`.</span></span>

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="604d6-279">Execute o projeto e a saída deverá ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="604d6-279">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

<span data-ttu-id="604d6-280">Essa saída ilustra algumas coisas diferentes:</span><span class="sxs-lookup"><span data-stu-id="604d6-280">This output illustrates a few different things:</span></span>
1. <span data-ttu-id="604d6-281">Comparando o resultado retornado à medida anterior `DumpMachine` , ele não ilustra _not_ a superposição QFT em relação a Estados de base.</span><span class="sxs-lookup"><span data-stu-id="604d6-281">Comparing the returned result to the pre-measurement `DumpMachine`, it clearly does _not_ illustrate the post-QFT superposition over basis states.</span></span>
    <span data-ttu-id="604d6-282">Uma medida retorna apenas um único estado de base, com uma probabilidade determinada pela amplitude desse Estado no wavefunction do sistema.</span><span class="sxs-lookup"><span data-stu-id="604d6-282">A measurement only returns a single basis state, with a probability determined by the amplitude of that state in the system's wavefunction.</span></span>
2. <span data-ttu-id="604d6-283">Da pós-medição `DumpMachine` , vemos que a medição _altera_ o estado em si, projetando-a da superposição inicial em relação a Estados de base única para o estado de base único que corresponde ao valor medido.</span><span class="sxs-lookup"><span data-stu-id="604d6-283">From the post-measurement `DumpMachine`, we see that measurement _changes_ the state itself, projecting it from the initial superposition over basis states to the single basis state that corresponds to the measured value.</span></span>

<span data-ttu-id="604d6-284">Se tivéssemos de repetir essa operação muitas vezes, veremos que as estatísticas de resultado começam a ilustrar a superposição ponderada igualmente do estado de QFT que dá ao aumento um resultado aleatório em cada imagem.</span><span class="sxs-lookup"><span data-stu-id="604d6-284">If we were to repeat this operation many times, we would see the result statistics begin to illustrate the equally weighted superposition of the post-QFT state that gives rise to a random result on each shot.</span></span>
<span data-ttu-id="604d6-285">_No entanto_, além de serem ineficientes e ainda imperfeitos, isso só reproduziria as amplitudes relativas dos Estados de base, e não as fases relativas entre elas.</span><span class="sxs-lookup"><span data-stu-id="604d6-285">_However_, besides being inefficient and still imperfect, this would nevertheless only reproduce the relative amplitudes of the basis states, not the relative phases between them.</span></span>
<span data-ttu-id="604d6-286">O último não é um problema neste exemplo, mas vemos que as fases relativas aparecem se uma entrada mais complexa fosse fornecida ao QFT do que $ \ket {000} $.</span><span class="sxs-lookup"><span data-stu-id="604d6-286">The latter is not an issue in this example, but we would see relative phases appear if given a more complex input to the QFT than $\ket{000}$.</span></span>

#### <a name="partial-measurements"></a><span data-ttu-id="604d6-287">Medidas parciais</span><span class="sxs-lookup"><span data-stu-id="604d6-287">Partial measurements</span></span> 
<span data-ttu-id="604d6-288">Para explorar como medir apenas algumas qubits do registro pode afetar o estado do sistema, tente adicionar o seguinte dentro do `for` loop, após a linha de medida:</span><span class="sxs-lookup"><span data-stu-id="604d6-288">To explore how measuring only some qubits of the register can affect the system's state, try adding the following inside the `for` loop, after the measurement line:</span></span>
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

<span data-ttu-id="604d6-289">Observe que, para acessar a `IntAsString` função, você precisará adicionar</span><span class="sxs-lookup"><span data-stu-id="604d6-289">Note that to access the `IntAsString` function you will have to add</span></span> 
```qsharp
    open Microsoft.Quantum.Convert;
```
<span data-ttu-id="604d6-290">com o restante das instruções de namespace `open` .</span><span class="sxs-lookup"><span data-stu-id="604d6-290">with the rest of the namespace `open` statements.</span></span>

<span data-ttu-id="604d6-291">Na saída resultante, você verá a projeção gradual em subespaços, uma vez que cada qubit é medido.</span><span class="sxs-lookup"><span data-stu-id="604d6-291">In the resulting output, you will see the gradual projection into subspaces as each qubit is measured.</span></span>


## <a name="use-the-q-libraries"></a><span data-ttu-id="604d6-292">Usar as bibliotecas de Q #</span><span class="sxs-lookup"><span data-stu-id="604d6-292">Use the Q# libraries</span></span>
<span data-ttu-id="604d6-293">Como mencionamos na introdução, grande parte do poder do Q # é o fato de que ele permite abstrair as preocupações de lidar com qubits individuais.</span><span class="sxs-lookup"><span data-stu-id="604d6-293">As we mentioned in the introduction, much of Q#'s power rests in the fact that it allows you to abstract-away the worries of dealing with individual qubits.</span></span>
<span data-ttu-id="604d6-294">Na verdade, se você quiser desenvolver programas Quantum que se aplicam em escala completa, se preocupar com o fato de que uma `H` operação vai antes ou depois de uma rotação específica apenas reduziria você.</span><span class="sxs-lookup"><span data-stu-id="604d6-294">Indeed, if you want to develop full-scale, applicable quantum programs, worrying about whether an `H` operation goes before or after a particular rotation would only slow you down.</span></span> 

<span data-ttu-id="604d6-295">As bibliotecas Q # contêm a operação [QFT](xref:microsoft.quantum.canon.qft) , que você pode simplesmente tomar e aplicar para qualquer número de qubits.</span><span class="sxs-lookup"><span data-stu-id="604d6-295">The Q# libraries contain the [QFT](xref:microsoft.quantum.canon.qft) operation, which you can simply take and apply for any number of qubits.</span></span>
<span data-ttu-id="604d6-296">Para experimentar, defina uma nova operação no arquivo Q # que tem o mesmo conteúdo de `Perform3QubitQFT` , mas com tudo, desde o primeiro `H` até o `SWAP` substituído por duas linhas fáceis:</span><span class="sxs-lookup"><span data-stu-id="604d6-296">To give it a try, define a new operation in your Q# file which has the same contents of `Perform3QubitQFT`, but with everything from the first `H` to the `SWAP` replaced by two easy lines:</span></span>
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
<span data-ttu-id="604d6-297">A primeira linha simplesmente cria uma [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expressão da matriz alocada de qubits, `qs` , que é o que a operação [QFT](xref:microsoft.quantum.canon.qft) utiliza como um argumento.</span><span class="sxs-lookup"><span data-stu-id="604d6-297">The first line simply creates a [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expression of the allocated array of qubits, `qs`, which is what the [QFT](xref:microsoft.quantum.canon.qft) operation takes as an argument.</span></span>
<span data-ttu-id="604d6-298">Isso corresponde à ordenação de índice do qubits no registro.</span><span class="sxs-lookup"><span data-stu-id="604d6-298">This corresponds to index ordering of the qubits in the register.</span></span>

<span data-ttu-id="604d6-299">Para ter acesso a essas operações, adicione `open` instruções para seus respectivos namespaces no início do arquivo Q #:</span><span class="sxs-lookup"><span data-stu-id="604d6-299">To have access to these operations, add `open` statements for their respective namespaces at the beginning of the Q# file:</span></span>
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

<span data-ttu-id="604d6-300">Agora, ajuste o programa de host para chamar o nome da nova operação (por exemplo `PerformIntrinsicQFT` ,) e dê a ele um experimente.</span><span class="sxs-lookup"><span data-stu-id="604d6-300">Now, adjust your host program to call the name of your new operation (e.g. `PerformIntrinsicQFT`), and give it a whirl.</span></span>

<span data-ttu-id="604d6-301">Para ver o verdadeiro benefício de usar as operações da biblioteca do Q #, altere o número de qubits para algo diferente de `3` :</span><span class="sxs-lookup"><span data-stu-id="604d6-301">To see the real benefit of using the Q# library operations, change the number of qubits to something other than `3`:</span></span>
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
<span data-ttu-id="604d6-302">Portanto, você pode aplicar o QFT apropriado para qualquer número determinado de qubits, sem precisar se preocupar com a bagunça de novas `H` operações e rotações em cada qubit.</span><span class="sxs-lookup"><span data-stu-id="604d6-302">You can thus apply the proper QFT for any given number of qubits, without having to worry about the mess of new `H` operations and rotations on each qubit.</span></span>

<span data-ttu-id="604d6-303">Observe que o simulador Quantum leva exponencialmente mais tempo para ser executado à medida que você aumenta o número de qubits---precisamente por que estamos ansiosos para o hardware Quantum real!</span><span class="sxs-lookup"><span data-stu-id="604d6-303">Note that the quantum simulator takes exponentially more time to run as you increase the number of qubits---precisely why we look forward to real quantum hardware!</span></span>













