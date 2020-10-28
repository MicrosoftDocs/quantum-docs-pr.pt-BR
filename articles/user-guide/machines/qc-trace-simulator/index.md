---
title: Simulador de rastreamento quântico – Quantum Development Kit
description: Aprenda a usar o simulador de rastreamento do computador quântico da Microsoft para depurar código clássico e estimar os requisitos de recursos de um programa Q#.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2e2d9f8494d8709fba34123793cecce4011b609a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690834"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a>Simulador de rastreamento quântico do Microsoft QDK (Quantum Development Kit)

A classe QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> executa um programa quântico sem realmente simular o estado de um computador quântico. Por esse motivo, o simulador de rastreamento quântico pode executar programas quânticos que usam milhares de qubits.  Ele é útil para duas finalidades principais: 

* Depuração de código clássico que faça parte de um programa quântico. 
* Estimativa dos recursos necessários para executar determinada instância de um programa quântico em um computador quântico. Na verdade, o [Avaliador de recursos](xref:microsoft.quantum.machines.resources-estimator), que fornece um conjunto mais limitado de métricas, é criado com base no simulador de rastreamento.

## <a name="invoking-the-quantum-trace-simulator"></a>Invocando o simulador de rastreamento quântico

É possível usar o simulador de rastreamento quântico para executar qualquer operação Q#.

Assim como acontece com outros computadores de destino, primeiramente você cria uma instância da classe `QCTraceSimulator` e, em seguida, passa-a como o primeiro parâmetro do método `Run` de uma operação.

Observe que, diferentemente da classe `QuantumSimulator`, a classe `QCTraceSimulator` não implementa a interface <xref:System.IDisposable> e, portanto, você não precisa colocá-la em uma instrução `using`.

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a>Como fornecer a probabilidade de resultados de medida

Como o simulador de rastreamento quântico não simula o estado real quântico, ele não pode calcular a probabilidade de resultados de medida em uma operação. 

Portanto, se uma operação incluir medidas, você precisará fornecer explicitamente essas probabilidades usando a operação <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> do namespace <xref:Microsoft.Quantum.Diagnostics>. O exemplo a seguir ilustra isso:

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

Quando o simulador de rastreamento quântico executar `AssertMeasurementProbability`, ele registrará isso medindo `PauliZ` em `source` e `q` deverá mostrar um resultado igual a `Zero` com a probabilidade de **0,5** . Quando ele executar a operação `M` posteriormente, ele localizará os valores gravados das probabilidades de resultado e `M` retornará `Zero` ou `One`, com a probabilidade de **0,5** . Quando o mesmo código for executado em um simulador que controla o estado quântico, esse simulador verificará se as probabilidades fornecidas em `AssertMeasurementProbability` estão corretas.

Observe que, se houver pelo menos uma operação de medida que não está anotada usando `AssertMeasurementProbability`, o simulador gerará um [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).

## <a name="quantum-trace-simulator-tools"></a>Ferramentas de simulador de rastreamento quântico

O QDK inclui cinco ferramentas que você pode usar com o simulador de rastreamento quântico para detectar bugs nos seus programas e executar estimativas de recursos do programa quântico: 

|Ferramenta | Descrição |
|-----| -----|
|[Verificador de entradas distintas](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |Verifica se há conflitos potenciais com qubits compartilhados |
|[Verificador de uso de qubits invalidados](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |Verifica se o programa aplica uma operação a um qubit que já foi liberado |
|[Contador de operações primitivas](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | Conta o número de primitivos usados em cada operação invocada em um programa quântico  |
|[Contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |Coleta contagens que representam o limite inferior da profundidade de cada operação invocada em um programa quântico   |
|[Contador de largura](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |Conta o número de qubits alocados e emprestados em cada operação em um programa quântico |

Cada uma dessas ferramentas é habilitada definindo sinalizadores apropriados no `QCTraceSimulatorConfiguration` e, em seguida, passando a configuração para a declaração de `QCTraceSimulator`. Para obter informações sobre como usar cada uma dessas ferramentas, confira os links na lista anterior. Para obter mais informações sobre como configurar o `QCTraceSimulator`, confira [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).

## <a name="qctracesimulator-methods"></a>Métodos QCTraceSimulator

O `QCTraceSimulator` tem vários métodos internos para recuperar os valores das métricas rastreadas durante uma operação quântica. Exemplos dos métodos [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) e [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) podem ser encontrados nos artigos [Contador de operações primitivo](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) e [Contador de largura](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter). Para saber mais sobre todos os métodos disponíveis, confira [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) na referência da API do Q#.  

## <a name="see-also"></a>Confira também

- [Avaliador de recursos quânticos](xref:microsoft.quantum.machines.resources-estimator)
- [Simulador quântico do Toffoli](xref:microsoft.quantum.machines.toffoli-simulator)
- [Simulador de estado completo quântico](xref:microsoft.quantum.machines.full-state-simulator) 