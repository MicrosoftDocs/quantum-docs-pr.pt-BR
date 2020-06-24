---
title: Kit de desenvolvimento do Quantum Toffoli simulador
description: Saiba mais sobre o simulador do Microsoft QDK Toffoli, um simulador de Quantum de finalidade especial que pode ser usado com milhões de qubits.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 8a29caaa0fa058600a74e7d130e644374cbfa19c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274320"
---
# <a name="quantum-development-kit-toffoli-simulator"></a>Kit de desenvolvimento do Quantum Toffoli simulador

O kit de desenvolvimento Quantum fornece um simulador de Toffoli, que é um simulador de finalidade especial que pode simular algoritmos de Quantum que são limitados a operações de Quantum x, CNOT e X com vários controle (toda a lógica clássica e cálculos estão disponíveis).

Embora o simulador de Toffoli seja muito mais restrito em operação do que o [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), ele pode simular muito mais qubits.
O simulador de Toffoli pode ser usado com milhões de qubits, enquanto o simulador de estado completo geralmente é limitado a cerca de 30.
Ele pode executar e depurar um conjunto limitado de algoritmos de Quantum escritos em Q # no seu computador; por exemplo, os Oracle que avaliam funções booleanas podem ser implementadas usando essas Gates e, portanto, são testadas para variar um grande número de qubits usando esse simulador.

Esse simulador Quantum é exposto por meio da `ToffoliSimulator` classe.
Para usar o simulador, basta criar uma instância dessa classe e passá-la para o `Run` método da operação Quantum que você deseja executar junto com o restante dos parâmetros:

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a>Outras operações

O `ToffoliSimulator` oferece suporte a rotações e exponenciação Paulis, como `R` e `Exp` , quando a operação resultante é igual `X` ou à identidade.

Há suporte para medição e Assert, mas apenas na `Z` base Pauli.
Observe que a probabilidade de alguma medida é sempre 0 ou 1; Não há aleatoriedade no simulador de Toffoli.

`DumpMachine`e `DumpRegister` têm suporte.
Ambos geram o `Z` estado da base atual de cada qubit, um qubit por linha.

## <a name="qubitcount"></a>QubitCount

Por padrão, o `ToffoliSimulator` aloca espaço para 65.536 qubits.
Se o algoritmo exigir mais do que isso, você poderá alterar a contagem de qubit fornecendo um valor para o `qubitCount` parâmetro para o construtor.
Cada qubit adicional requer um byte adicional de memória, portanto, não há nenhum custo significativo para a estimativa do número de qubits que você precisará.

Por exemplo:

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
