---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Tipo definido pelo usuário SyndromeMeasOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 1314e16d26c7310bab21caa91cb398d4b6f09b29
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693429"
---
# <a name="syndromemeasop-user-defined-type"></a>Tipo definido pelo usuário SyndromeMeasOp

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Agrupa [](https://nuget.org/packages/)


Representa uma operação que é usada para medir a síndrome de um bloco de código com correção de erros.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a>Comentários

A assinatura `(LogicalRegister => Syndrome)` representa uma operação que atua em conjunto no qubits em `LogicalRegister` e em algumas qubits auxiliares seguidos por uma medida do qubits auxiliar para extrair um `Syndrome` valor que representa a `Result[]` dessas medições.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. ErrorCorrection. síndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)