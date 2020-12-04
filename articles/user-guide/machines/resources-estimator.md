---
title: Estimador de recursos do Quantum – kit de desenvolvimento do Quantum
description: Saiba mais sobre o estimador de recursos do Microsoft QDK, que estima os recursos necessários para executar uma determinada instância de uma Q# operação em um computador Quantum.
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: de425c2d91c6528b13c3bedd81acb4b4273ed711
ms.sourcegitcommit: 7c687495a79d75ae9e029e5a41baec84d9e07bb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2020
ms.locfileid: "96604636"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="6987f-103">Estimador de recursos do kit de desenvolvimento Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="6987f-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="6987f-104">Como o nome indica, a `ResourcesEstimator` classe estima os recursos necessários para executar uma determinada instância de uma Q# operação em um computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="6987f-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="6987f-105">Ele realiza isso executando a operação Quantum sem realmente simular o estado de um computador Quantum; por esse motivo, ele estima recursos para Q# operações que usam milhares de qubits, desde que a parte clássica do código seja executada em um tempo razoável.</span><span class="sxs-lookup"><span data-stu-id="6987f-105">It accomplishes this by running the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="6987f-106">O estimador de recursos é criado sobre o [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro), que fornece um conjunto mais rico de métricas e ferramentas para ajudar a depurar Q# programas.</span><span class="sxs-lookup"><span data-stu-id="6987f-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="6987f-107">Invocando e executando o estimador de recursos</span><span class="sxs-lookup"><span data-stu-id="6987f-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="6987f-108">Você pode usar o estimador de recursos para executar qualquer Q# operação.</span><span class="sxs-lookup"><span data-stu-id="6987f-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="6987f-109">Para obter detalhes adicionais, consulte [maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="6987f-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="6987f-110">Invocando o estimador de recursos de C #</span><span class="sxs-lookup"><span data-stu-id="6987f-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="6987f-111">Assim como acontece com outros computadores de destino, primeiramente você cria uma instância da classe `ResourcesEstimator` e, em seguida, passa-a como o primeiro parâmetro do método `Run` de uma operação.</span><span class="sxs-lookup"><span data-stu-id="6987f-111">As with other target machines, you first create an instance of the `ResourcesEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="6987f-112">Observe que, diferentemente da classe `QuantumSimulator`, a classe `ResourcesEstimator` não implementa a interface <xref:System.IDisposable> e, portanto, você não precisa colocá-la em uma instrução `using`.</span><span class="sxs-lookup"><span data-stu-id="6987f-112">Note that, unlike the `QuantumSimulator` class, the `ResourcesEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();
            Console.WriteLine(estimator.ToTSV());
        }
    }
}
```

<span data-ttu-id="6987f-113">Como mostra o exemplo, o `ResourcesEstimator` fornece o `ToTSV()` método, que gera uma tabela com valores separados por tabulações (TSV).</span><span class="sxs-lookup"><span data-stu-id="6987f-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="6987f-114">Você pode salvar a tabela em um arquivo ou exibi-la no console para análise.</span><span class="sxs-lookup"><span data-stu-id="6987f-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="6987f-115">Veja a seguir um exemplo de saída do programa anterior:</span><span class="sxs-lookup"><span data-stu-id="6987f-115">The following is a sample output from the preceding program:</span></span>

```output
Metric          Sum
CNOT            1000
QubitClifford   1000
R               0
Measure         4002
T               0
Depth           0
Width           2
BorrowedWidth   0
```

> [!NOTE]
> <span data-ttu-id="6987f-116">Uma `ResourcesEstimator` instância do não redefine seus cálculos em todas as execuções.</span><span class="sxs-lookup"><span data-stu-id="6987f-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="6987f-117">Se você usar a mesma instância para executar outra operação, ela agregará os novos resultados com os resultados existentes.</span><span class="sxs-lookup"><span data-stu-id="6987f-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="6987f-118">Se você precisar redefinir cálculos entre execuções, crie uma nova instância para cada execução.</span><span class="sxs-lookup"><span data-stu-id="6987f-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="6987f-119">Invocando o estimador de recursos do Python</span><span class="sxs-lookup"><span data-stu-id="6987f-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="6987f-120">Use o método [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) da biblioteca do Python com a operação importada Q# :</span><span class="sxs-lookup"><span data-stu-id="6987f-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="6987f-121">Invocando o estimador de recursos da linha de comando</span><span class="sxs-lookup"><span data-stu-id="6987f-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="6987f-122">Ao executar um Q# programa a partir da linha de comando, use o parâmetro **--Simulator** (ou **-s** Shortcut) para especificar o `ResourcesEstimator` computador de destino.</span><span class="sxs-lookup"><span data-stu-id="6987f-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="6987f-123">O comando a seguir executa um programa usando o estimador de recursos:</span><span class="sxs-lookup"><span data-stu-id="6987f-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="6987f-124">Invocando o estimador de recursos de notebooks Juptyer</span><span class="sxs-lookup"><span data-stu-id="6987f-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="6987f-125">Use a Q# [estimativa de%](xref:microsoft.quantum.iqsharp.magic-ref.simulate) de comando mágico mágica para executar a Q# operação.</span><span class="sxs-lookup"><span data-stu-id="6987f-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="6987f-126">Recuperando programaticamente os dados estimados</span><span class="sxs-lookup"><span data-stu-id="6987f-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="6987f-127">Além de uma tabela TSV, você pode recuperar programaticamente os recursos estimados durante a execução por meio da `Data` Propriedade do estimador de recursos.</span><span class="sxs-lookup"><span data-stu-id="6987f-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="6987f-128">A `Data` propriedade fornece uma `System.DataTable` instância com duas colunas: `Metric` e `Sum` , indexada pelos nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="6987f-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="6987f-129">O código a seguir mostra como recuperar e imprimir o número total de `QubitClifford` `T` e `CNOT` as operações usadas por uma Q# operação:</span><span class="sxs-lookup"><span data-stu-id="6987f-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();

            var data = estimator.Data;
            Console.WriteLine($"QubitCliffords: {data.Rows.Find("QubitClifford")["Sum"]}");
            Console.WriteLine($"Ts: {data.Rows.Find("T")["Sum"]}");
            Console.WriteLine($"CNOTs: {data.Rows.Find("CNOT")["Sum"]}");
        }
    }
}
```

