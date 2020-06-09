---
title: Simulador de rastreamento de computador do Quantum
description: Aprenda a usar o simulador de rastreamento de computador do Microsoft Quantum para depurar código clássico e estimar os requisitos de recursos de um programa quântico.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 4cec688da35951271d87396d9b6a8fed744defc6
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84577658"
---
# <a name="quantum-trace-simulator"></a>Simulador de rastreamento quântico

O simulador de rastreamento de computador quântico da Microsoft executa um programa quântico sem realmente simular o estado de um computador quântico.  Por esse motivo, o simulador de rastreamento pode executar programas quânticos que usam milhares de qubits.  Ele é útil para duas finalidades principais: 

* Depuração de código clássico que faça parte de um programa quântico. 
* Estimativa dos recursos necessários para executar determinada instância de um programa quântico em um computador quântico.

O simulador de rastreamento depende de informações adicionais fornecidas pelo usuário de quando as medidas precisam ser executadas. Confira a seção [Como fornecer a probabilidade de resultados de medida](#providing-the-probability-of-measurement-outcomes) para obter mais detalhes sobre esse tópico. 

## <a name="providing-the-probability-of-measurement-outcomes"></a>Como fornecer a probabilidade de resultados de medida

Há dois tipos de medidas que aparecem em algoritmos quânticos. O primeiro tipo desempenha uma função auxiliar em que o usuário geralmente conhece a probabilidade dos resultados. Nesse caso, o usuário pode escrever <xref:microsoft.quantum.intrinsic.assertprob> por meio do namespace <xref:microsoft.quantum.intrinsic> para expressar esse conhecimento. O exemplo a seguir ilustra isso:

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

Quando o simulador de rastreamento executar `AssertProb`, ele registrará isso medindo `PauliZ` em `source`, e `q` deverá receber um resultado igual a `Zero` com a probabilidade 0,5. Quando o simulador executar `M` mais tarde, ele encontrará os valores registrados das probabilidades de resultado e `M` retornará `Zero` ou `One` com a probabilidade 0,5. Quando o mesmo código for executado em um simulador que controla o estado quântico, esse simulador verificará se as probabilidades fornecidas em `AssertProb` estão corretas.

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a>Como executar o programa com o simulador de rastreamento de computador quântico 

O simulador de rastreamento de computador quântico pode ser exibido como qualquer outro computador de destino. O programa de driver C# para usá-lo é muito semelhante ao de qualquer outro simulador de quantum: 

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

Observe que, se houver pelo menos uma medida não anotada usando `AssertProb`, o simulador gerará `UnconstrainedMeasurementException` por meio do namespace `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators`. Confira a documentação da API em [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) para obter mais detalhes.

Além de executar programas quânticos, o simulador de rastreamento é fornecido com cinco componentes para detectar bugs em programas e executar estimativas de recursos de programa quântico: 

* [Verificador de Entradas Distintas](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [Verificador de Uso de Qubits Invalidados](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [Contador de Operações Primitivas](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [Contador da Profundidade de Circuito](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)
* [Contador da Largura de Circuito](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)

Cada um desses componentes pode ser habilitado pela definição de sinalizadores apropriados em `QCTraceSimulatorConfiguration`. Mais detalhes sobre como usar cada um desses componentes são fornecidos nos arquivos de referência correspondentes. Confira a documentação da API em [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) para obter detalhes específicos.

## <a name="see-also"></a>Confira também
A referência de C# do [simulador de rastreamento](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) de computador quântico 

