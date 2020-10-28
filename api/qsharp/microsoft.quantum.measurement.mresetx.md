---
uid: Microsoft.Quantum.Measurement.MResetX
title: Operação MResetX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: a16d7405388b560edcdb6c36b6668791f7ba1398
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697023"
---
# <a name="mresetx-operation"></a>Operação MResetX

Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)

Agrupa [](https://nuget.org/packages/)


Mede um único qubit na base X e o redefine para um estado inicial fixo após a medição.

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a>Descrição

Executa uma medida de qubit único no $X $-base e garante que o qubit seja retornado para $ \ket {0} $ após a medição.

## <a name="input"></a>Entrada

### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um único qubit a ser medido.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

O resultado da medição `target` na base Pauli $X $.