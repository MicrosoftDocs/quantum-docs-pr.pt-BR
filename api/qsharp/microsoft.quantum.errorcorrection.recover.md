---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Operação de recuperação
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: bdf09decc3705d3285f4eb605c176d7764a994d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200570"
---
# <a name="recover-operation"></a>Operação de recuperação

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa uma única rodada de correção de erro por um código Quantum descrito por um `QECC` tipo.

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>Entrada

### <a name="code--qecc"></a>código: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)

Um código Quantum-corrigindo códigos empacotados como um `QECC` tipo descreve a codificação e a decodificação de dados Quantum e como os síndromes de erro devem ser medidos.


### <a name="fn--recoveryfn"></a>FN: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Um `RecoveryFn` que mapeia cada síndrome de erro para as `Pauli[]` operações que corrigem o erro detectado.


### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Uma matriz de qubits onde o código de estabilizador é definido.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [Microsoft. Quantum. ErrorCorrection. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Microsoft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)