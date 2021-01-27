---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: Operação ApplyUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859122"
---
# <a name="applyunitary-operation"></a>Operação ApplyUnitary

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica o portão definido por 2 ^ n x 2 ^ n matriz unitário.

Falha se a matriz não for unitário ou tiver tamanho incorreto.

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="unitary--complex"></a>unitário: [complexo](xref:Microsoft.Quantum.Math.Complex)[] []

2 ^ n x 2 ^ n matriz unitário que descreve a operação.
Se matriz não for um tamanho unitário ou não for adequado, o lançará uma exceção.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Qubits ao qual aplicar o registro de operação de comprimento n.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

