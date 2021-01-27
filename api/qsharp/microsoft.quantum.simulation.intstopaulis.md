---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Função IntsToPaulis
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 6904054bb1aff3a57c80882694b4c217812b2b81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842232"
---
# <a name="intstopaulis-function"></a>Função IntsToPaulis

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converte uma matriz de inteiros em uma matriz de operadores de Pauli de qubit único.

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a>Entrada

### <a name="ints--int"></a>ints: [int](xref:microsoft.quantum.lang-ref.int)[]

Matriz de inteiros no intervalo `0..3`  a ser convertido em operadores Pauli.



## <a name="output--pauli"></a>Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Uma matriz `paulis` de operadores Pauli `Pauli[]` tem o mesmo comprimento `ints` que isso `paulis[idxPauli]` é igual ao elemento de `[PauliI, PauliX, PauliY, PauliZ]` fornecido por `ints[idxPauli]` .