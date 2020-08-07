---
title: Quantum Toffoli Simulator-kit de desenvolvimento do Quantum
description: Saiba mais sobre o simulador do Microsoft QDK Toffoli, um simulador de Quantum de finalidade especial que pode ser usado com milhões de qubits.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8a981645703423856e667be7c3dccf5270a5885f
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868093"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a>Simulador do QDK (Kit de desenvolvimento do Quantum) Toffoli

O simulador QDK Toffoli é um simulador de finalidade especial com escopo limitado e só dá suporte a `X` `CNOT` operações de Quantum com vários controle, e `X` . Toda a lógica clássica e os cálculos estão disponíveis.

Embora o simulador de Toffoli seja mais restrito em funcionalidade do que o [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), ele tem a vantagem de ser capaz de simular muito mais qubits. O simulador de Toffoli pode ser usado com milhões de qubits, enquanto o simulador de estado completo é limitado a cerca de 30 qubits. Isso é útil, por exemplo, com ORACLES que avaliam funções booleanas – elas podem ser implementadas usando o conjunto limitado de algoritmos com suporte e testadas em um grande número de qubits.

## <a name="invoking-the-toffoli-simulator"></a>Invocando o simulador de Toffoli

Você expõe o simulador Toffoli por meio da `ToffoliSimulator` classe. Para obter detalhes adicionais, consulte [maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-toffoli-simulator-from-c"></a>Invocando o simulador de Toffoli de C #

Assim como acontece com outros computadores de destino, primeiramente você cria uma instância da classe `ToffoliSimulator` e, em seguida, passa-a como o primeiro parâmetro do método `Run` de uma operação.

Observe que, diferentemente da classe `QuantumSimulator`, a classe `ToffoliSimulator` não implementa a interface <xref:System.IDisposable> e, portanto, você não precisa colocá-la em uma instrução `using`.

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a>Invocando o simulador de Toffoli do Python

Use o método [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) da biblioteca do Python com a operação importada Q# :

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a>Invocando o simulador Toffoli da linha de comando

Ao executar um Q# programa a partir da linha de comando, use o parâmetro **--Simulator** (ou **-s** Shortcut) para especificar o computador de destino do simulador de Toffoli. O comando a seguir executa um programa usando o estimador de recursos: 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a>Invocando o simulador do Toffoli de blocos de anotações do Juptyer

Use o Q# comando mágico I [% Toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) para executar a Q# operação.

```
%toffoli myOperation
```

## <a name="supported-operations"></a>Operações com suporte

O simulador do Toffoli dá suporte a:

* Rotações e exponenciação Paulis, como `R` e `Exp` , quando a operação resultante é igual a `X` ou a matriz de identidade.
* Operações de medição e [declaração](xref:microsoft.quantum.diagnostics.assertmeasurement) , mas apenas na `Z` base Pauli. Observe que a probabilidade de uma operação de medida é sempre **0** ou **1**; Não há aleatoriedade no simulador de Toffoli.
* `DumpMachine`e `DumpRegister` funções.
Ambas as funções produzem o `Z` estado de base atual de cada qubit, uma qubit por linha.

## <a name="specifying-the-number-of-qubits"></a>Especificando o número de qubits

Por padrão, uma `ToffoliSimulator` instância aloca espaço para 65.536 qubits.
Se o algoritmo exigir mais qubits do que isso, você poderá especificar a contagem de qubit fornecendo um valor para o `qubitCount` parâmetro para o construtor.
Cada qubit adicional requer apenas um byte de memória, portanto, não há nenhum custo significativo para a estimativa do número de qubits que você precisará.

Por exemplo:

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a>Confira também

- [Estimador de recursos Quantum](xref:microsoft.quantum.machines.resources-estimator)
- [Simulador de rastreamento Quantum](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Simulador de estado completo Quantum](xref:microsoft.quantum.machines.full-state-simulator) 