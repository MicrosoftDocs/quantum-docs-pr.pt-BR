---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Tipo definido pelo usuário ReflectionOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 7bb0626e7cca9ae0b640699ea57f2e114bda2d06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226648"
---
# <a name="reflectionoracle-user-defined-type"></a>Tipo definido pelo usuário ReflectionOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa uma reflexão do Oracle.

Uma reflexão do Oracle, $O $, tem entradas:

- A fase $ \phi $ pela qual girar o subespaço refletido.
- O qubit se registra no qual executar a reflexão determinada.

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Itens nomeados

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a>ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL



## <a name="remarks"></a>Comentários

Este Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ executa uma reflexão parcial por uma fase $ \phi $ sobre um único estado puro $ \ket{\psi} $.