---
uid: Microsoft.Quantum.Canon.ApplyAndChain
title: Operação ApplyAndChain
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAndChain
qsharp.summary: Computes a chain of AND gates
ms.openlocfilehash: c53bca6ecf964f4358b0a7ff1c61d4e8e195cd7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219355"
---
# <a name="applyandchain-operation"></a>Operação ApplyAndChain

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Computa uma cadeia de e Gates

```qsharp
operation ApplyAndChain (auxRegister : Qubit[], ctrlRegister : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="description"></a>Descrição

O qubits auxiliar para computar resultados temporários deve ser especificado explicitamente.
O comprimento desse registro é `Length(ctrlRegister) - 2` , se houver pelo menos dois controles, caso contrário, o comprimento será 0.

## <a name="input"></a>Entrada

### <a name="auxregister--qubit"></a>auxRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="ctrlregister--qubit"></a>ctrlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