## <a name="metrics-reported"></a><span data-ttu-id="6987f-130">Métricas relatadas</span><span class="sxs-lookup"><span data-stu-id="6987f-130">Metrics Reported</span></span>

<span data-ttu-id="6987f-131">O estimador de recursos acompanha as seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="6987f-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="6987f-132">Métrica</span><span class="sxs-lookup"><span data-stu-id="6987f-132">Metric</span></span>|<span data-ttu-id="6987f-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="6987f-133">Description</span></span>|
|----|----|
|<span data-ttu-id="6987f-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="6987f-134">__CNOT__</span></span>    |<span data-ttu-id="6987f-135">A contagem de operações de execução `CNOT` (também conhecida como operações Pauli X controladas).</span><span class="sxs-lookup"><span data-stu-id="6987f-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="6987f-136">__QubitClifford__</span><span class="sxs-lookup"><span data-stu-id="6987f-136">__QubitClifford__</span></span> |<span data-ttu-id="6987f-137">A contagem de execuções de uma única qubit Clifford e operações de Pauli.</span><span class="sxs-lookup"><span data-stu-id="6987f-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="6987f-138">__Medida__</span><span class="sxs-lookup"><span data-stu-id="6987f-138">__Measure__</span></span>    |<span data-ttu-id="6987f-139">A contagem de execuções de qualquer medida.</span><span class="sxs-lookup"><span data-stu-id="6987f-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="6987f-140">__R__</span><span class="sxs-lookup"><span data-stu-id="6987f-140">__R__</span></span>    |<span data-ttu-id="6987f-141">A contagem de execuções de qualquer rotação de qubit única, excluindo `T` , Clifford e Pauli operações.</span><span class="sxs-lookup"><span data-stu-id="6987f-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="6987f-142">__T__</span><span class="sxs-lookup"><span data-stu-id="6987f-142">__T__</span></span>    |<span data-ttu-id="6987f-143">A contagem de execuções de `T` operações e seus conjugados, incluindo as `T` operações, T_x = h. T. H e T_y = hipótese. T. hipótese.</span><span class="sxs-lookup"><span data-stu-id="6987f-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="6987f-144">__Profundidade__</span><span class="sxs-lookup"><span data-stu-id="6987f-144">__Depth__</span></span>|<span data-ttu-id="6987f-145">Profundidade do circuito Quantum executado pela Q# operação (veja [abaixo](#depth-width-and-qubitcount)).</span><span class="sxs-lookup"><span data-stu-id="6987f-145">Depth of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="6987f-146">Por padrão, a métrica de profundidade conta apenas `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="6987f-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="6987f-147">Para obter mais detalhes, consulte o [contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span><span class="sxs-lookup"><span data-stu-id="6987f-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="6987f-148">__Largura__</span><span class="sxs-lookup"><span data-stu-id="6987f-148">__Width__</span></span>|<span data-ttu-id="6987f-149">Largura do circuito Quantum executada pela Q# operação (veja [abaixo](#depth-width-and-qubitcount)).</span><span class="sxs-lookup"><span data-stu-id="6987f-149">Width of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="6987f-150">Por padrão, a métrica de profundidade conta apenas `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="6987f-150">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="6987f-151">Para obter mais detalhes, consulte [contador de largura](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span><span class="sxs-lookup"><span data-stu-id="6987f-151">For more details, see [Width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span></span>   |
|<span data-ttu-id="6987f-152">__QubitCount__</span><span class="sxs-lookup"><span data-stu-id="6987f-152">__QubitCount__</span></span>    |<span data-ttu-id="6987f-153">O limite inferior para o número máximo de qubits alocadas durante a execução da Q# operação.</span><span class="sxs-lookup"><span data-stu-id="6987f-153">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="6987f-154">Essa métrica pode não ser compatível com __profundidade__ (veja abaixo).</span><span class="sxs-lookup"><span data-stu-id="6987f-154">This metric might not be compatible with __Depth__ (see below).</span></span>  |
|<span data-ttu-id="6987f-155">__BorrowedWidth__</span><span class="sxs-lookup"><span data-stu-id="6987f-155">__BorrowedWidth__</span></span>    |<span data-ttu-id="6987f-156">O número máximo de qubits emprestados dentro da Q# operação.</span><span class="sxs-lookup"><span data-stu-id="6987f-156">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |


