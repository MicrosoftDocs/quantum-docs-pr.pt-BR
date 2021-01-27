---
title: Estimador de recursos do Quantum – kit de desenvolvimento do Quantum
description: Saiba mais sobre o estimador de recursos do Microsoft QDK, que estima os recursos necessários para executar uma determinada instância de uma Q# operação em um computador Quantum.
author: anpaz
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: c3aa94c8b34ad7247fbdeab4bf4dcb96ce746014
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847473"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a>Estimador de recursos do kit de desenvolvimento Quantum (QDK)

Como o nome indica, a `ResourcesEstimator` classe estima os recursos necessários para executar uma determinada instância de uma Q# operação em um computador Quantum. Ele realiza isso executando a operação Quantum sem realmente simular o estado de um computador Quantum; por esse motivo, ele estima recursos para Q# operações que usam milhares de qubits, desde que a parte clássica do código seja executada em um tempo razoável.

O estimador de recursos é criado sobre o [simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro), que fornece um conjunto mais rico de métricas e ferramentas para ajudar a depurar Q# programas.

## <a name="invoking-and-running-the-resources-estimator"></a>Invocando e executando o estimador de recursos

Você pode usar o estimador de recursos para executar qualquer Q# operação. Para obter detalhes adicionais, consulte [maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-resources-estimator-from-c"></a>Invocando o estimador de recursos de C # 

Assim como acontece com outros computadores de destino, primeiramente você cria uma instância da classe `ResourcesEstimator` e, em seguida, passa-a como o primeiro parâmetro do método `Run` de uma operação.

Observe que, diferentemente da classe `QuantumSimulator`, a classe `ResourcesEstimator` não implementa a interface <xref:System.IDisposable> e, portanto, você não precisa colocá-la em uma instrução `using`.

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

Como mostra o exemplo, o `ResourcesEstimator` fornece o `ToTSV()` método, que gera uma tabela com valores separados por tabulações (TSV). Você pode salvar a tabela em um arquivo ou exibi-la no console para análise. Veja a seguir um exemplo de saída do programa anterior:

