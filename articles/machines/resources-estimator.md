---
title: Estimador de recursos do kit de desenvolvimento Quantum
description: 'Saiba mais sobre o estimador de recursos, que estima os recursos necessários para executar uma determinada instância de uma operação Q # em um computador Quantum.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: b0c800c3946d2e4ba4457127fb9495dc9dcf2934
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630125"
---
# <a name="the-resources-estimator-target-machine"></a>O computador de destino do avaliador de recursos

Como o nome indica, o `ResourcesEstimator` estima os recursos necessários para executar uma determinada instância de uma operação Q # em um computador Quantum.
Ele realiza isso executando a operação Quantum sem realmente simular o estado de um computador Quantum; por esse motivo, ele pode estimar recursos para operações Q # que usam milhares de qubits, se a parte clássica do código puder ser executada em um tempo razoável.

## <a name="usage"></a>Uso

O `ResourcesEstimator` é apenas outro tipo de computador de destino, portanto, ele pode ser usado para executar qualquer operação Q #. 

Como outros computadores de destino, para usá-lo em um programa de host C#, crie uma instância e passe-a como o primeiro parâmetro do método da operação `Run` :

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

Como mostra o exemplo, o `ResourcesEstimator` fornece um `ToTSV()` método para gerar uma tabela com TSV (valores separados por tabulação) que podem ser salvos em um arquivo ou gravados no console para análise. A saída do programa acima deve ser semelhante a esta:

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
> O `ResourcesEstimator` não redefine seus cálculos em cada execução, se a mesma instância for usada para executar outra operação, ele continuará agregando contagens sobre os resultados existentes.
> Se você precisar redefinir cálculos entre execuções, crie uma nova instância para cada execução.


## <a name="programmatically-retrieving-the-estimated-data"></a>Recuperando programaticamente os dados estimados

Além de uma tabela TSV, os recursos estimados podem ser recuperados programaticamente por meio da `ResourcesEstimator` `Data` Propriedade do. `Data`fornece uma `System.DataTable` instância com duas colunas: `Metric` e `Sum` , indexada pelos nomes de métricas.

O código a seguir mostra como recuperar e imprimir o número total de `QubitClifford` `T` e `CNOT` Gates usados por uma operação Q #:

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

A seguir está a lista de métricas estimada pelo `ResourcesEstimator` :

* __CNOT__: a contagem de CNOT (também conhecida como a porta controlada de Pauli X) de Gates executada.
* __QubitClifford__: a contagem de uma única qubit Clifford e Pauli Gates executadas.
* __Medida__: a contagem de qualquer medida executada.
* __R__: a contagem de qualquer rotação qubit única executada, excluindo T, Clifford e Pauli Gates.
* __T__: a contagem de t Gates e seus conjugados, incluindo o Gate t, T_x = h. T. H e T_y = hipótese. T. hipótese, executado.
* __Profundidade__: profundidade do circuito Quantum executado pela operação Q #. Por padrão, somente T Gates são contadas na profundidade, consulte o [contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) para obter detalhes.
* __Largura__: o número máximo de qubits alocadas durante a execução da operação Q #.
* __BorrowedWidth__: número máximo de qubits emprestados dentro da operação Q #.


## <a name="providing-the-probability-of-measurement-outcomes"></a>Como fornecer a probabilidade de resultados de medida

<xref:microsoft.quantum.intrinsic.assertprob>do <xref:microsoft.quantum.intrinsic> namespace pode ser usado para fornecer informações sobre a probabilidade esperada de uma medida para ajudar a conduzir a execução do programa Q #. O exemplo a seguir ilustra isso:

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

Quando o `ResourcesEstimator` encontrar `AssertProb` , ele registrará essa `PauliZ` medição `source` e `q` deverá receber um resultado de `Zero` com a probabilidade 0,5. Quando ele for executado `M` posteriormente, ele encontrará os valores gravados das probabilidades de resultado e `M` retornará `Zero` ou `One` com a probabilidade 0,5.


## <a name="see-also"></a>Confira também

O `ResourcesEstimator` é criado com base no [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro)de computador Quantum, que fornece um conjunto mais rico de métricas, a capacidade de relatar métricas no grafo de Call completo e recursos como o [corretor de entradas distintos](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) para ajudar a encontrar bugs em programas de Q #. Consulte a documentação do [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro) para obter mais informações.

