---
title: Maneiras de executar um Q# programa
description: Visão geral das diferentes maneiras de executar Q# programas. Na linha de comando, Q# notebooks Jupyter e programas de host clássico no Python ou em uma linguagem .net.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8e3fa83700417a4ffaf9e3be91796c9e9513b253
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869725"
---
# <a name="ways-to-run-a-no-locq-program"></a><span data-ttu-id="5c410-104">Maneiras de executar um Q# programa</span><span class="sxs-lookup"><span data-stu-id="5c410-104">Ways to run a Q# program</span></span>

<span data-ttu-id="5c410-105">Um dos maiores pontos fortes do kit de desenvolvimento Quantum é sua flexibilidade entre plataformas e ambientes de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="5c410-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="5c410-106">No entanto, isso também significa que novos Q# usuários podem se encontrar confusos ou sobrecarregados pelas inúmeras opções encontradas no [Guia de instalação](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="5c410-106">However, this also means that new Q# users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="5c410-107">Nesta página, explicamos o que acontece quando um Q# programa é executado e comparamos as diferentes maneiras em que os usuários podem fazer isso.</span><span class="sxs-lookup"><span data-stu-id="5c410-107">On this page, we explain what happens when a Q# program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="5c410-108">Uma distinção principal é que Q# pode ser executada:</span><span class="sxs-lookup"><span data-stu-id="5c410-108">A primary distinction is that Q# can be run:</span></span>
- <span data-ttu-id="5c410-109">como um aplicativo autônomo, onde Q# é o único idioma envolvido e o programa é invocado diretamente.</span><span class="sxs-lookup"><span data-stu-id="5c410-109">as a standalone application, where Q# is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="5c410-110">Dois métodos realmente se enquadram nesta categoria:</span><span class="sxs-lookup"><span data-stu-id="5c410-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="5c410-111">a interface de linha de comando</span><span class="sxs-lookup"><span data-stu-id="5c410-111">the command line interface</span></span>
  - <span data-ttu-id="5c410-112">Q#Blocos de anotações do Jupyter</span><span class="sxs-lookup"><span data-stu-id="5c410-112">Q# Jupyter Notebooks</span></span>
