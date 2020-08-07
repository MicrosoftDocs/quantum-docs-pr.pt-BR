---
title: Estimador de recursos do Quantum – kit de desenvolvimento do Quantum
description: Saiba mais sobre o estimador de recursos do Microsoft QDK, que estima os recursos necessários para executar uma determinada instância de uma Q# operação em um computador Quantum.
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: d5338eb740716d9d7f408703347f572688bbccb2
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868178"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="c562b-103">Estimador de recursos do kit de desenvolvimento Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="c562b-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="c562b-104">Como o nome indica, a `ResourcesEstimator` classe estima os recursos necessários para executar uma determinada instância de uma Q# operação em um computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="c562b-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="c562b-105">Ele realiza isso executando a operação Quantum sem realmente simular o estado de um computador Quantum; por esse motivo, ele estima recursos para Q# operações que usam milhares de qubits, desde que a parte clássica do código seja executada em um tempo razoável.</span><span class="sxs-lookup"><span data-stu-id="c562b-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="c562b-106">O estimador de recursos é criado sobre o [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro), que fornece um conjunto mais rico de métricas e ferramentas para ajudar a depurar Q# programas.</span><span class="sxs-lookup"><span data-stu-id="c562b-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="c562b-107">Invocando e executando o estimador de recursos</span><span class="sxs-lookup"><span data-stu-id="c562b-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="c562b-108">Você pode usar o estimador de recursos para executar qualquer Q# operação.</span><span class="sxs-lookup"><span data-stu-id="c562b-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="c562b-109">Para obter detalhes adicionais, consulte [maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="c562b-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="c562b-110">Invocando o estimador de recursos de C #</span><span class="sxs-lookup"><span data-stu-id="c562b-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="c562b-111">Assim como acontece com outros computadores de destino, primeiramente você cria uma instância da classe `ResourceEstimator` e, em seguida, passa-a como o primeiro parâmetro do método `Run` de uma operação.</span><span class="sxs-lookup"><span data-stu-id="c562b-111">As with other target machines, you first create an instance of the `ResourceEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="c562b-112">Observe que, diferentemente da classe `QuantumSimulator`, a classe `ResourceEstimator` não implementa a interface <xref:System.IDisposable> e, portanto, você não precisa colocá-la em uma instrução `using`.</span><span class="sxs-lookup"><span data-stu-id="c562b-112">Note that, unlike the `QuantumSimulator` class, the `ResourceEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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

<span data-ttu-id="c562b-113">Como mostra o exemplo, o `ResourcesEstimator` fornece o `ToTSV()` método, que gera uma tabela com valores separados por tabulações (TSV).</span><span class="sxs-lookup"><span data-stu-id="c562b-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="c562b-114">Você pode salvar a tabela em um arquivo ou exibi-la no console para análise.</span><span class="sxs-lookup"><span data-stu-id="c562b-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="c562b-115">Veja a seguir um exemplo de saída do programa anterior:</span><span class="sxs-lookup"><span data-stu-id="c562b-115">The following is a sample output from the preceding program:</span></span>

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
> <span data-ttu-id="c562b-116">Uma `ResourcesEstimator` instância do não redefine seus cálculos em todas as execuções.</span><span class="sxs-lookup"><span data-stu-id="c562b-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="c562b-117">Se você usar a mesma instância para executar outra operação, ela agregará os novos resultados com os resultados existentes.</span><span class="sxs-lookup"><span data-stu-id="c562b-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="c562b-118">Se você precisar redefinir cálculos entre execuções, crie uma nova instância para cada execução.</span><span class="sxs-lookup"><span data-stu-id="c562b-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="c562b-119">Invocando o estimador de recursos do Python</span><span class="sxs-lookup"><span data-stu-id="c562b-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="c562b-120">Use o método [estimate_resources ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) da biblioteca do Python com a operação importada Q# :</span><span class="sxs-lookup"><span data-stu-id="c562b-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="c562b-121">Invocando o estimador de recursos da linha de comando</span><span class="sxs-lookup"><span data-stu-id="c562b-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="c562b-122">Ao executar um Q# programa a partir da linha de comando, use o parâmetro **--Simulator** (ou **-s** Shortcut) para especificar o `ResourcesEstimator` computador de destino.</span><span class="sxs-lookup"><span data-stu-id="c562b-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="c562b-123">O comando a seguir executa um programa usando o estimador de recursos:</span><span class="sxs-lookup"><span data-stu-id="c562b-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="c562b-124">Invocando o estimador de recursos de notebooks Juptyer</span><span class="sxs-lookup"><span data-stu-id="c562b-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="c562b-125">Use a Q# [estimativa de%](xref:microsoft.quantum.iqsharp.magic-ref.simulate) de comando mágico mágica para executar a Q# operação.</span><span class="sxs-lookup"><span data-stu-id="c562b-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="c562b-126">Recuperando programaticamente os dados estimados</span><span class="sxs-lookup"><span data-stu-id="c562b-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="c562b-127">Além de uma tabela TSV, você pode recuperar programaticamente os recursos estimados durante a execução por meio da `Data` Propriedade do estimador de recursos.</span><span class="sxs-lookup"><span data-stu-id="c562b-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="c562b-128">A `Data` propriedade fornece uma `System.DataTable` instância com duas colunas: `Metric` e `Sum` , indexada pelos nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="c562b-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="c562b-129">O código a seguir mostra como recuperar e imprimir o número total de `QubitClifford` `T` e `CNOT` as operações usadas por uma Q# operação:</span><span class="sxs-lookup"><span data-stu-id="c562b-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="c562b-130">Métricas relatadas</span><span class="sxs-lookup"><span data-stu-id="c562b-130">Metrics Reported</span></span>

