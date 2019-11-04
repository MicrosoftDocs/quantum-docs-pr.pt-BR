---
title: Simulador de estado completo do kit de desenvolvimento do Quantum | Microsoft Docs
description: Visão geral do simulador de estado completo do kit de desenvolvimento do quantum da Microsoft
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: ab0e65765d27e301a59948d7c02105a523022e68
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184671"
---
# <a name="quantum-development-kit-full-state-simulator"></a><span data-ttu-id="0c1f0-103">Simulador de estado completo do kit de desenvolvimento do Quantum</span><span class="sxs-lookup"><span data-stu-id="0c1f0-103">Quantum Development Kit Full State Simulator</span></span>

<span data-ttu-id="0c1f0-104">O kit de desenvolvimento Quantum fornece um simulador de Quantum de estado completo semelhante a [Liq $ UI | \rangle $](http://stationq.github.io/Liquid/) da Microsoft Research.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-104">The Quantum Development Kit provides a full state quantum simulator similar to [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) from Microsoft Research.</span></span>
<span data-ttu-id="0c1f0-105">Esse simulador pode ser usado para executar e depurar algoritmos Quantum escritos em Q # no seu computador.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-105">This simulator can be used to execute and debug quantum algorithms written in Q# on your computer.</span></span>

<span data-ttu-id="0c1f0-106">Esse simulador Quantum é exposto por meio da classe `QuantumSimulator`.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-106">This quantum simulator is exposed via the `QuantumSimulator` class.</span></span> <span data-ttu-id="0c1f0-107">Para usar o simulador, basta criar uma instância dessa classe e passá-la para o método `Run` da operação Quantum que você deseja executar junto com o restante dos parâmetros:</span><span class="sxs-lookup"><span data-stu-id="0c1f0-107">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a><span data-ttu-id="0c1f0-108">IDisposable</span><span class="sxs-lookup"><span data-stu-id="0c1f0-108">IDisposable</span></span>

<span data-ttu-id="0c1f0-109">A classe `QuantumSimulator` implementa <xref:System.IDisposable>, portanto, o método `Dispose` deve ser chamado uma vez que a instância do simulador não seja mais usada.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-109">The `QuantumSimulator` class implements <xref:System.IDisposable>, thus the `Dispose` method should be called once the instance of the simulator is not used anymore.</span></span> <span data-ttu-id="0c1f0-110">A melhor maneira de fazer isso é encapsular o simulador em uma instrução `using`, como no exemplo acima.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-110">The best way to do this is to wrap the simulator within a `using` statement, as in the example above.</span></span>

## <a name="seed"></a><span data-ttu-id="0c1f0-111">Semente</span><span class="sxs-lookup"><span data-stu-id="0c1f0-111">Seed</span></span>

<span data-ttu-id="0c1f0-112">O `QuantumSimulator` usa um gerador de número aleatório para simular a aleatoriedade Quantum.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-112">The `QuantumSimulator` uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="0c1f0-113">Para fins de teste, às vezes é útil ter resultados determinísticos.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-113">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="0c1f0-114">Isso pode ser feito fornecendo uma semente para o gerador de números aleatórios no construtor do `QuantumSimulator`por meio do parâmetro `randomNumberGeneratorSeed`:</span><span class="sxs-lookup"><span data-stu-id="0c1f0-114">This can be accomplished by providing a seed for the random number generator in the `QuantumSimulator`'s constructor via the `randomNumberGeneratorSeed` parameter:</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a><span data-ttu-id="0c1f0-115">Threads</span><span class="sxs-lookup"><span data-stu-id="0c1f0-115">Threads</span></span>

<span data-ttu-id="0c1f0-116">O `QuantumSimulator` usa [OpenMP](http://www.openmp.org/) para paralelizar a Algebra linear necessária.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-116">The `QuantumSimulator` uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="0c1f0-117">Por padrão, o OpenMP usa todos os threads de hardware disponíveis, o que significa que os programas com pequenos números de qubits geralmente serão executados lentamente, pois a coordenação necessária irá Dwarf o trabalho real.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-117">By default OpenMP uses all available hardware threads, which means that programs with small numbers of qubits will often run slowly because the coordination required will dwarf the actual work.</span></span> <span data-ttu-id="0c1f0-118">Isso pode ser corrigido definindo a variável de ambiente `OMP_NUM_THREADS` como um número pequeno.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-118">This can be fixed by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="0c1f0-119">Como uma regra prática muito interessante, 1 thread é bom para até cerca de 4 qubits e, em seguida, um thread adicional por qubit é bom, embora isso seja altamente dependente de seu algoritmo.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-119">As a very rough rule of thumb, 1 thread is good for up to about 4 qubits, and then an additional thread per qubit is good, although this is highly dependent on your algorithm.</span></span>

