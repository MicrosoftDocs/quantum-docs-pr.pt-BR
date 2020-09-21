---
title: Quantum Toffoli Simulator-kit de desenvolvimento do Quantum
description: Saiba mais sobre o simulador do Microsoft QDK Toffoli, um simulador de Quantum de finalidade especial que pode ser usado com milhões de qubits.
author: alan-geller
ms.author: ageller
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 82882f01d1b5c036faee71f18a18b2595107ddb7
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835903"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a><span data-ttu-id="9b7ae-103">Simulador do QDK (Kit de desenvolvimento do Quantum) Toffoli</span><span class="sxs-lookup"><span data-stu-id="9b7ae-103">Quantum Development Kit (QDK) Toffoli simulator</span></span>

<span data-ttu-id="9b7ae-104">O simulador QDK Toffoli é um simulador de finalidade especial com escopo limitado e só dá suporte a `X` `CNOT` operações de Quantum com vários controle, e `X` .</span><span class="sxs-lookup"><span data-stu-id="9b7ae-104">The QDK Toffoli simulator is a special-purpose simulator with a limited scope and only supports `X`, `CNOT`, and multi-controlled `X` quantum operations.</span></span> <span data-ttu-id="9b7ae-105">Toda a lógica clássica e os cálculos estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-105">All classical logic and computations are available.</span></span>

<span data-ttu-id="9b7ae-106">Embora o simulador de Toffoli seja mais restrito em funcionalidade do que o [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), ele tem a vantagem de ser capaz de simular muito mais qubits.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-106">While the Toffoli simulator is more restricted in functionality than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it has the advantage of being able to simulate far more qubits.</span></span> <span data-ttu-id="9b7ae-107">O simulador de Toffoli pode ser usado com milhões de qubits, enquanto o simulador de estado completo é limitado a cerca de 30 qubits.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-107">The Toffoli simulator can be used with millions of qubits, while the full state simulator is limited to about 30 qubits.</span></span> <span data-ttu-id="9b7ae-108">Isso é útil, por exemplo, com ORACLES que avaliam funções booleanas – elas podem ser implementadas usando o conjunto limitado de algoritmos com suporte e testadas em um grande número de qubits.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-108">This is useful, for example, with oracles that evaluate Boolean functions - they can be implemented using the limited set of supported algorithms and tested on a large number of qubits.</span></span>

## <a name="invoking-the-toffoli-simulator"></a><span data-ttu-id="9b7ae-109">Invocando o simulador de Toffoli</span><span class="sxs-lookup"><span data-stu-id="9b7ae-109">Invoking the Toffoli simulator</span></span>

<span data-ttu-id="9b7ae-110">Você expõe o simulador Toffoli por meio da `ToffoliSimulator` classe.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-110">You expose the Toffoli simulator via the `ToffoliSimulator` class.</span></span> <span data-ttu-id="9b7ae-111">Para obter detalhes adicionais, consulte [maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="9b7ae-111">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-toffoli-simulator-from-c"></a><span data-ttu-id="9b7ae-112">Invocando o simulador de Toffoli de C #</span><span class="sxs-lookup"><span data-stu-id="9b7ae-112">Invoking the Toffoli simulator from C#</span></span>

