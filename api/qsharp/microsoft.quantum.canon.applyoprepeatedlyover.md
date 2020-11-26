---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver
title: Operação ApplyOpRepeatedlyOver
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOver
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 343392d5a6af07cdc45fd8bab6656d59a6f2b350
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218301"
---
# <a name="applyoprepeatedlyover-operation"></a>Operação ApplyOpRepeatedlyOver

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica o mesmo op em um registro qubit várias vezes.

```qsharp
operation ApplyOpRepeatedlyOver (op : (Qubit[] => Unit), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="op--qubit--unit"></a>op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Uma operação a ser aplicada várias vezes no registro qubit


### <a name="targets--int"></a>destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []

Matrizes aninhadas que descrevem os destinos da operação. Cada matriz deve conter uma lista de ints que descreve o qubits a ser usado.


### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit registrar-se para ser tratado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplySeriesOfOps](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)