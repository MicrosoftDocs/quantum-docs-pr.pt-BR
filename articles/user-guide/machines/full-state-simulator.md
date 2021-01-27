---
title: Simulador de Quantum de estado completo – kit de desenvolvimento do Quantum
description: Saiba como executar seus Q# programas no Microsoft Quantum Development Kit o simulador de estado completo.
author: anpaz
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.full-state-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 950e61c812cc6df739ddaa1de855f753557d6d1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858182"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a>Simulador de estado completo do QDK (Kit de desenvolvimento do Quantum)

O QDK fornece um simulador de estado completo que simula um computador Quantum em seu computador local. Você pode usar o simulador de estado completo para executar e depurar algoritmos de Quantum escritos em Q# , utilizando até 30 qubits. O simulador de estado completo é semelhante ao simulador do Quantum usado na  [interface do usuário do Liq $ | \rangle $](http://stationq.github.io/Liquid/) da Microsoft Research.

## <a name="invoking-and-running-the-full-state-simulator"></a>Invocando e executando o simulador de estado completo

Você expõe o simulador de estado completo por meio da `QuantumSimulator` classe. Para obter detalhes adicionais, consulte [maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-simulator-from-c"></a>Invocando o simulador a partir de C #

Crie uma instância da `QuantumSimulator` classe e, em seguida, passe-a para o `Run` método de uma operação Quantum, juntamente com quaisquer parâmetros adicionais.
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

Como a `QuantumSimulator` classe implementa a <xref:System.IDisposable> interface, você deve chamar o `Dispose` método assim que não precisar mais da instância do simulador. A melhor maneira de fazer isso é encapsular a declaração de simulador e as operações em uma instrução [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) , que chama automaticamente o `Dispose` método.

### <a name="invoking-the-simulator-from-python"></a>Invocando o simulador do Python

Use o método [simular ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) da Q# biblioteca do Python com a operação importada Q# :

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a>Invocando o simulador a partir da linha de comando

Ao executar um Q# programa a partir da linha de comando, o simulador de estado completo é o computador de destino padrão. Opcionalmente, você pode usar o parâmetro **--Simulator** (ou **-s** Shortcut) para especificar o computador de destino desejado. Ambos os comandos a seguir executam um programa usando o simulador de estado completo. 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a>Invocando o simulador de notebooks Juptyer

Use o Q# comando mágico I [% simular](xref:microsoft.quantum.iqsharp.magic-ref.simulate) para executar a Q# operação.

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a>Propagando o simulador

Por padrão, o simulador de estado completo usa um gerador de número aleatório para simular a aleatoriedade Quantum. Para fins de teste, às vezes é útil ter resultados determinísticos. Em um programa em C#, você pode fazer isso fornecendo uma semente para o gerador de números aleatórios no `QuantumSimulator` Construtor por meio do `randomNumberGeneratorSeed` parâmetro.

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a>Configurando threads

O simulador de estado completo usa [OpenMP](http://www.openmp.org/) para paralelizar a Algebra linear necessária. Por padrão, o OpenMP usa todos os threads de hardware disponíveis, o que significa que programas com pequenos números de qubits geralmente são executados lentamente porque a coordenação necessária Dwarfs o trabalho real. Você pode corrigir isso definindo a variável de ambiente `OMP_NUM_THREADS` para um número pequeno. Como regra prática, configure um thread para até quatro qubits e, em seguida, um thread adicional por qubit. Talvez seja necessário ajustar a variável dependendo do algoritmo.

## <a name="see-also"></a>Confira também

- [Avaliador de recursos quânticos](xref:microsoft.quantum.machines.resources-estimator)
- [Simulador quântico do Toffoli](xref:microsoft.quantum.machines.toffoli-simulator)
- [Simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)