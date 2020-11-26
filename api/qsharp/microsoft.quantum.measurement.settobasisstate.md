---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Operação SetToBasisState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: 2612bfe488c830abd835be89b2f8ea6795abf675
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194144"
---
# <a name="settobasisstate-operation"></a>Operação SetToBasisState

Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Define um qubit para um determinado estado de base computacional medindo o qubit e aplicando uma inversão de bit, se necessário.

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a>Entrada

### <a name="desired--__invalidresult__"></a>desejado: __inválido <Result>__

O estado base ao qual o qubit deve ser definido.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

O qubit cujo estado deve ser definido.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Como uma constante desta operação, chamar `M(q)` imediatamente após `SetToBasisState(result, q)` será retornado `result` .