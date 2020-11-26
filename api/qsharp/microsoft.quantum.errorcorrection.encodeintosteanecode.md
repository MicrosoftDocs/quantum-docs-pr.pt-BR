---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: Operação EncodeIntoSteaneCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: e74c7fdc5acbb1a8c417bad3eb3630314e3f71bc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201011"
---
# <a name="encodeintosteanecode-operation"></a>Operação EncodeIntoSteaneCode

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Uma operação de codificação que mapeia um registro Quantum não codificado para um registro Quantum codificado sob o código Quantum ⟦ 7, 1, 3 ⟧ Steane.

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Entrada

### <a name="physregister--qubit"></a>physRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro qubit que contém um estado Quantum não codificado


### <a name="auxqubits--qubit"></a>auxQubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro qubit que é inicialmente zero e que é adicionado ao sistema Quantum para que uma operação de codificação possa ser executada



## <a name="output--logicalregister"></a>Saída: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Um registro Quantum que mantém o estado depois que o codificador Steane tiver sido aplicado

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. ErrorCorrection. SteaneCodeDecoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)