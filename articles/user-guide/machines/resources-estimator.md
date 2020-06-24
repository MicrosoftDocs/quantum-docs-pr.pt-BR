---
title: Estimador de recursos do kit de desenvolvimento Quantum
description: 'Saiba mais sobre o estimador de recursos, que estima os recursos necessários para executar uma determinada instância de uma operação Q # em um computador Quantum.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: b0c800c3946d2e4ba4457127fb9495dc9dcf2934
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274256"
---
# <a name="the-resources-estimator-target-machine"></a><span data-ttu-id="697a4-103">O computador de destino do avaliador de recursos</span><span class="sxs-lookup"><span data-stu-id="697a4-103">The Resources Estimator Target Machine</span></span>

<span data-ttu-id="697a4-104">Como o nome indica, o `ResourcesEstimator` estima os recursos necessários para executar uma determinada instância de uma operação Q # em um computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="697a4-104">As the name implies, the `ResourcesEstimator` estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>
<span data-ttu-id="697a4-105">Ele realiza isso executando a operação Quantum sem realmente simular o estado de um computador Quantum; por esse motivo, ele pode estimar recursos para operações Q # que usam milhares de qubits, se a parte clássica do código puder ser executada em um tempo razoável.</span><span class="sxs-lookup"><span data-stu-id="697a4-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it can estimate resources for Q# operations that use thousands of qubits, if the classical part of the code can be run in a reasonable time.</span></span>

## <a name="usage"></a><span data-ttu-id="697a4-106">Uso</span><span class="sxs-lookup"><span data-stu-id="697a4-106">Usage</span></span>

<span data-ttu-id="697a4-107">O `ResourcesEstimator` é apenas outro tipo de computador de destino, portanto, ele pode ser usado para executar qualquer operação Q #.</span><span class="sxs-lookup"><span data-stu-id="697a4-107">The `ResourcesEstimator` is just another type of target machine, thus it can be used to run any Q# operation.</span></span> 

<span data-ttu-id="697a4-108">Como outros computadores de destino, para usá-lo em um programa de host C#, crie uma instância e passe-a como o primeiro parâmetro do método da operação `Run` :</span><span class="sxs-lookup"><span data-stu-id="697a4-108">As other target machines, to use it on a C# host program create an instance and pass it as the first parameter of the operation's `Run` method:</span></span>

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

<span data-ttu-id="697a4-109">Como mostra o exemplo, o `ResourcesEstimator` fornece um `ToTSV()` método para gerar uma tabela com TSV (valores separados por tabulação) que podem ser salvos em um arquivo ou gravados no console para análise.</span><span class="sxs-lookup"><span data-stu-id="697a4-109">As the example shows, the `ResourcesEstimator` provides a `ToTSV()` method to generate a table with tab-separated-values (TSV) that can be saved into a file or written to the console for analysis.</span></span> <span data-ttu-id="697a4-110">A saída do programa acima deve ser semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="697a4-110">The output of the above program should look something like this:</span></span>

```Output
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
> <span data-ttu-id="697a4-111">O `ResourcesEstimator` não redefine seus cálculos em cada execução, se a mesma instância for usada para executar outra operação, ele continuará agregando contagens sobre os resultados existentes.</span><span class="sxs-lookup"><span data-stu-id="697a4-111">The `ResourcesEstimator` does not reset its calculations on every run, if the same instance is used to execute another operation it will keep aggregating counts on top of existing results.</span></span>
> <span data-ttu-id="697a4-112">Se você precisar redefinir cálculos entre execuções, crie uma nova instância para cada execução.</span><span class="sxs-lookup"><span data-stu-id="697a4-112">If you need to reset calculations between runs, create a new instance for every execution.</span></span>


## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="697a4-113">Recuperando programaticamente os dados estimados</span><span class="sxs-lookup"><span data-stu-id="697a4-113">Programmatically Retrieving the Estimated Data</span></span>

<span data-ttu-id="697a4-114">Além de uma tabela TSV, os recursos estimados podem ser recuperados programaticamente por meio da `ResourcesEstimator` `Data` Propriedade do.</span><span class="sxs-lookup"><span data-stu-id="697a4-114">In addition to a TSV table, the resources estimated can be retrieved programmatically via the `ResourcesEstimator`'s `Data` property.</span></span> <span data-ttu-id="697a4-115">`Data`fornece uma `System.DataTable` instância com duas colunas: `Metric` e `Sum` , indexada pelos nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="697a4-115">`Data` provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics names.</span></span>

<span data-ttu-id="697a4-116">O código a seguir mostra como recuperar e imprimir o número total de `QubitClifford` `T` e `CNOT` Gates usados por uma operação Q #:</span><span class="sxs-lookup"><span data-stu-id="697a4-116">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` gates used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="697a4-117">Métricas relatadas</span><span class="sxs-lookup"><span data-stu-id="697a4-117">Metrics Reported</span></span>

