---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Operação AllowAtMostNQubits
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 5376b6f39d12d664342fbf71e67442c6ef8a0827
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202542"
---
# <a name="allowatmostnqubits-operation"></a>Operação AllowAtMostNQubits

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Entre uma chamada para essa operação e seu adjacente, o declara que, no máximo, um determinado número de qubits adicionais são alocados com instruções using.

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a>Entrada

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número máximo de qubits que podem ser alocadas.


### <a name="message--string"></a>mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Uma mensagem a ser exibida após a falha.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Esta operação pode ser substituída por um não op em destinos que não dão suporte a ela.