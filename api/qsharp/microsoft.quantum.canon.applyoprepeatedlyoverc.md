---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverC
title: Operação ApplyOpRepeatedlyOverC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverC
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 08c3af3a4877481833973061aa4d54c2b29304c9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218250"
---
# <a name="applyoprepeatedlyoverc-operation"></a>Operação ApplyOpRepeatedlyOverC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica o mesmo op em um registro qubit várias vezes.

```qsharp
operation ApplyOpRepeatedlyOverC (op : (Qubit[] => Unit is Ctl), targets : Int[][], register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Entrada

### <a name="op--qubit--unit--is-ctl"></a>op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

Uma operação a ser aplicada várias vezes no registro qubit


### <a name="targets--int"></a>destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []

Matrizes aninhadas que descrevem os destinos da operação. Cada matriz deve conter uma lista de ints que descreve o qubits a ser usado.


### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit registrar-se para ser tratado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplySeriesOfOps](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)