- <span data-ttu-id="5c410-113">com um *programa de host*adicional, escrito em Python ou em uma linguagem .net (por exemplo, C# ou F #), que invoca o programa e pode processar os resultados retornados.</span><span class="sxs-lookup"><span data-stu-id="5c410-113">with an additional *host program*, written in Python or a .NET language (e.g. C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="5c410-114">Para entender melhor esses processos e suas diferenças, consideramos um Q# programa simples e comparamos as maneiras como ele pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="5c410-114">To best understand these processes and their differences, we consider a simple Q# program and compare the ways it can be executed.</span></span>

## <a name="basic-no-locq-program"></a><span data-ttu-id="5c410-115">Q#Programa básico</span><span class="sxs-lookup"><span data-stu-id="5c410-115">Basic Q# program</span></span>

<span data-ttu-id="5c410-116">Um programa Quantum básico pode consistir em preparar um qubit em uma superposição igual de Estados $ \ket {0} $ e $ \ket {1} $, medindo-o e retornando o resultado, que será aleatoriamente um desses dois Estados com probabilidade igual.</span><span class="sxs-lookup"><span data-stu-id="5c410-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="5c410-117">Na verdade, esse processo está no núcleo do início rápido do [gerador de números aleatórios Quantum](xref:microsoft.quantum.quickstarts.qrng) .</span><span class="sxs-lookup"><span data-stu-id="5c410-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="5c410-118">No Q# , isso seria executado pelo seguinte código:</span><span class="sxs-lookup"><span data-stu-id="5c410-118">In Q#, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="5c410-119">No entanto, esse código sozinho não pode ser executado pelo Q# .</span><span class="sxs-lookup"><span data-stu-id="5c410-119">However, this code alone can't be executed by Q#.</span></span>
<span data-ttu-id="5c410-120">Para isso, ele precisa criar o corpo de uma [operação](xref:microsoft.quantum.guide.basics#q-operations-and-functions), que, em seguida, é executado quando chamado---diretamente ou por outra operação.</span><span class="sxs-lookup"><span data-stu-id="5c410-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.guide.basics#q-operations-and-functions), which is then executed when called---either directly or by another operation.</span></span> <span data-ttu-id="5c410-121">Portanto, você pode escrever uma operação do seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="5c410-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="5c410-122">Você definiu uma operação, `MeasureSuperposition` , que não recebe entradas e retorna um valor do tipo [Result](xref:microsoft.quantum.guide.types).</span><span class="sxs-lookup"><span data-stu-id="5c410-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="5c410-123">Embora os exemplos nesta página consistam apenas em Q# *operações*, todos os conceitos que discutiremos referem-se igualmente às Q# *funções*e, portanto, nos referimos a elas coletivamente como *chamáveis*.</span><span class="sxs-lookup"><span data-stu-id="5c410-123">While the examples on this page only consist of Q# *operations*, all of the concepts we will discuss pertain equally to Q# *functions*, and therefore we refer to them collectively as *callables*.</span></span> <span data-ttu-id="5c410-124">Suas diferenças são discutidas em [ Q# noções básicas: operações e funções](xref:microsoft.quantum.guide.basics#q-operations-and-functions), e mais detalhes sobre como defini-las podem ser encontrados em [operações e funções](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="5c410-124">Their differences are discussed at [Q# basics: operations and functions](xref:microsoft.quantum.guide.basics#q-operations-and-functions), and more details on defining them can be found at [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

### <a name="callable-defined-in-a-no-locq-file"></a><span data-ttu-id="5c410-125">Callable definido em um Q# arquivo</span><span class="sxs-lookup"><span data-stu-id="5c410-125">Callable defined in a Q# file</span></span>

<span data-ttu-id="5c410-126">O callable é precisamente o que é chamado e executado pelo Q# .</span><span class="sxs-lookup"><span data-stu-id="5c410-126">The callable is precisely what's called and run by Q#.</span></span>
<span data-ttu-id="5c410-127">No entanto, ele requer mais algumas adições para compor um `*.qs` Q# arquivo completo.</span><span class="sxs-lookup"><span data-stu-id="5c410-127">However, it requires a few more additions to comprise a full `*.qs` Q# file.</span></span>

<span data-ttu-id="5c410-128">Todos os Q# tipos e os chamados (aqueles que você define e os intrínsecos ao idioma) são definidos em *namespaces*, que fornecem a cada um um nome completo que pode ser referenciado.</span><span class="sxs-lookup"><span data-stu-id="5c410-128">All Q# types and callables (both those you define and those intrinsic to the language) are defined within *namespaces*, which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="5c410-129">Por exemplo, as [`H`](xref:microsoft.quantum.intrinsic.h) [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) operações e são encontradas nos [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) namespaces e (parte das [ Q# bibliotecas padrão](xref:microsoft.quantum.qsharplibintro)).</span><span class="sxs-lookup"><span data-stu-id="5c410-129">For example, the [`H`](xref:microsoft.quantum.intrinsic.h) and [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) namespaces (part of the [Q# Standard Libraries](xref:microsoft.quantum.qsharplibintro)).</span></span>
<span data-ttu-id="5c410-130">Assim, eles sempre podem ser chamados por meio de *full* seus nomes completos `Microsoft.Quantum.Intrinsic.H(<qubit>)` e `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` , mas sempre fazer isso levaria a um código muito confuso.</span><span class="sxs-lookup"><span data-stu-id="5c410-130">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="5c410-131">Em vez disso, `open` as instruções permitem que os chamadores sejam referenciados com uma abreviação mais concisa, como fizemos no corpo da operação acima.</span><span class="sxs-lookup"><span data-stu-id="5c410-131">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="5c410-132">Portanto, o Q# arquivo completo que contém nossa operação consistiria em definir nosso próprio namespace, abrir os namespaces para aqueles que são chamados pela operação e, em seguida, nossa operação:</span><span class="sxs-lookup"><span data-stu-id="5c410-132">The full Q# file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="5c410-133">Os namespaces também podem ser *alias* quando abertos, o que pode ser útil se os nomes de tipo/callable em dois namespaces entrarem em conflito.</span><span class="sxs-lookup"><span data-stu-id="5c410-133">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="5c410-134">Por exemplo, poderíamos usar `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` acima e, em seguida, chamar `H` via `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="5c410-134">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="5c410-135">Uma exceção a tudo disso é o [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) namespace, que é sempre aberto automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5c410-135">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="5c410-136">Portanto, os chamadores como o [`Length`](xref:microsoft.quantum.core.length) sempre podem ser usados diretamente.</span><span class="sxs-lookup"><span data-stu-id="5c410-136">Therefore, callables like [`Length`](xref:microsoft.quantum.core.length) can always be used directly.</span></span>

### <a name="execution-on-target-machines"></a><span data-ttu-id="5c410-137">Execução em computadores de destino</span><span class="sxs-lookup"><span data-stu-id="5c410-137">Execution on target machines</span></span>

<span data-ttu-id="5c410-138">Agora o modelo de execução geral de um Q# programa fica claro.</span><span class="sxs-lookup"><span data-stu-id="5c410-138">Now the general execution model of a Q# program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

<span data-ttu-id="5c410-139">Em primeiro lugar, o resgatável específico a ser executado tem acesso a quaisquer outros chamados e tipos definidos no mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="5c410-139">Firstly, the specific callable to be executed has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="5c410-140">Ele também acessa aqueles de qualquer uma das [ Q# bibliotecas](xref:microsoft.quantum.libraries), mas eles devem ser referenciados por meio de seu nome completo ou por meio do uso de `open` instruções descritas acima.</span><span class="sxs-lookup"><span data-stu-id="5c410-140">It also access those from any of the [Q# libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="5c410-141">O próprio callable é executado em um *[computador de destino](xref:microsoft.quantum.machines)*.</span><span class="sxs-lookup"><span data-stu-id="5c410-141">The callable itself is then executed on a *[target machine](xref:microsoft.quantum.machines)*.</span></span>
<span data-ttu-id="5c410-142">Esses computadores de destino podem ser hardwares de Quantum reais ou vários simuladores disponíveis como parte do QDK.</span><span class="sxs-lookup"><span data-stu-id="5c410-142">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="5c410-143">Para nossos objetivos aqui, a máquina de destino mais útil é uma instância do [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` , que calcula o comportamento do programa como se ele estivesse sendo executado em um computador Quantum sem ruído.</span><span class="sxs-lookup"><span data-stu-id="5c410-143">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being executed on a noise-free quantum computer.</span></span>

<span data-ttu-id="5c410-144">Até agora, descrevemos o que acontece quando um Q# resgatável específico está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="5c410-144">So far, we've described what happens when a specific Q# callable is being executed.</span></span>
<span data-ttu-id="5c410-145">Independentemente de Q# ser usado em um aplicativo autônomo ou com um programa host, esse processo geral é mais ou menos o mesmo---, portanto, a flexibilidade do QDK.</span><span class="sxs-lookup"><span data-stu-id="5c410-145">Regardless of whether Q# is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="5c410-146">As diferenças entre as diferentes maneiras de chamar o kit de desenvolvimento Quantum, portanto, se revelam *sobre como* esse Q# callable é chamado para ser executado e de que maneira todos os resultados são retornados.</span><span class="sxs-lookup"><span data-stu-id="5c410-146">The differences between the different ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that Q# callable is called to be executed, and in what manner any results are returned.</span></span>
<span data-ttu-id="5c410-147">Mais especificamente, as diferenças giram em volta</span><span class="sxs-lookup"><span data-stu-id="5c410-147">More specifically, the differences revolve around</span></span> 
1. <span data-ttu-id="5c410-148">indicando qual Q# callable deve ser executado,</span><span class="sxs-lookup"><span data-stu-id="5c410-148">indicating which Q# callable is to be executed,</span></span>
2. <span data-ttu-id="5c410-149">como possíveis argumentos chamáveis são fornecidos,</span><span class="sxs-lookup"><span data-stu-id="5c410-149">how potential callable arguments are provided,</span></span>
3. <span data-ttu-id="5c410-150">especificando o computador de destino no qual será executado, e</span><span class="sxs-lookup"><span data-stu-id="5c410-150">specifying the target machine on which to execute it, and</span></span>
4. <span data-ttu-id="5c410-151">como os resultados são retornados.</span><span class="sxs-lookup"><span data-stu-id="5c410-151">how any results are returned.</span></span>

<span data-ttu-id="5c410-152">Primeiro, discutimos como isso é feito com o Q# aplicativo autônomo na linha de comando e, em seguida, usamos os programas de host Python e C#.</span><span class="sxs-lookup"><span data-stu-id="5c410-152">First, we discuss how this is done with the Q# standalone application from the command line, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="5c410-153">Reservamos o aplicativo autônomo de Q# notebooks Jupyter para o último, porque ao contrário dos três primeiros, a funcionalidade principal não é centralizada em um Q# arquivo local.</span><span class="sxs-lookup"><span data-stu-id="5c410-153">We reserve the standalone application of Q# Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local Q# file.</span></span>

> [!NOTE]
> <span data-ttu-id="5c410-154">Embora não o ilustre nesses exemplos, uma semelhança entre os métodos de execução é que todas as mensagens impressas dentro do Q# programa (por [`Message`](xref:microsoft.quantum.intrinsic.message) [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) exemplo, ou) normalmente serão sempre impressas no respectivo console.</span><span class="sxs-lookup"><span data-stu-id="5c410-154">Although we don't illustrate it in these examples, one commonality between the execution methods is that any messages printed from inside the Q# program (by way of [`Message`](xref:microsoft.quantum.intrinsic.message) or [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="no-locq-from-the-command-line"></a><span data-ttu-id="5c410-155">Q#na linha de comando</span><span class="sxs-lookup"><span data-stu-id="5c410-155">Q# from the command line</span></span>
<span data-ttu-id="5c410-156">Uma das maneiras mais fáceis de começar a escrever Q# programas é evitar a preocupação com arquivos separados e uma segunda linguagem completamente.</span><span class="sxs-lookup"><span data-stu-id="5c410-156">One of the easiest ways to get started writing Q# programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="5c410-157">O uso do Visual Studio Code ou do Visual Studio com a extensão QDK permite um fluxo de trabalho contínuo no qual executamos o Q# callable de apenas um único Q# arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-157">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run Q# callables from only a single Q# file.</span></span>

<span data-ttu-id="5c410-158">Para isso, finalmente invocaremos a execução do programa digitando</span><span class="sxs-lookup"><span data-stu-id="5c410-158">For this, we will ultimately invoke the program's execution by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="5c410-159">na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5c410-159">in the command line.</span></span>
<span data-ttu-id="5c410-160">O fluxo de trabalho mais simples é quando o local do diretório do terminal é o mesmo que o Q# arquivo, que pode ser facilmente manipulado junto com Q# a edição de arquivos usando o terminal integrado no vs Code, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="5c410-160">The simplest workflow is when the terminal's directory location is the same as the Q# file, which can be easily handled alongside Q# file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="5c410-161">No entanto, o [ `dotnet run` comando](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) aceita inúmeras opções e o programa também pode ser executado de um local diferente, simplesmente fornecendo `--project <PATH>` o local do Q# arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-161">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the Q# file.</span></span>


### <a name="add-entry-point-to-no-locq-file"></a><span data-ttu-id="5c410-162">Adicionar ponto de entrada ao Q# arquivo</span><span class="sxs-lookup"><span data-stu-id="5c410-162">Add entry point to Q# file</span></span>

<span data-ttu-id="5c410-163">A maioria dos arquivos conterá Q# mais de um callable, por isso naturalmente, precisamos permitir que o compilador saiba o *que* pode ser executado ao fornecer o `dotnet run` comando.</span><span class="sxs-lookup"><span data-stu-id="5c410-163">Most Q# files will contain more than one callable, so naturally we need to let the compiler know *which* callable to execute when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="5c410-164">Isso é feito com uma simples alteração no Q# próprio arquivo:</span><span class="sxs-lookup"><span data-stu-id="5c410-164">This is done with a simple change to the Q# file itself:</span></span> 
    - <span data-ttu-id="5c410-165">Adicione uma linha com `@EntryPoint()` diretamente antes do callable.</span><span class="sxs-lookup"><span data-stu-id="5c410-165">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="5c410-166">Portanto, nosso arquivo acima se tornaria</span><span class="sxs-lookup"><span data-stu-id="5c410-166">Our file from above would therefore become</span></span>
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

<span data-ttu-id="5c410-167">Agora, uma chamada de `dotnet run` da linha de comando leva a ser `MeasureSuperposition` executada e o valor retornado é impresso diretamente no terminal.</span><span class="sxs-lookup"><span data-stu-id="5c410-167">Now, a call of `dotnet run` from the command line leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="5c410-168">Portanto, você verá ou será `One` `Zero` impresso.</span><span class="sxs-lookup"><span data-stu-id="5c410-168">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="5c410-169">Observe que não importa se você tiver mais chamadores definidos abaixo dele, somente `MeasureSuperposition` será executado.</span><span class="sxs-lookup"><span data-stu-id="5c410-169">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="5c410-170">Além disso, não é problema se seu callable incluir [comentários de documentação](xref:microsoft.quantum.guide.filestructure#documentation-comments) antes de sua declaração, o `@EntryPoint()` atributo pode ser simplesmente colocado acima deles.</span><span class="sxs-lookup"><span data-stu-id="5c410-170">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.guide.filestructure#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="5c410-171">Argumentos que podem ser chamados</span><span class="sxs-lookup"><span data-stu-id="5c410-171">Callable arguments</span></span>

<span data-ttu-id="5c410-172">Até agora, consideramos apenas uma operação que não usa entradas.</span><span class="sxs-lookup"><span data-stu-id="5c410-172">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="5c410-173">Suponha que queríamos executar uma operação semelhante, mas em várias qubits---o número de que é fornecido como um argumento.</span><span class="sxs-lookup"><span data-stu-id="5c410-173">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="5c410-174">Tal operação poderia ser gravada como</span><span class="sxs-lookup"><span data-stu-id="5c410-174">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="5c410-175">onde o valor retornado é uma matriz dos resultados da medição.</span><span class="sxs-lookup"><span data-stu-id="5c410-175">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="5c410-176">Observe que [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) e [`ForEach`](xref:microsoft.quantum.arrays.foreach) estão nos [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) namespaces e, exigindo instruções adicionais `open` para cada um.</span><span class="sxs-lookup"><span data-stu-id="5c410-176">Note that [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) and [`ForEach`](xref:microsoft.quantum.arrays.foreach) are in the [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) and [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="5c410-177">Se movermos o `@EntryPoint()` atributo para preceder essa nova operação (Observe que só pode haver uma linha em um arquivo), tentar executá-la com simplesmente `dotnet run` resulta em uma mensagem de erro que indica quais opções de linha de comando adicionais são necessárias e como expressá-las.</span><span class="sxs-lookup"><span data-stu-id="5c410-177">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command line options are required, and how to express them.</span></span>

<span data-ttu-id="5c410-178">O formato geral para a linha de comando é realmente `dotnet run [options]` , e os argumentos que podem ser chamados são fornecidos lá.</span><span class="sxs-lookup"><span data-stu-id="5c410-178">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="5c410-179">Nesse caso, o argumento `n` está ausente e mostra que precisamos fornecer a opção `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="5c410-179">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="5c410-180">Para executar o `MeasureSuperpositionArray` para `n=4` qubits, portanto, usamos</span><span class="sxs-lookup"><span data-stu-id="5c410-180">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="5c410-181">produzindo uma saída semelhante a</span><span class="sxs-lookup"><span data-stu-id="5c410-181">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="5c410-182">É claro que isso se estende a vários argumentos.</span><span class="sxs-lookup"><span data-stu-id="5c410-182">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="5c410-183">Os nomes de argumentos definidos em `camelCase` são ligeiramente alterados pelo compilador para serem aceitos como Q# entradas.</span><span class="sxs-lookup"><span data-stu-id="5c410-183">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as Q# inputs.</span></span> <span data-ttu-id="5c410-184">Por exemplo, se em vez de `n` , usamos o nome `numQubits` acima, essa entrada seria fornecida na linha de comando via `--num-qubits 4` em vez de `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="5c410-184">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="5c410-185">A mensagem de erro também fornece outras opções que podem ser usadas, incluindo como alterar o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="5c410-185">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="5c410-186">Computadores de destino diferentes</span><span class="sxs-lookup"><span data-stu-id="5c410-186">Different target machines</span></span>

<span data-ttu-id="5c410-187">Como as saídas de nossas operações até agora têm sido os resultados esperados de sua ação em qubits reais, fica claro que o computador de destino padrão da linha de comando é o simulador de quauntum de estado completo, `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="5c410-187">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quauntum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="5c410-188">No entanto, podemos instruir os chamadores a serem executados em um computador de destino específico com a opção `--simulator` (ou a abreviação `-s` ).</span><span class="sxs-lookup"><span data-stu-id="5c410-188">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="5c410-189">Por exemplo, poderíamos executá-lo em [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :</span><span class="sxs-lookup"><span data-stu-id="5c410-189">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="5c410-190">A saída impressa é, então,</span><span class="sxs-lookup"><span data-stu-id="5c410-190">The printed output is then</span></span>

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

<span data-ttu-id="5c410-191">Para obter detalhes sobre o que essas métricas indicam, consulte [avaliador de recursos: métricas relatadas](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span><span class="sxs-lookup"><span data-stu-id="5c410-191">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-execution-summary"></a><span data-ttu-id="5c410-192">Resumo da execução de linha de comando</span><span class="sxs-lookup"><span data-stu-id="5c410-192">Command line execution summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a><span data-ttu-id="5c410-193">Não Q# `dotnet run` Opções</span><span class="sxs-lookup"><span data-stu-id="5c410-193">Non-Q# `dotnet run` options</span></span>

<span data-ttu-id="5c410-194">Como mencionamos brevemente acima com a `--project` opção, o [ `dotnet run` comando](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) também aceita opções não relacionadas aos argumentos que podem ser Q# chamados.</span><span class="sxs-lookup"><span data-stu-id="5c410-194">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the Q# callable arguments.</span></span>
<span data-ttu-id="5c410-195">Se fornecer ambos os tipos de opções, as `dotnet` opções específicas deverão ser fornecidas primeiro, seguidas por um delimitador `--` e, em seguida, as Q# opções específicas.</span><span class="sxs-lookup"><span data-stu-id="5c410-195">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the Q#-specific options.</span></span>
<span data-ttu-id="5c410-196">Por exemplo, especificar um caminho junto com um número qubits para a operação acima seria executado via `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="5c410-196">For example, specifiying a path along with a number qubits for the operation above would be executed via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="no-locq-with-host-programs"></a><span data-ttu-id="5c410-197">Q#com programas de host</span><span class="sxs-lookup"><span data-stu-id="5c410-197">Q# with host programs</span></span>

<span data-ttu-id="5c410-198">Com Q# o arquivo em mãos, uma alternativa à chamada de uma operação ou função diretamente da linha de comando é usar um *programa de host* em outra linguagem clássica.</span><span class="sxs-lookup"><span data-stu-id="5c410-198">With our Q# file in hand, an alternative to calling an operation or function directly from the command line is to use a *host program* in another classical language.</span></span> <span data-ttu-id="5c410-199">Especificamente, isso pode ser feito com Python ou uma linguagem .NET, como C# ou F # (para fins de brevidade, só detalharemos C# aqui).</span><span class="sxs-lookup"><span data-stu-id="5c410-199">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="5c410-200">Um pouco mais de configuração é necessário para habilitar a interoperabilidade, mas esses detalhes podem ser encontrados nos [guias de instalação](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="5c410-200">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="5c410-201">Resumindo, a situação agora inclui um arquivo de programa host (por exemplo, `*.py` ou `*.cs` ) no mesmo local que o nosso Q# arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-201">In a nutshell, the situation now includes a host program file (e.g. `*.py` or `*.cs`) in the same location as our Q# file.</span></span>
<span data-ttu-id="5c410-202">Agora é o programa *host* que é executado e, no decorrer da sua execução, ele pode chamar Q# operações e funções específicas do Q# arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-202">It's now the *host* program that gets run, and in the course of its execution it can call specific Q# operations and functions from the Q# file.</span></span>
<span data-ttu-id="5c410-203">O núcleo da interoperabilidade se baseia no Q# compilador, tornando o conteúdo do Q# arquivo acessível ao programa host para que ele possa ser chamado.</span><span class="sxs-lookup"><span data-stu-id="5c410-203">The core of the interoperability is based on the Q# compiler making the contents of the Q# file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="5c410-204">Um dos principais benefícios do uso de um programa de host é que os dados clássicos retornados pelo Q# programa podem ser processados ainda mais no idioma do host.</span><span class="sxs-lookup"><span data-stu-id="5c410-204">One of the main benefits of using a host program is that the classical data returned by the Q# program can then be further processed in the host language.</span></span>
<span data-ttu-id="5c410-205">Isso pode consistir em um processamento de dados avançado (por exemplo, algo que não pode ser executado internamente no Q# ) e, em seguida, chamar Q# ações adicionais com base nesses resultados ou algo tão simples quanto plotar os Q# resultados.</span><span class="sxs-lookup"><span data-stu-id="5c410-205">This could consist of some advanced data processing (e.g. something that can't be performed internally in Q#), and then calling further Q# actions based on those results, or something as simple as plotting the Q# results.</span></span>

<span data-ttu-id="5c410-206">O esquema geral é mostrado aqui e discutimos as implementações específicas para Python e C# abaixo.</span><span class="sxs-lookup"><span data-stu-id="5c410-206">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="5c410-207">Um exemplo que usa um programa de host F # pode ser encontrado em [exemplos de interoperabilidade .net](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="5c410-207">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="5c410-208">O `@EntryPoint()` atributo usado para Q# aplicativos de linha de comando não pode ser usado com programas de host.</span><span class="sxs-lookup"><span data-stu-id="5c410-208">The `@EntryPoint()` attribute used for Q# command line applications cannot be used with host programs.</span></span>
> <span data-ttu-id="5c410-209">Um erro será gerado se estiver presente no Q# arquivo que está sendo chamado por um host.</span><span class="sxs-lookup"><span data-stu-id="5c410-209">An error will be raised if it is present in the Q# file being called by a host.</span></span> 

<span data-ttu-id="5c410-210">Para trabalhar com diferentes programas de host, não há nenhuma alteração necessária para um `*.qs` Q# arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-210">To work with different host programs, there are no changes required to a `*.qs` Q# file.</span></span>
<span data-ttu-id="5c410-211">As implementações do programa host a seguir funcionam com o mesmo Q# arquivo:</span><span class="sxs-lookup"><span data-stu-id="5c410-211">The following host program implementations all work with the same Q# file:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

<span data-ttu-id="5c410-212">Selecione a guia correspondente ao seu idioma de host de interesse.</span><span class="sxs-lookup"><span data-stu-id="5c410-212">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="5c410-213">Python</span><span class="sxs-lookup"><span data-stu-id="5c410-213">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="5c410-214">Um programa de host do Python é construído da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5c410-214">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="5c410-215">Importe o `qsharp` módulo, que registra o carregador de módulo para Q# interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="5c410-215">Import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="5c410-216">Isso permite que Q# os namespaces apareçam como módulos Python, dos quais podemos "importar" Q# chamados.</span><span class="sxs-lookup"><span data-stu-id="5c410-216">This allows Q# namespaces to appear as Python modules, from which we can "import" Q# callables.</span></span>
    <span data-ttu-id="5c410-217">Observe que, tecnicamente, não são os Q# próprios chamados que são importados, mas, em vez disso, os stubs do Python que permitem chamá-los.</span><span class="sxs-lookup"><span data-stu-id="5c410-217">Note that it is technically not the Q# callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="5c410-218">Eles se comportam como objetos de classes python, nos quais usamos métodos para especificar os computadores de destino para os quais enviar a operação para execução.</span><span class="sxs-lookup"><span data-stu-id="5c410-218">These then behave as objects of Python classes, on which we use methods to specify the target machines to send the operation to for execution.</span></span>

2. <span data-ttu-id="5c410-219">Importe os Q# chamados que invocaremos diretamente---nesse caso, `MeasureSuperposition` e `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="5c410-219">Import those Q# callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="5c410-220">Com o `qsharp` módulo importado, você também pode importar os chamadores diretamente dos Q# namespaces da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5c410-220">With the `qsharp` module imported, you can also import callables directly from the Q# library namespaces.</span></span>

3. <span data-ttu-id="5c410-221">Entre qualquer outro código Python, agora você pode chamar aqueles que podem ser chamados em computadores de destino específicos e atribuir seus retornos a variáveis (se eles retornarem um valor) para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="5c410-221">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="5c410-222">Especificando computadores de destino</span><span class="sxs-lookup"><span data-stu-id="5c410-222">Specifying target machines</span></span>
<span data-ttu-id="5c410-223">Chamar uma operação a ser executada em um computador de destino específico é feito por meio de métodos de Python diferentes no objeto importado.</span><span class="sxs-lookup"><span data-stu-id="5c410-223">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="5c410-224">Por exemplo, `.simulate(<args>)` , usa o `QuantumSimulator` para executar a operação, enquanto `.estimate_resources(<args>)` faz isso no `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="5c410-224">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="5c410-225">Passando entradas para Q\#</span><span class="sxs-lookup"><span data-stu-id="5c410-225">Passing inputs to Q\#</span></span>
<span data-ttu-id="5c410-226">Os argumentos para o Q# callable devem ser fornecidos na forma de um argumento de palavra-chave, em que a palavra-chave é o nome do argumento na definição que pode ser Q# chamada.</span><span class="sxs-lookup"><span data-stu-id="5c410-226">Arguments for the Q# callable should be provided in the form of a keyword argument, where the keyword is the argument name in the Q# callable definition.</span></span>
<span data-ttu-id="5c410-227">Ou seja, `MeasureSuperpositionArray.simulate(n=4)` é válido, enquanto `MeasureSuperpositionArray.simulate(4)` geraria um erro.</span><span class="sxs-lookup"><span data-stu-id="5c410-227">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="5c410-228">Portanto, o programa de host do Python</span><span class="sxs-lookup"><span data-stu-id="5c410-228">Therefore, the Python host program</span></span> 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

<span data-ttu-id="5c410-229">resulta em uma saída semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="5c410-229">results in an output like the following:</span></span>

```python
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

### <a name="c"></a>[<span data-ttu-id="5c410-230">C#</span><span class="sxs-lookup"><span data-stu-id="5c410-230">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="5c410-231">Um programa de host C# tem vários componentes e funciona muito bem com alguns componentes do QDK, como os simuladores, que são criados em C#.</span><span class="sxs-lookup"><span data-stu-id="5c410-231">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="5c410-232">O Q# compilador funciona aqui gerando um namespace C# nomeado de maneira equivalente do Q# namespace em nosso Q# arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-232">The Q# compiler works here by generating an equivalently named C# namespace from the Q# namespace in our Q# file.</span></span>
<span data-ttu-id="5c410-233">Ele gera ainda mais uma classe C# nomeada de maneira equivalente para cada um dos Q# chamados ou tipos definidos por aí.</span><span class="sxs-lookup"><span data-stu-id="5c410-233">It further generates an equivalently named C# class for each of the Q# callables or types defined therein.</span></span>

<span data-ttu-id="5c410-234">Primeiro, fazemos todas as classes usadas em nosso programa host disponível com `using` instruções, que são aproximadamente análogo para as `open` instruções em nosso Q# arquivo:</span><span class="sxs-lookup"><span data-stu-id="5c410-234">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our Q# file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

<span data-ttu-id="5c410-235">Em seguida, declaramos nosso namespace C#, alguns outros bits e partes (Confira o bloco de código completo abaixo) e, em seguida, qualquer programação clássica que desejamos (por exemplo, computação de argumentos para os Q# chamadores).</span><span class="sxs-lookup"><span data-stu-id="5c410-235">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (e.g. computing arguments for the Q# callables).</span></span>
<span data-ttu-id="5c410-236">O último não é necessário em nosso caso, mas um exemplo desse uso pode ser encontrado no [exemplo de interoperabilidade do .net](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="5c410-236">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="5c410-237">Computadores de destino</span><span class="sxs-lookup"><span data-stu-id="5c410-237">Target machines</span></span>

<span data-ttu-id="5c410-238">Voltando para Q# , devemos criar uma instância de qualquer máquina de destino em que executaremos nossas operações.</span><span class="sxs-lookup"><span data-stu-id="5c410-238">Getting back to Q#, we must create an instance of whatever target machine we will execute our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="5c410-239">O uso de outros computadores de destino é tão simples quanto criar uma instância de um diferente, embora a maneira de fazer isso e processar os retornos possa ser um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="5c410-239">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="5c410-240">Para fins de brevidade, vamos para o [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) por enquanto, e incluímos o [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [seguinte](#including-the-resources-estimator).</span><span class="sxs-lookup"><span data-stu-id="5c410-240">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="5c410-241">Cada classe C# gerada a partir das Q# operações tem um `Run` método, o primeiro argumento do qual deve ser a instância do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="5c410-241">Each C# class generated from the Q# operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="5c410-242">Portanto, para executar `MeasureSuperposition` no `QuantumSimulator` , usamos `MeasureSuperposition.Run(sim)` .</span><span class="sxs-lookup"><span data-stu-id="5c410-242">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="5c410-243">Os resultados retornados podem então ser atribuídos a variáveis em C#:</span><span class="sxs-lookup"><span data-stu-id="5c410-243">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="5c410-244">O `Run` método é executado de forma assíncrona porque esse será o caso de hardware Quantum real e, portanto, a `await` palavra-chave bloqueará a execução adicional até que a tarefa seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5c410-244">The `Run` method is executed asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further execution until the task completes.</span></span>

<span data-ttu-id="5c410-245">Se o Q# callable não tiver nenhum retorno (ou seja, tiver tipo de retorno `Unit` ), a execução ainda poderá ser feita da mesma maneira sem atribuí-lo a uma variável.</span><span class="sxs-lookup"><span data-stu-id="5c410-245">If the Q# callable does not have any returns (i.e. has return type `Unit`), then the execution can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="5c410-246">Nesse caso, a linha inteira consistiria simplesmente de</span><span class="sxs-lookup"><span data-stu-id="5c410-246">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="5c410-247">Argumentos</span><span class="sxs-lookup"><span data-stu-id="5c410-247">Arguments</span></span>

<span data-ttu-id="5c410-248">Todos os argumentos para o Q# callable são simplesmente passados como argumentos adicionais após o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="5c410-248">Any arguments to the Q# callable are simply passed as additional arguments afer the target machine.</span></span>
<span data-ttu-id="5c410-249">Portanto, os resultados de `MeasureSuperpositionArray` em `n=4` qubits seriam buscados por meio de</span><span class="sxs-lookup"><span data-stu-id="5c410-249">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="5c410-250">Um programa completo de host C# poderia, portanto, parecer</span><span class="sxs-lookup"><span data-stu-id="5c410-250">A full C# host program could thus look like</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

<span data-ttu-id="5c410-251">No local do arquivo C#, o programa de host pode ser executado na linha de comando digitando</span><span class="sxs-lookup"><span data-stu-id="5c410-251">At the location of the C# file, the host program can be run from the command line by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="5c410-252">e, nesse caso, você verá a saída gravada no console semelhante a</span><span class="sxs-lookup"><span data-stu-id="5c410-252">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="5c410-253">Devido à interoperabilidade do compilador com namespaces, podemos também tornar nossos Q# callableable disponíveis sem a `using NamespaceName;` instrução e simplesmente corresponder o título do namespace do C# a ele.</span><span class="sxs-lookup"><span data-stu-id="5c410-253">Due to the compiler's interoperability with namespaces, we could alternatively make our Q# callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="5c410-254">Ou seja, substituindo `namespace host` por `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="5c410-254">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="5c410-255">Incluindo o estimador de recursos</span><span class="sxs-lookup"><span data-stu-id="5c410-255">Including the resources estimator</span></span>

<span data-ttu-id="5c410-256">O [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requer uma implementação um pouco diferente para recuperar a saída.</span><span class="sxs-lookup"><span data-stu-id="5c410-256">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="5c410-257">Em primeiro lugar, em vez de instanciá-los como uma variável com uma `using` instrução (como fazemos com o `QuantumSimulator` ), nós criamos mais diretamente objetos da classe por meio de</span><span class="sxs-lookup"><span data-stu-id="5c410-257">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="5c410-258">Observe que, em vez de um único simulador de destino ser usado por várias Q# operações, criamos uma instância de cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="5c410-258">Notice that instead of a single target simulator to be used by multiple Q# operations, we have instantiated one for each.</span></span> <span data-ttu-id="5c410-259">Isso ocorre porque os próprios objetos são modificados quando usados como computadores de destino, e seus resultados podem ser recuperados posteriormente com o método de classe `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="5c410-259">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="5c410-260">Para executar as operações nos estimadores de recursos, usamos</span><span class="sxs-lookup"><span data-stu-id="5c410-260">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="5c410-261">e, em seguida, busque os resultados como valores separados por tabulação (TSV) com `estimatorSingleQ.ToTSV()` e `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="5c410-261">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="5c410-262">Portanto, um programa de host C# completo que usa ambos `QuantumSimulator` e `ResourcesEstimator` poderia ter a forma:</span><span class="sxs-lookup"><span data-stu-id="5c410-262">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


<span data-ttu-id="5c410-263">que produziria uma saída semelhante a</span><span class="sxs-lookup"><span data-stu-id="5c410-263">which would yield output similar to</span></span>

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="no-locq-jupyter-notebooks"></a><span data-ttu-id="5c410-264">Q#Blocos de anotações do Jupyter</span><span class="sxs-lookup"><span data-stu-id="5c410-264">Q# Jupyter Notebooks</span></span>
<span data-ttu-id="5c410-265">Q#Os notebooks Jupyter usam o kernel I Q# , que permite que você defina, compile e execute o Q# callables em um único bloco de anotações---tudo junto com instruções, observações e outros conteúdos.</span><span class="sxs-lookup"><span data-stu-id="5c410-265">Q# Jupyter Notebooks make use of the IQ# kernel, which allows you to define, compile, and run Q# callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="5c410-266">Isso significa que, embora seja possível importar e usar o conteúdo dos `*.qs` Q# arquivos, eles não são necessários no modelo de execução.</span><span class="sxs-lookup"><span data-stu-id="5c410-266">This means that while it is possible to import and use the contents of `*.qs` Q# files, they are not necessary in the execution model.</span></span>

<span data-ttu-id="5c410-267">Aqui, detalharemos como executar as Q# operações definidas acima, mas uma introdução mais ampla ao uso de Q# notebooks Jupyter é fornecida em [introdução aos Q# blocos de anotações e Jupyter](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span><span class="sxs-lookup"><span data-stu-id="5c410-267">Here, we will detail how to run the Q# operations defined above, but a more broad introduction to using Q# Jupyter Notebooks is provided at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="5c410-268">Definindo operações</span><span class="sxs-lookup"><span data-stu-id="5c410-268">Defining operations</span></span>

<span data-ttu-id="5c410-269">Em uma Q# Jupyter notebook, você insere Q# o código da mesma forma que faria dentro do namespace de um Q# arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-269">In a Q# Jupyter Notebook, you enter Q# code just as we would from inside the namespace of a Q# file.</span></span>

<span data-ttu-id="5c410-270">Portanto, podemos habilitar o acesso a callables a partir das [ Q# bibliotecas padrão](xref:microsoft.quantum.qsharplibintro) com `open` instruções para seus respectivos namespaces.</span><span class="sxs-lookup"><span data-stu-id="5c410-270">So, we can enable access to callables from the [Q# standard libraries](xref:microsoft.quantum.qsharplibintro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="5c410-271">Após a execução de uma célula com tal instrução, as definições desses namespaces estão disponíveis em todo o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c410-271">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="5c410-272">Os chamados de [Microsoft. Quantum. intrínseca](xref:microsoft.quantum.intrinsic) e [Microsoft. Quantum. Canon](xref:microsoft.quantum.canon) (por exemplo, [`H`](xref:microsoft.quantum.intrinsic.h) e [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) ficam automaticamente disponíveis para operações definidas nas células de Q# notebooks Jupyter.</span><span class="sxs-lookup"><span data-stu-id="5c410-272">Callables from [Microsoft.Quantum.Intrinsic](xref:microsoft.quantum.intrinsic) and [Microsoft.Quantum.Canon](xref:microsoft.quantum.canon) (e.g. [`H`](xref:microsoft.quantum.intrinsic.h) and [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach)) are automatically available to operations defined within cells in Q# Jupyter Notebooks.</span></span>
> <span data-ttu-id="5c410-273">No entanto, isso não é verdadeiro para o código trazido de Q# arquivos de origem externos (um processo mostrado em [introdução a Q# e Jupyter notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span><span class="sxs-lookup"><span data-stu-id="5c410-273">However, this is not true for code brought in from external Q# source files (a process shown at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="5c410-274">Da mesma forma, a definição de operações requer apenas a gravação do Q# código e a execução da célula.</span><span class="sxs-lookup"><span data-stu-id="5c410-274">Similarly, defining operations requires only writing the Q# code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="600">

<span data-ttu-id="5c410-275">Em seguida, a saída lista essas operações, que podem ser chamadas a partir de células futuras.</span><span class="sxs-lookup"><span data-stu-id="5c410-275">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="5c410-276">Computadores de destino</span><span class="sxs-lookup"><span data-stu-id="5c410-276">Target machines</span></span>

<span data-ttu-id="5c410-277">A funcionalidade para executar operações em computadores de destino específicos é fornecida por meio de [ Q# comandos mágicos](xref:microsoft.quantum.guide.quickref.iqsharp).</span><span class="sxs-lookup"><span data-stu-id="5c410-277">The functionality to run operations on specific target machines is provided via [IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="5c410-278">Por exemplo, utiliza `%simulate` o `QuantumSimulator` e `%estimate` usa o `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="5c410-278">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Simulate and estimate resources Jupyter cell" width="500">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="5c410-279">Passando entradas para funções e operações</span><span class="sxs-lookup"><span data-stu-id="5c410-279">Passing inputs to functions and operations</span></span>

<span data-ttu-id="5c410-280">Atualmente, os comandos mágicos de execução só podem ser usados com operações que não usam argumentos.</span><span class="sxs-lookup"><span data-stu-id="5c410-280">Currently the execution magic commands can only be used with operations that take no arguments.</span></span> <span data-ttu-id="5c410-281">Portanto, para executar `MeasureSuperpositionArray` , precisamos definir uma operação "wrapper" que chama a operação com os argumentos:</span><span class="sxs-lookup"><span data-stu-id="5c410-281">So, to run `MeasureSuperpositionArray`, we need to define a "wrapper" operation which then calls the operation with the arguments:</span></span>

<img src="../media/hostprograms_jupyter_wrapper_def_sim_crop.png" alt="Wrapper function and simulate Jupyter cell" width="550">

<span data-ttu-id="5c410-282">É claro que essa operação pode ser usada de forma semelhante com `%estimate` e outros comandos de execução.</span><span class="sxs-lookup"><span data-stu-id="5c410-282">This operation can of course be used similarly with `%estimate` and other execution commands.</span></span>
