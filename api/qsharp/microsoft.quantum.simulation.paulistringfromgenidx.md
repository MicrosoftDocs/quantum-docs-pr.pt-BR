---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Função PauliStringFromGenIdx
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: a937dc648c5de5a5f6de7da996448af497b92185
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230303"
---
# <a name="paulistringfromgenidx-function"></a>Função PauliStringFromGenIdx

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Extrai a cadeia de caracteres Pauli e seus índices qubit de um termo Pauli descrito por um `GeneratorIndex` .

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a>Entrada

### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` tipo que codifica um termo de Pauli.



## <a name="output--pauliint"></a>Saída: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])

A cadeia de caracteres Pauli do termo descrito por um `GeneratorIndex` e os índices para o qubits em que ele atua.