## <a name="depth-width-and-qubitcount"></a><span data-ttu-id="6987f-157">Profundidade, largura e QubitCount</span><span class="sxs-lookup"><span data-stu-id="6987f-157">Depth, Width, and QubitCount</span></span>

<span data-ttu-id="6987f-158">As estimativas de profundidade e largura relatadas são compatíveis entre si.</span><span class="sxs-lookup"><span data-stu-id="6987f-158">Reported Depth and Width estimates are compatible with each other.</span></span>
<span data-ttu-id="6987f-159">(Anteriormente, os dois números eram atingíveis, mas circuitos diferentes seriam necessários para profundidade e largura.) Atualmente, ambas as métricas nesse par podem ser obtidas pelo mesmo circuito ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6987f-159">(Previously both numbers were achievable, but different circuits would be required for Depth and for Width.) Currently both metrics in this pair can be achieved by the same circuit at the same time.</span></span>

<span data-ttu-id="6987f-160">As seguintes métricas são relatadas:</span><span class="sxs-lookup"><span data-stu-id="6987f-160">The following metrics are reported:</span></span>

<span data-ttu-id="6987f-161">__Profundidade:__ Para a operação raiz, o tempo necessário para executá-lo assumindo tempos de portão específicos.</span><span class="sxs-lookup"><span data-stu-id="6987f-161">__Depth:__ For the root operation - time it takes to execute it assuming specific gate times.</span></span>
<span data-ttu-id="6987f-162">Para operações chamadas ou a diferença de tempo de operações subsequentes entre o tempo de disponibilidade qubit mais recente no início e no fim da operação.</span><span class="sxs-lookup"><span data-stu-id="6987f-162">For operations called or subsequent operations - time difference between latest qubit availability time at the beginning and the end of the operation.</span></span>

