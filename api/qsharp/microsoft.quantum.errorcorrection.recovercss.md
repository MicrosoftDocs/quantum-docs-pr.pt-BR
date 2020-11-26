---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Operação RecoverCSS
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: eb01b1b9fccc19f0e3f1fd5ee596b95d0d61563f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200536"
---
# <a name="recovercss-operation"></a>Operação RecoverCSS

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa uma única rodada de correção de erro por um código Quantum descrito por um `CSS` tipo.

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>Entrada

### <a name="code--css"></a>código: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

Um código baseado em CSS de Quantum-corrigindo o pacote de códigos como um `CSS` tipo descreve a codificação e decodificação de dados Quantum e como os síndromes de erro devem ser medidos.


### <a name="fnx--recoveryfn"></a>fnX: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Um `RecoveryFn` que mapeia cada síndrome $X $ Error para as `Pauli[]` operações que corrigem o erro detectado.


### <a name="fnz--recoveryfn"></a>fnZ: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Um `RecoveryFn` que mapeia cada síndrome $Z $ Error para as `Pauli[]` operações que corrigem o erro detectado.


### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Uma matriz de qubits onde o código de estabilizador é definido.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [Microsoft. Quantum. ErrorCorrection. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Microsoft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)