<span data-ttu-id="697a4-118">A seguir está a lista de métricas estimada pelo `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="697a4-118">The following is the list of metrics estimated by the `ResourcesEstimator`:</span></span>

* <span data-ttu-id="697a4-119">__CNOT__: a contagem de CNOT (também conhecida como a porta controlada de Pauli X) de Gates executada.</span><span class="sxs-lookup"><span data-stu-id="697a4-119">__CNOT__: The count of CNOT (also known as the Controlled Pauli X gate) gates executed.</span></span>
* <span data-ttu-id="697a4-120">__QubitClifford__: a contagem de uma única qubit Clifford e Pauli Gates executadas.</span><span class="sxs-lookup"><span data-stu-id="697a4-120">__QubitClifford__: The count of any single qubit Clifford and Pauli gates executed.</span></span>
* <span data-ttu-id="697a4-121">__Medida__: a contagem de qualquer medida executada.</span><span class="sxs-lookup"><span data-stu-id="697a4-121">__Measure__:  The count of any measurements executed.</span></span>
* <span data-ttu-id="697a4-122">__R__: a contagem de qualquer rotação qubit única executada, excluindo T, Clifford e Pauli Gates.</span><span class="sxs-lookup"><span data-stu-id="697a4-122">__R__: The count of any single qubit rotations executed, excluding T, Clifford and Pauli gates.</span></span>
* <span data-ttu-id="697a4-123">__T__: a contagem de t Gates e seus conjugados, incluindo o Gate t, T_x = h. T. H e T_y = hipótese. T. hipótese, executado.</span><span class="sxs-lookup"><span data-stu-id="697a4-123">__T__: The count of T gates and their conjugates, including the T gate, T_x = H.T.H, and T_y = Hy.T.Hy, executed.</span></span>
* <span data-ttu-id="697a4-124">__Profundidade__: profundidade do circuito Quantum executado pela operação Q #.</span><span class="sxs-lookup"><span data-stu-id="697a4-124">__Depth__: Depth of the quantum circuit executed by the Q# operation.</span></span> <span data-ttu-id="697a4-125">Por padrão, somente T Gates são contadas na profundidade, consulte o [contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="697a4-125">By default, only T gates are counted in the depth, see [depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) for details.</span></span>
* <span data-ttu-id="697a4-126">__Largura__: o número máximo de qubits alocadas durante a execução da operação Q #.</span><span class="sxs-lookup"><span data-stu-id="697a4-126">__Width__: Maximum number of qubits allocated during the execution of the Q# operation.</span></span>
* <span data-ttu-id="697a4-127">__BorrowedWidth__: número máximo de qubits emprestados dentro da operação Q #.</span><span class="sxs-lookup"><span data-stu-id="697a4-127">__BorrowedWidth__: Maximum number of qubits borrowed inside the Q# operation.</span></span>


## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="697a4-128">Como fornecer a probabilidade de resultados de medida</span><span class="sxs-lookup"><span data-stu-id="697a4-128">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="697a4-129"><xref:microsoft.quantum.intrinsic.assertprob>do <xref:microsoft.quantum.intrinsic> namespace pode ser usado para fornecer informações sobre a probabilidade esperada de uma medida para ajudar a conduzir a execução do programa Q #.</span><span class="sxs-lookup"><span data-stu-id="697a4-129"><xref:microsoft.quantum.intrinsic.assertprob> from the <xref:microsoft.quantum.intrinsic> namespace can be used to provide information about the expected probability of a measurement to help drive the execution of the Q# program.</span></span> <span data-ttu-id="697a4-130">O exemplo a seguir ilustra isso:</span><span class="sxs-lookup"><span data-stu-id="697a4-130">The following example illustrates this:</span></span>

```qsharp
operation Teleport(source : Qubit, target : Qubit) : Unit {

    using (qubit = Qubit()) {

        H(q);
        CNOT(qubit, target);

        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [qubit], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(qubit) == One) { X(target); X(qubit); }
    }
}
```

<span data-ttu-id="697a4-131">Quando o `ResourcesEstimator` encontrar `AssertProb` , ele registrará essa `PauliZ` medição `source` e `q` deverá receber um resultado de `Zero` com a probabilidade 0,5.</span><span class="sxs-lookup"><span data-stu-id="697a4-131">When the `ResourcesEstimator` encounters `AssertProb` it will record that measuring `PauliZ` on `source` and `q` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="697a4-132">Quando ele for executado `M` posteriormente, ele encontrará os valores gravados das probabilidades de resultado e `M` retornará `Zero` ou `One` com a probabilidade 0,5.</span><span class="sxs-lookup"><span data-stu-id="697a4-132">When it executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span>


## <a name="see-also"></a><span data-ttu-id="697a4-133">Veja também</span><span class="sxs-lookup"><span data-stu-id="697a4-133">See also</span></span>

<span data-ttu-id="697a4-134">O `ResourcesEstimator` é criado com base no [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum, que fornece um conjunto mais rico de métricas, a capacidade de relatar métricas no grafo de Call completo e recursos como o [corretor de entradas distintos](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) para ajudar a encontrar bugs em programas de Q #.</span><span class="sxs-lookup"><span data-stu-id="697a4-134">The `ResourcesEstimator` is built on top of the quantum computer [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics, the ability to report metrics on the full call-graph, and features like [distinct inputs checker](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) to help find bugs on Q# programs.</span></span> <span data-ttu-id="697a4-135">Consulte a documentação do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="697a4-135">Please refer to the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) documentation for more information.</span></span>