<span data-ttu-id="6987f-163">__Largura:__ Para a operação raiz-número de qubits realmente usados para executá-lo (e operação que ele chama).</span><span class="sxs-lookup"><span data-stu-id="6987f-163">__Width:__ For the root operation - number of qubits actually used to execute it (and operation it calls).</span></span>
<span data-ttu-id="6987f-164">Para operações chamadas ou operações subsequentes, quantos mais qubits foram usados, além do qubits já usado no início da operação.</span><span class="sxs-lookup"><span data-stu-id="6987f-164">For operations called or subsequent operations - how many more qubits were used in addition to the qubits already used at the beginning of the operation.</span></span>

<span data-ttu-id="6987f-165">Observe que os qubits reutilizados não contribuem para esse número.</span><span class="sxs-lookup"><span data-stu-id="6987f-165">Please note, that reused qubits do not contribute to this number.</span></span>
<span data-ttu-id="6987f-166">Ou seja, se alguns qubits tiverem sido liberados antes da operação A ser iniciada, e todas as qubit exigidas por essa operação A (e as operações chamadas de A) fossem satisfeitas com a reutilização da versão anterior qubits, a largura da operação A é relatada como 0.</span><span class="sxs-lookup"><span data-stu-id="6987f-166">I.e. if a few qubits have been released before operation A starts, and all qubit demanded by this operation A (and operations called from A) were satisfied by reusing previously release qubits, the Width of operation A is reported as 0.</span></span> <span data-ttu-id="6987f-167">Os qubits emprestados com êxito não contribuem com a largura.</span><span class="sxs-lookup"><span data-stu-id="6987f-167">Successfully borrowed qubits do not contribute to the Width either.</span></span>

<span data-ttu-id="6987f-168">__QubitCount:__ Para a operação raiz-número mínimo de qubits que seriam suficientes para executar esta operação (e as operações chamadas a partir dela).</span><span class="sxs-lookup"><span data-stu-id="6987f-168">__QubitCount:__ For the root operation - minimum number of qubits that would be sufficient to execute this operation (and operations called from it).</span></span>
<span data-ttu-id="6987f-169">Para operações chamadas ou operações subsequentes-número mínimo de qubits que seriam suficientes para executar essa operação separadamente.</span><span class="sxs-lookup"><span data-stu-id="6987f-169">For operations called or subsequent operations - minimum number of qubits that would be sufficient to execute this operation separately.</span></span> <span data-ttu-id="6987f-170">Esse número não inclui qubits de entrada.</span><span class="sxs-lookup"><span data-stu-id="6987f-170">This number doesn't include input qubits.</span></span> <span data-ttu-id="6987f-171">Ele inclui qubits emprestado.</span><span class="sxs-lookup"><span data-stu-id="6987f-171">It does include borrowed qubits.</span></span>

<span data-ttu-id="6987f-172">Há suporte para dois modos de operação.</span><span class="sxs-lookup"><span data-stu-id="6987f-172">Two modes of operation are supported.</span></span> <span data-ttu-id="6987f-173">É selecionado por meio da configuração de QCTraceSimulatorConfiguration. OptimizeDepth.</span><span class="sxs-lookup"><span data-stu-id="6987f-173">Mode is selected by setting QCTraceSimulatorConfiguration.OptimizeDepth.</span></span>

