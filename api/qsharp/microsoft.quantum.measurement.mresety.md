---
uid: Microsoft.Quantum.Measurement.MResetY
title: Operação MResetY
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 48aba7317d0e48d089ec6c4814efdee51bb8e2ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697024"
---
# <a name="mresety-operation"></a>Operação MResetY

Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)

Agrupa [](https://nuget.org/packages/)


Mede um único qubit na base Y e o redefine para um estado inicial fixo após a medição.

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a>Descrição

Executa uma medida de qubit único no $Y $-base e garante que o qubit seja retornado para $ \ket {0} $ após a medição.

## <a name="input"></a>Entrada

### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um único qubit a ser medido.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

O resultado da medição `target` na base Pauli $Y $.