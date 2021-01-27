---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Redefinir operação
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: b4275796b966bfe7f55271f4e92866410a14e830
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818639"
---
# <a name="reset-operation"></a>Redefinir operação

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Considerando um único qubit, o mede e garante que ele esteja no estado | 0 ⟩, de modo que ele possa ser liberado com segurança.

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a>Entrada

### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

O qubit cujo estado deve ser redefinido para $ \ket {0} $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

