---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Tipo definido pelo usuário SyndromeMeasOp
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 65e47d82546b1df0beec2c00f435d3e7a28e6ae6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200247"
---
# <a name="syndromemeasop-user-defined-type"></a>Tipo definido pelo usuário SyndromeMeasOp

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa uma operação que é usada para medir a síndrome de um bloco de código com correção de erros.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a>Comentários

A assinatura `(LogicalRegister => Syndrome)` representa uma operação que atua em conjunto no qubits em `LogicalRegister` e em algumas qubits auxiliares seguidos por uma medida do qubits auxiliar para extrair um `Syndrome` valor que representa a `Result[]` dessas medições.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. ErrorCorrection. síndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)