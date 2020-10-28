---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: Operação ApplyIfElseBC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: 032d92484dc96481cb981d9d8acfeed248a9116d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694300"
---
# <a name="applyifelsebc-operation"></a>Operação ApplyIfElseBC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Aplica uma das duas operações controláveis, dependendo do valor de um bit clássico.

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit
```


## <a name="description"></a>Descrição

Dado um pouco `bit` , o aplica a operação `trueOp` com `trueInput` como sua entrada quando `bit` está `true` e se aplica `falseOp(falseInput)` quando `bit` é `false` .

## <a name="input"></a>Entrada

### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

O valor booliano usado para determinar se `trueOp` ou `falseOp` é aplicado.


### <a name="trueop--t--unit-ctl"></a>trueOp: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

A operação controláveis a ser aplicada quando `bit` é `true` .


### <a name="trueinput--t"></a>trueInput: ' t

A entrada a ser fornecida para `trueOp` quando `bit` é `true` .


### <a name="falseop--u--unit-ctl"></a>falseOp: ' U => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)

A operação controláveis a ser aplicada quando `bit` é `false` .


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