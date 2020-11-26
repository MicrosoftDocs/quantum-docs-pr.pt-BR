---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Operação EncodeIntoFiveQubitCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 70e52b7440dca1fa8761db13d6187cb6bf8c43c4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200978"
---
# <a name="encodeintofivequbitcode-operation"></a>Operação EncodeIntoFiveQubitCode

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Codifica no código Quantum ⟦ 5, 1, 3 ⟧.

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Entrada

### <a name="physregister--qubit"></a>physRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um qubit que representa um estado não codificado. Esta matriz `Qubit[]` tem comprimento 1.


### <a name="auxqubits--qubit"></a>auxQubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro de qubits auxiliares que será usado para representar o estado codificado.



## <a name="output--logicalregister"></a>Saída: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Uma matriz de qubits físico do tipo `LogicalRegister` que armazena o estado codificado.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)