<span data-ttu-id="c562b-131">O estimador de recursos acompanha as seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="c562b-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="c562b-132">Métrica</span><span class="sxs-lookup"><span data-stu-id="c562b-132">Metric</span></span>|<span data-ttu-id="c562b-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="c562b-133">Description</span></span>|
|----|----|
|<span data-ttu-id="c562b-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="c562b-134">__CNOT__</span></span>    |<span data-ttu-id="c562b-135">A contagem de operações de execução `CNOT` (também conhecida como operações Pauli X controladas).</span><span class="sxs-lookup"><span data-stu-id="c562b-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="c562b-136">__QubitClifford__</span><span class="sxs-lookup"><span data-stu-id="c562b-136">__QubitClifford__</span></span> |<span data-ttu-id="c562b-137">A contagem de execuções de uma única qubit Clifford e operações de Pauli.</span><span class="sxs-lookup"><span data-stu-id="c562b-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="c562b-138">__Medida__</span><span class="sxs-lookup"><span data-stu-id="c562b-138">__Measure__</span></span>    |<span data-ttu-id="c562b-139">A contagem de execuções de qualquer medida.</span><span class="sxs-lookup"><span data-stu-id="c562b-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="c562b-140">__R__</span><span class="sxs-lookup"><span data-stu-id="c562b-140">__R__</span></span>    |<span data-ttu-id="c562b-141">A contagem de execuções de qualquer rotação de qubit única, excluindo `T` , Clifford e Pauli operações.</span><span class="sxs-lookup"><span data-stu-id="c562b-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="c562b-142">__T__</span><span class="sxs-lookup"><span data-stu-id="c562b-142">__T__</span></span>    |<span data-ttu-id="c562b-143">A contagem de execuções de `T` operações e seus conjugados, incluindo as `T` operações, T_x = h. T. H e T_y = hipótese. T. hipótese.</span><span class="sxs-lookup"><span data-stu-id="c562b-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="c562b-144">__Depth__</span><span class="sxs-lookup"><span data-stu-id="c562b-144">__Depth__</span></span>|<span data-ttu-id="c562b-145">O limite inferior para a profundidade do circuito Quantum executado pela Q# operação.</span><span class="sxs-lookup"><span data-stu-id="c562b-145">The lower bound for the depth of the quantum circuit run by the Q# operation.</span></span> <span data-ttu-id="c562b-146">Por padrão, a métrica de profundidade conta apenas `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="c562b-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="c562b-147">Para obter mais detalhes, consulte o [contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span><span class="sxs-lookup"><span data-stu-id="c562b-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="c562b-148">__Largura__</span><span class="sxs-lookup"><span data-stu-id="c562b-148">__Width__</span></span>    |<span data-ttu-id="c562b-149">O limite inferior para o número máximo de qubits alocadas durante a execução da Q# operação.</span><span class="sxs-lookup"><span data-stu-id="c562b-149">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="c562b-150">Talvez não seja possível obter os limites mais baixos de __profundidade__ e __largura__ simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="c562b-150">It might not be possible to achieve both __Depth__ and __Width__ lower bounds simultaneously.</span></span>  |
|<span data-ttu-id="c562b-151">__BorrowedWidth__</span><span class="sxs-lookup"><span data-stu-id="c562b-151">__BorrowedWidth__</span></span>    |<span data-ttu-id="c562b-152">O número máximo de qubits emprestados dentro da Q# operação.</span><span class="sxs-lookup"><span data-stu-id="c562b-152">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="c562b-153">Como fornecer a probabilidade de resultados de medida</span><span class="sxs-lookup"><span data-stu-id="c562b-153">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="c562b-154">Você pode usar <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> do <xref:microsoft.quantum.diagnostics> namespace para fornecer informações sobre a probabilidade esperada de uma operação de medição.</span><span class="sxs-lookup"><span data-stu-id="c562b-154">You can use <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> from the <xref:microsoft.quantum.diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="c562b-155">Para obter mais informações, consulte o [simulador de rastreamento do Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span><span class="sxs-lookup"><span data-stu-id="c562b-155">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="c562b-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="c562b-156">See also</span></span>

- [<span data-ttu-id="c562b-157">Simulador de rastreamento Quantum</span><span class="sxs-lookup"><span data-stu-id="c562b-157">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="c562b-158">Simulador quântico do Toffoli</span><span class="sxs-lookup"><span data-stu-id="c562b-158">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="c562b-159">Simulador de estado completo quântico</span><span class="sxs-lookup"><span data-stu-id="c562b-159">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 