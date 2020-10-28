---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Tipo definido pelo usuário ReflectionOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 8e35e7e508ea7e0c30ea2a70633f71a6c87d4be1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696910"
---
# <a name="reflectionoracle-user-defined-type"></a>Tipo definido pelo usuário ReflectionOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Agrupa [](https://nuget.org/packages/)


Representa uma reflexão do Oracle.

Uma reflexão do Oracle, $O $, tem entradas:

- A fase $ \phi $ pela qual girar o subespaço refletido.
- O qubit se registra no qual executar a reflexão determinada.

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Itens nomeados

### <a name="applyreflection--doublequbit--unit-adj--ctl"></a>ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL



## <a name="remarks"></a>Comentários

Este Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ executa uma reflexão parcial por uma fase $ \phi $ sobre um único estado puro $ \ket{\psi} $.