<span data-ttu-id="9b7ae-113">Assim como acontece com outros computadores de destino, primeiramente você cria uma instância da classe `ToffoliSimulator` e, em seguida, passa-a como o primeiro parâmetro do método `Run` de uma operação.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-113">As with other target machines, you first create an instance of the `ToffoliSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="9b7ae-114">Observe que, diferentemente da classe `QuantumSimulator`, a classe `ToffoliSimulator` não implementa a interface <xref:System.IDisposable> e, portanto, você não precisa colocá-la em uma instrução `using`.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-114">Note that, unlike the `QuantumSimulator` class, the `ToffoliSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a><span data-ttu-id="9b7ae-115">Invocando o simulador de Toffoli do Python</span><span class="sxs-lookup"><span data-stu-id="9b7ae-115">Invoking the Toffoli simulator from Python</span></span>

<span data-ttu-id="9b7ae-116">Use o método [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) da biblioteca do Python com a operação importada Q# :</span><span class="sxs-lookup"><span data-stu-id="9b7ae-116">Use the [toffoli_simulate()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a><span data-ttu-id="9b7ae-117">Invocando o simulador Toffoli da linha de comando</span><span class="sxs-lookup"><span data-stu-id="9b7ae-117">Invoking the Toffoli simulator from the command line</span></span>

<span data-ttu-id="9b7ae-118">Ao executar um Q# programa a partir da linha de comando, use o parâmetro **--Simulator** (ou **-s** Shortcut) para especificar o computador de destino do simulador de Toffoli.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-118">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the Toffoli simulator target machine.</span></span> <span data-ttu-id="9b7ae-119">O comando a seguir executa um programa usando o estimador de recursos:</span><span class="sxs-lookup"><span data-stu-id="9b7ae-119">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a><span data-ttu-id="9b7ae-120">Invocando o simulador do Toffoli de blocos de anotações do Juptyer</span><span class="sxs-lookup"><span data-stu-id="9b7ae-120">Invoking the Toffoli simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="9b7ae-121">Use o Q# comando mágico I [% Toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) para executar a Q# operação.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-121">Use the IQ# magic command [%toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) to run the Q# operation.</span></span>

```
%toffoli myOperation
```

## <a name="supported-operations"></a><span data-ttu-id="9b7ae-122">Operações com suporte</span><span class="sxs-lookup"><span data-stu-id="9b7ae-122">Supported operations</span></span>

<span data-ttu-id="9b7ae-123">O simulador do Toffoli dá suporte a:</span><span class="sxs-lookup"><span data-stu-id="9b7ae-123">The Toffoli simulator supports:</span></span>

* <span data-ttu-id="9b7ae-124">Rotações e exponenciação Paulis, como `R` e `Exp` , quando a operação resultante é igual a `X` ou a matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-124">Rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation equals `X` or the identity matrix.</span></span>
* <span data-ttu-id="9b7ae-125">Operações de medição e [declaração](xref:microsoft.quantum.diagnostics.assertmeasurement) , mas apenas na `Z` base Pauli.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-125">Measurement and [assert](xref:microsoft.quantum.diagnostics.assertmeasurement) operations, but only in the Pauli `Z` basis.</span></span> <span data-ttu-id="9b7ae-126">Observe que a probabilidade de uma operação de medida é sempre **0** ou **1**; Não há aleatoriedade no simulador de Toffoli.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-126">Note that a measurement operation's probability is always either **0** or **1**; there is no randomness in the Toffoli simulator.</span></span>
* <span data-ttu-id="9b7ae-127">`DumpMachine` e `DumpRegister` funções.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-127">`DumpMachine` and `DumpRegister` functions.</span></span>
<span data-ttu-id="9b7ae-128">Ambas as funções produzem o `Z` estado de base atual de cada qubit, uma qubit por linha.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-128">Both functions output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="specifying-the-number-of-qubits"></a><span data-ttu-id="9b7ae-129">Especificando o número de qubits</span><span class="sxs-lookup"><span data-stu-id="9b7ae-129">Specifying the number of qubits</span></span>

<span data-ttu-id="9b7ae-130">Por padrão, uma `ToffoliSimulator` instância aloca espaço para 65.536 qubits.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-130">By default, a `ToffoliSimulator` instance allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="9b7ae-131">Se o algoritmo exigir mais qubits do que isso, você poderá especificar a contagem de qubit fornecendo um valor para o `qubitCount` parâmetro para o construtor.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-131">If your algorithm requires more qubits than this, you can specify the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="9b7ae-132">Cada qubit adicional requer apenas um byte de memória, portanto, não há nenhum custo significativo para a estimativa do número de qubits que você precisará.</span><span class="sxs-lookup"><span data-stu-id="9b7ae-132">Each additional qubit requires only one byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="9b7ae-133">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9b7ae-133">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a><span data-ttu-id="9b7ae-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b7ae-134">See also</span></span>

- [<span data-ttu-id="9b7ae-135">Estimador de recursos Quantum</span><span class="sxs-lookup"><span data-stu-id="9b7ae-135">Quantum Resources Estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="9b7ae-136">Simulador de rastreamento Quantum</span><span class="sxs-lookup"><span data-stu-id="9b7ae-136">Quantum Trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="9b7ae-137">Simulador de estado completo Quantum</span><span class="sxs-lookup"><span data-stu-id="9b7ae-137">Quantum Full State simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 