```output
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
> Uma `ResourcesEstimator` instância do não redefine seus cálculos em todas as execuções. Se você usar a mesma instância para executar outra operação, ela agregará os novos resultados com os resultados existentes. Se você precisar redefinir cálculos entre execuções, crie uma nova instância para cada execução.

### <a name="invoking-the-resources-estimator-from-python"></a>Invocando o estimador de recursos do Python

Use o método [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) da biblioteca do Python com a operação importada Q# :

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a>Invocando o estimador de recursos da linha de comando

Ao executar um Q# programa a partir da linha de comando, use o parâmetro **--Simulator** (ou **-s** Shortcut) para especificar o `ResourcesEstimator` computador de destino. O comando a seguir executa um programa usando o estimador de recursos: 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a>Invocando o estimador de recursos de notebooks Juptyer

Use a Q# [estimativa de%](xref:microsoft.quantum.iqsharp.magic-ref.simulate) de comando mágico mágica para executar a Q# operação.

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a>Recuperando programaticamente os dados estimados

Além de uma tabela TSV, você pode recuperar programaticamente os recursos estimados durante a execução por meio da `Data` Propriedade do estimador de recursos. A `Data` propriedade fornece uma `System.DataTable` instância com duas colunas: `Metric` e `Sum` , indexada pelos nomes de métricas.

O código a seguir mostra como recuperar e imprimir o número total de `QubitClifford` `T` e `CNOT` as operações usadas por uma Q# operação:

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

O estimador de recursos acompanha as seguintes métricas:

|Métrica|Descrição|
|----|----|
|__CNOT__    |A contagem de operações de execução `CNOT` (também conhecida como operações Pauli X controladas).|
|__QubitClifford__ |A contagem de execuções de uma única qubit Clifford e operações de Pauli.|
|__Medida__    |A contagem de execuções de qualquer medida.  |
|__R__    |A contagem de execuções de qualquer rotação de qubit única, excluindo `T` , Clifford e Pauli operações.  |
|__T__    |A contagem de execuções de `T` operações e seus conjugados, incluindo as `T` operações, T_x = h. T. H e T_y = hipótese. T. hipótese.  |
|__Profundidade__|Profundidade do circuito Quantum executado pela Q# operação (veja [abaixo](#depth-width-and-qubitcount)). Por padrão, a métrica de profundidade conta apenas `T` Gates. Para obter mais detalhes, consulte o [contador de profundidade](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).   |
|__Largura__|Largura do circuito Quantum executada pela Q# operação (veja [abaixo](#depth-width-and-qubitcount)). Por padrão, a métrica de profundidade conta apenas `T` Gates. Para obter mais detalhes, consulte [contador de largura](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).   |
|__QubitCount__    |O limite inferior para o número máximo de qubits alocadas durante a execução da Q# operação. Essa métrica pode não ser compatível com __profundidade__ (veja abaixo).  |
|__BorrowedWidth__    |O número máximo de qubits emprestados dentro da Q# operação.  |


## <a name="depth-width-and-qubitcount"></a>Profundidade, largura e QubitCount

As estimativas de profundidade e largura relatadas são compatíveis entre si.
(Anteriormente, os dois números eram atingíveis, mas circuitos diferentes seriam necessários para profundidade e largura.) Atualmente, ambas as métricas nesse par podem ser obtidas pelo mesmo circuito ao mesmo tempo.

As seguintes métricas são relatadas:

__Profundidade:__ Para a operação raiz, o tempo necessário para executá-lo, supondo que os tempos de portão configurados.
Para operações chamadas ou a diferença de tempo de operações subsequentes entre o tempo de disponibilidade qubit mais recente no início e no fim da operação.

__Largura:__ Para a operação raiz-número de qubits realmente usados para executá-lo (e operação que ele chama).
Para operações chamadas ou operações subsequentes, quantos mais qubits foram usados, além do qubits já usado no início da operação.

Observe que os qubits reutilizados não contribuem para esse número.
Ou seja, se alguns qubits tiverem sido liberados antes da operação A ser iniciada, e todas as qubit exigidas por essa operação A (e as operações chamadas de A) fossem satisfeitas com a reutilização da versão anterior qubits, a largura da operação A é relatada como 0. Os qubits emprestados com êxito não contribuem com a largura.

__QubitCount:__ Para a operação raiz-número mínimo de qubits que seriam suficientes para executar esta operação (e as operações chamadas a partir dela).
Para operações chamadas ou operações subsequentes-número mínimo de qubits que seriam suficientes para executar essa operação separadamente. Esse número não inclui qubits de entrada. Ele inclui qubits emprestado.

Há suporte para dois modos de operação. É selecionado por meio da configuração de QCTraceSimulatorConfiguration. OptimizeDepth.

__OptimizeDepth = false:__ Esse é o modo padrão. QubitManager é incentivado a reutilizar o qubits e reutilizará o qubits liberado antes de alocar novos. Para a __largura__ da operação raiz se torna a largura mínima (limite inferior). A __profundidade__ compatível é relatada na qual ela pode ser obtida. __QubitCount__ será igual à __largura__ da operação raiz, supondo que não haja empréstimo.

__OptimizeDepth = true:__ QubitManager é desencorajado da reutilização de qubit e a otimização baseada em heurística para a reutilização de qubit é executada durante e após a execução. Para a __profundidade__ da operação raiz se torna a profundidade mínima (limite inferior). A __largura__ compatível é relatada para essa profundidade (ambas podem ser obtidas ao mesmo tempo). Para otimizar a largura, as Gates encontradas posteriormente no programa podem ser agendadas antes que as Gates encontradas anteriormente no programa, mas qubits estão agendadas para serem reutilizadas de forma que a profundidade permaneça mínima. Como os qubits são reutilizados com base nos valores de tempo, é recomendável que os tempos de portão sejam configurados para serem valores inteiros. Não há garantia de que a __largura__ seja ideal. Mais informações podem ser encontradas na [largura e na profundidade do whitepaper no rastreador](https://github.com/microsoft/qsharp-runtime/tree/main/src/Simulation/Simulators/QCTraceSimulator/Docs).

## <a name="providing-the-probability-of-measurement-outcomes"></a>Como fornecer a probabilidade de resultados de medida

Você pode usar <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> do <xref:Microsoft.Quantum.Diagnostics> namespace para fornecer informações sobre a probabilidade esperada de uma operação de medição. Para obter mais informações, consulte o [simulador de rastreamento do Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)

## <a name="see-also"></a>Confira também

- [Simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Simulador quântico do Toffoli](xref:microsoft.quantum.machines.toffoli-simulator)
- [Simulador de estado completo quântico](xref:microsoft.quantum.machines.full-state-simulator) 
