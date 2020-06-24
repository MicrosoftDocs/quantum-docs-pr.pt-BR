---
title: Simulador de estado completo
description: 'Saiba como executar seus programas do Q # no Microsoft Quantum Development Kit o simulador de estado completo.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: f73abbc4366b003e4b22366ed83ca9c897737307
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274268"
---
# <a name="quantum-development-kit-full-state-simulator"></a>Simulador de estado completo do kit de desenvolvimento do Quantum

O kit de desenvolvimento Quantum fornece um simulador de Quantum de estado completo semelhante a [Liq $ UI | \rangle $](http://stationq.github.io/Liquid/) da Microsoft Research.
Esse simulador pode ser usado para executar e depurar algoritmos Quantum escritos em Q # no seu computador.

Esse simulador Quantum é exposto por meio da `QuantumSimulator` classe. Para usar o simulador, basta criar uma instância dessa classe e passá-la para o `Run` método da operação Quantum que você deseja executar junto com o restante dos parâmetros:

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a>IDisposable

A `QuantumSimulator` classe implementa <xref:System.IDisposable> , portanto, o `Dispose` método deve ser chamado uma vez que a instância do simulador não seja mais usada. A melhor maneira de fazer isso é encapsular o simulador em uma `using` instrução, como no exemplo acima.

## <a name="seed"></a>Seed

O `QuantumSimulator` usa um gerador de números aleatórios para simular a aleatoriedade da Quantum. Para fins de teste, às vezes é útil ter resultados determinísticos. Isso pode ser feito fornecendo uma semente para o gerador de número aleatório no `QuantumSimulator` construtor do por meio do `randomNumberGeneratorSeed` parâmetro:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Threads

O `QuantumSimulator` usa [OpenMP](http://www.openmp.org/) para paralelizar a Algebra linear necessária. Por padrão, o OpenMP usa todos os threads de hardware disponíveis, o que significa que programas com pequenos números de qubits geralmente serão executados lentamente, pois a coordenação necessária reduzirá o trabalho real. Isso pode ser corrigido definindo a variável de ambiente `OMP_NUM_THREADS` como um número pequeno. Como uma regra prática muito ampla, 1 thread é adequado para até cerca de 4 qubits e, em seguida, 1 thread adicional por qubit é adequado, embora isso seja altamente dependente de seu algoritmo.