<span data-ttu-id="6987f-174">__OptimizeDepth = true:__ QubitManager é desencorajado de qubit reutilização e aloca novas qubit toda vez que for solicitado por um qubit.</span><span class="sxs-lookup"><span data-stu-id="6987f-174">__OptimizeDepth=true:__ QubitManager is discouraged from qubit reuse and allocates new qubit every time it is asked for a qubit.</span></span> <span data-ttu-id="6987f-175">Para a __profundidade__ da operação raiz se torna a profundidade mínima (limite inferior).</span><span class="sxs-lookup"><span data-stu-id="6987f-175">For the root operation __Depth__ becomes the minimum depth (lower bound).</span></span> <span data-ttu-id="6987f-176">A __largura__ compatível é relatada para essa profundidade (ambas podem ser obtidas ao mesmo tempo).</span><span class="sxs-lookup"><span data-stu-id="6987f-176">Compatible __Width__ is reported for this depth (both can be achieved at the same time).</span></span> <span data-ttu-id="6987f-177">Observe que essa largura provavelmente não será ideal, considerando essa profundidade.</span><span class="sxs-lookup"><span data-stu-id="6987f-177">Note, that this width will likely be not optimal given this depth.</span></span> <span data-ttu-id="6987f-178">__QubitCount__ pode ser menor que a largura da operação raiz porque ela assume reutilização.</span><span class="sxs-lookup"><span data-stu-id="6987f-178">__QubitCount__ may be lower than Width for the root operation because it assumes reuse.</span></span>

<span data-ttu-id="6987f-179">__OptimizeDepth = false:__ QubitManager é incentivado a reutilizar o qubits e reutilizará o qubits liberado antes de alocar novos.</span><span class="sxs-lookup"><span data-stu-id="6987f-179">__OptimizeDepth=false:__ QubitManager is encouraged to reuse qubits and will reuse released qubits before allocating new ones.</span></span> <span data-ttu-id="6987f-180">Para a __largura__ da operação raiz se torna a largura mínima (limite inferior).</span><span class="sxs-lookup"><span data-stu-id="6987f-180">For the root operation __Width__ becomes the minimal width (lower bound).</span></span> <span data-ttu-id="6987f-181">A __profundidade__ compatível é relatada na qual ela pode ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6987f-181">Compatible __Depth__ is reported on which it can be achieved.</span></span> <span data-ttu-id="6987f-182">__QubitCount__ será igual à __largura__ da operação raiz, supondo que não haja empréstimo.</span><span class="sxs-lookup"><span data-stu-id="6987f-182">__QubitCount__ will be the same as __Width__ for the root operation assuming no borrowing.</span></span>

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="6987f-183">Como fornecer a probabilidade de resultados de medida</span><span class="sxs-lookup"><span data-stu-id="6987f-183">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="6987f-184">Você pode usar <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> do <xref:Microsoft.Quantum.Diagnostics> namespace para fornecer informações sobre a probabilidade esperada de uma operação de medição.</span><span class="sxs-lookup"><span data-stu-id="6987f-184">You can use <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> from the <xref:Microsoft.Quantum.Diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="6987f-185">Para obter mais informações, consulte o [simulador de rastreamento do Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span><span class="sxs-lookup"><span data-stu-id="6987f-185">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="6987f-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="6987f-186">See also</span></span>

- [<span data-ttu-id="6987f-187">Simulador de rastreamento Quantum</span><span class="sxs-lookup"><span data-stu-id="6987f-187">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="6987f-188">Simulador quântico do Toffoli</span><span class="sxs-lookup"><span data-stu-id="6987f-188">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="6987f-189">Simulador de estado completo quântico</span><span class="sxs-lookup"><span data-stu-id="6987f-189">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 
