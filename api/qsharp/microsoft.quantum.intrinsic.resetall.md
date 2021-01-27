---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: Operação ResetAll
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: 2b8e7fc0e7881d8c1bd6f14c150476262b7a2b19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849313"
---
# <a name="resetall-operation"></a>Operação ResetAll

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Dada uma matriz de qubits, meça-os e verifique se estão no estado | 0 ⟩, de modo que eles possam ser liberados com segurança.

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Uma matriz de qubits cujos Estados devem ser redefinidos para $ \ket {0} $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

