---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroC
title: Operação ApplyIfZeroC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroC
qsharp.summary: ''
ms.openlocfilehash: 6de4fcf86495136f2caec6fb6f873a18d751c977
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697121"
---
# <a name="applyifzeroc-operation"></a>Operação ApplyIfZeroC

Namespace: [Microsoft. Quantum. Simulation. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

Agrupa [](https://nuget.org/packages/)




```qsharp
operation ApplyIfZeroC<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T)) : Unit
```


## <a name="input"></a>Entrada

### <a name="measurementresult--__invalidresult__"></a>measurementResult: __inválido <Result>__




### <a name="onresultzeroop--t--unit-ctl"></a>onResultZeroOp: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)




### <a name="zeroarg--t"></a>zeroArg: ' t





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

