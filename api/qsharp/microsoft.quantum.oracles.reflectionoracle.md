---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Tipo definido pelo usuário ReflectionOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 1ef07126596b70d2c5574430656009116c34d2bc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854484"
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