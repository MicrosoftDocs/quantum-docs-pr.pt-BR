---
title: Simuladores quânticos e programas Q#
description: Descreve os simuladores quânticos disponíveis como computadores de destino para programas Q#.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 6/17/2020
ms.topic: article
uid: microsoft.quantum.machines
no-loc:
- Q#
- $$v
ms.openlocfilehash: 77401ca3642b89d708f338f852dc60bf7346b87b
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868297"
---
# <a name="quantum-simulators"></a>Simuladores quânticos

Simuladores quânticos são programas de software executados em computadores clássicos e atuam como um *computador de destino* para um programa Q#. Assim, é possível executar e testar programas quânticos em um ambiente que prevê como os qubits reagem a diferentes operações. Este artigo descreve os simuladores quânticos incluídos no QDK (Quantum Development Kit) e maneiras diferentes de passar um programa Q# para os simuladores quânticos, por exemplo, por meio da linha de comando ou usando o código de driver escrito em uma linguagem clássica.  



## <a name="the-quantum-development-kit-qdk-quantum-simulators"></a>Atualizar os simuladores quânticos do QDK (Quantum Development Kit)

O simulador quântico é responsável por fornecer implementações de primitivos quânticos para o algoritmo. Isso inclui operações primitivas, como `H`, `CNOT` e `Measure`, bem como gerenciamento e acompanhamento de qubits. O QDK inclui diferentes classes de simuladores quânticos que representam modelos de execução diferentes para o mesmo algoritmo quântico. 


Cada tipo de simulador quântico pode fornecer diferentes implementações desses primitivos. Por exemplo, o [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator) executa o algoritmo quântico ao simular totalmente o [vetor de estado quântico](xref:microsoft.quantum.glossary#quantum-state), enquanto o [simulador de rastreamento de computador quântico](xref:microsoft.quantum.machines.qc-trace-simulator.intro) não considera o estado quântico real. Em vez disso, ele rastreia o uso de portões, qubits e outros recursos para o algoritmo.

### <a name="quantum-machine-classes"></a>Classes de computador quântico

No futuro, o QDK definirá classes adicionais de computadores quânticos para dar suporte a outros tipos de simulação e a execução em hardware quântico. Permitir que o algoritmo permaneça constante enquanto varia a implementação de computador subjacente facilita o teste e a depuração de um algoritmo em simulação e, em seguida, executa-o em um hardware real com a confiança de que o algoritmo não foi alterado.

O QDK inclui várias classes de computadores quânticos, todas definidas no namespace `Microsoft.Quantum.Simulation.Simulators`.

|Simulador |Classe|Descrição|
|-----|------|---|
|[Simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator)| `QuantumSimulator` | Executa e depura algoritmos quânticos e é limitado a cerca de 30 qubits. |
|[Avaliador de recursos simples](xref:microsoft.quantum.machines.resources-estimator)| `ResourcesEstimator` | Realiza uma análise de nível superior dos recursos necessários para executar um algoritmo quântico e dá suporte a milhares de qubits.|
|[Avaliador de recursos baseado em rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)|  `QCTraceSimulator` |Executa uma análise avançada de consumos de recursos para todo o grafo de chamadas do algoritmo e dá suporte a milhares de qubits.|
|[Simulador do Toffoli](xref:microsoft.quantum.machines.toffoli-simulator)| `ToffoliSimulator` |Simula os algoritmos quânticos que são limitados a `X`, `CNOT` e a operações quânticas `X` com vários controles e dá suporte a milhões de qubits. |

## <a name="invoking-the-quantum-simulator"></a>Invocando o simulador quântico

Em [Maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs), três modos de passar o código Q# para o simulador quântico são demonstrados: 

* Usando a linha de comando
* Usando um programa de host em Python
* Usando um programa de host em C#

Os computadores quânticos são instâncias de classes .NET normais e, portanto, são criadas invocando o construtor delas, assim como qualquer classe .NET. O procedimento depende de como você executa o programa Q#.

## <a name="next-steps"></a>Próximas etapas

* Para saber detalhes sobre como invocar computadores de destino para programas Q# em ambientes distintos, confira [Maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).
