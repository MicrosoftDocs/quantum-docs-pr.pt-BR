---
title: Estimador de recursos do kit de desenvolvimento Quantum
description: 'Saiba mais sobre o estimador de recursos, que estima os recursos necessários para executar uma determinada instância de uma operação Q # em um computador Quantum.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 51186134e9279727fec212cdce84f69493aaa656
ms.sourcegitcommit: a0e50c5f07841b99204c068cf5b5ec8ed087ffea
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2020
ms.locfileid: "80320816"
---
# <a name="the-resourcesestimator-target-machine"></a>O computador de destino ResourcesEstimator

Como o nome indica, o `ResourcesEstimator` estima os recursos necessários para executar uma determinada instância de uma operação Q # em um computador Quantum.
Ele realiza isso executando a operação Quantum sem realmente simular o estado de um computador Quantum; por esse motivo, ele pode estimar recursos para operações Q # que usam milhares de qubits, se a parte clássica do código puder ser executada em um tempo razoável.

## <a name="usage"></a>Uso

O `ResourcesEstimator` é apenas outro tipo de computador de destino, portanto, ele pode ser usado para executar qualquer operação Q #. 

Como outros computadores de destino, para usá-lo C# em um programa de host, crie uma instância e passe-a como o primeiro parâmetro do método de `Run` da operação:

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

Como mostra o exemplo, o `ResourcesEstimator` fornece um método `ToTSV()` para gerar uma tabela com TSV (valores separados por tabulação) que podem ser salvos em um arquivo ou gravados no console para análise. A saída do programa acima deve ser semelhante a esta:

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
> O `ResourcesEstimator` não redefine seus cálculos em todas as execuções, se a mesma instância for usada para executar outra operação, ele continuará agregando contagens sobre os resultados existentes.
> Se você precisar redefinir cálculos entre execuções, crie uma nova instância para cada execução.


## <a name="programmatically-retrieving-the-estimated-data"></a>Recuperando programaticamente os dados estimados

Além de uma tabela TSV, os recursos estimados podem ser recuperados programaticamente por meio da propriedade `Data` do `ResourcesEstimator`. `Data` fornece uma instância de `System.DataTable` com duas colunas: `Metric` e `Sum`, indexadas pelos nomes de métricas.

O código a seguir mostra como recuperar e imprimir o número total de `QubitClifford`, `T` e `CNOT` Gates usados por uma operação Q #:

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

## <a name="metrics-reported"></a>Métricas relatadas

A seguir está a lista de métricas estimadas pelo `ResourcesEstimator`:

* __CNOT__: a contagem de CNOT (também conhecida como a porta controlada de Pauli X) de Gates executada.
* __QubitClifford__: a contagem de uma única qubit Clifford e Pauli Gates executadas.
* __Medida__: a contagem de qualquer medida executada.
* __R__: a contagem de qualquer rotação qubit única executada, excluindo T, Clifford e Pauli Gates.
* __T__: a contagem de t Gates e seus conjugados, incluindo o Gate t, T_x = h. T. H e T_y = hipótese. T. hipótese, executado.
* __Profundidade__: profundidade do circuito Quantum executado pela operação Q #. Por padrão, somente T Gates são contadas na profundidade, consulte o [contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) para obter detalhes.
* __Largura__: o número máximo de qubits alocadas durante a execução da operação Q #.
* __BorrowedWidth__: número máximo de qubits emprestados dentro da operação Q #.


## <a name="providing-the-probability-of-measurement-outcomes"></a>Como fornecer a probabilidade de resultados de medida

<xref:microsoft.quantum.intrinsic.assertprob> do namespace <xref:microsoft.quantum.intrinsic> pode ser usado para fornecer informações sobre a probabilidade esperada de uma medida para ajudar a conduzir a execução do programa Q #. O exemplo a seguir ilustra isso:

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

Quando o `ResourcesEstimator` encontrar `AssertProb` ele gravará que medir `PauliZ` em `source` e `q` deverá receber um resultado de `Zero` com a probabilidade 0,5. Quando ele for executado `M` mais tarde, ele encontrará os valores gravados das probabilidades de resultado e `M` retornará `Zero` ou `One` com a probabilidade 0,5.


## <a name="see-also"></a>Confira também

O `ResourcesEstimator` é criado sobre o [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum, que fornece um conjunto mais rico de métricas, a capacidade de relatar métricas no grafo de Call completo e recursos como o [Verificador de entradas distintos](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) para ajudar a encontrar bugs em programas de Q #. Consulte a documentação do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) para obter mais informações.

