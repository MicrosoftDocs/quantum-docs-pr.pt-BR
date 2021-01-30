---
uid: Microsoft.Quantum.Simulation.PauliEvolutionImpl
title: Operação PauliEvolutionImpl
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.

  See [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 1c588c225cb7c91830e986c7eca9b9fafd445d4e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847940"
---
# <a name="paulievolutionimpl-operation"></a>Operação PauliEvolutionImpl

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa um gerador dinâmico como um conjunto de Gates e uma expansão na base Pauli.

Consulte [modelagem de gerador dinâmico](/quantum/libraries/data-structures#dynamical-generator-modeling) para obter mais detalhes.

```qsharp
operation PauliEvolutionImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, delta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Um índice de gerador a ser representado como uma evolução unitário na base Pauli.


### <a name="delta--double"></a>Delta: [duplo](xref:microsoft.quantum.lang-ref.double)

Um multiplicador na duração da evolução do tempo pelo termo referenciado em `generatorIndex` .


### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registre-se sob o operador de evolução do tempo.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

