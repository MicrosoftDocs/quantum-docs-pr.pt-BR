---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseIntrinsicCA
title: Operação ApplyIfElseIntrinsicCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: 6ba83f7344c77b95f2e7397cd42f39884556547a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855689"
---
# <a name="applyifelseintrinsicca-operation"></a>Operação ApplyIfElseIntrinsicCA

Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyIfElseIntrinsicCA (measurementResult : Result, onResultZeroOp : (Unit => Unit is Ctl + Adj), onResultOneOp : (Unit => Unit is Ctl + Adj)) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="measurementresult--__invalidresult__"></a>measurementResult: __inválido <Result>__




### <a name="onresultzeroop--unit--unit--is-adj--ctl"></a>onResultZeroOp: unidade de [unidade](xref:microsoft.quantum.lang-ref.unit) => [](xref:microsoft.quantum.lang-ref.unit) é adj + CTL




### <a name="onresultoneop--unit--unit--is-adj--ctl"></a>onResultOneOp: unidade de [unidade](xref:microsoft.quantum.lang-ref.unit) => [](xref:microsoft.quantum.lang-ref.unit) é adj + CTL





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

