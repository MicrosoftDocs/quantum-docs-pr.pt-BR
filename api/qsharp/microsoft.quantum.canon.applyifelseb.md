---
uid: Microsoft.Quantum.Canon.ApplyIfElseB
title: Operação ApplyIfElseB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseB
qsharp.summary: Applies one of two operations, depending on the value of a classical bit.
ms.openlocfilehash: 68c06a5141b9ff423c2d18adc3a9e162eed939f6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694301"
---
# <a name="applyifelseb-operation"></a>Operação ApplyIfElseB

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Aplica uma das duas operações, dependendo do valor de um bit clássico.

```qsharp
operation ApplyIfElseB<'T, 'U> (bit : Bool, (trueOp : ('T => Unit), trueInput : 'T), (falseOp : ('U => Unit), falseInput : 'U)) : Unit
```


## <a name="description"></a>Descrição

Dado um pouco `bit` , o aplica a operação `trueOp` com `trueInput` como sua entrada quando `bit` está `true` e se aplica `falseOp(falseInput)` quando `bit` é `false` .

## <a name="input"></a>Entrada

### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

O valor booliano usado para determinar se `trueOp` ou `falseOp` é aplicado.


### <a name="trueop--t--unit"></a>trueOp: t = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

A operação a ser aplicada quando `bit` é `true` .


### <a name="trueinput--t"></a>trueInput: ' t

A entrada a ser fornecida para `trueOp` quando `bit` é `true` .


### <a name="falseop--u--unit"></a>falseOp: ' U = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

A operação a ser aplicada quando `bit` é `false` .


### <a name="falseinput--u"></a>falseInput: ' U

A entrada a ser fornecida para `falseOp` quando `bit` é `false` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação `trueOp` a ser aplicada condicionalmente.
### <a name="u"></a>' U

O tipo de entrada da operação `falseOp` a ser aplicada condicionalmente.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyIfZero](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Microsoft. Quantum. Canon. ApplyIfOne](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Microsoft. Quantum. Canon. ApplyIfElseRC](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Microsoft. Quantum. Canon. ApplyIfElseRA](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Microsoft. Quantum. Canon. ApplyIfElseRCA](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)