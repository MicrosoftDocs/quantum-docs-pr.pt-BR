---
uid: Microsoft.Quantum.Canon.ApplyIfElseBCA
title: Operação ApplyIfElseBCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical bit.
ms.openlocfilehash: 3ed9d7cbf277f4c3acd0e6c3b5f920c3e140855d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844966"
---
# <a name="applyifelsebca-operation"></a>Operação ApplyIfElseBCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma das duas operações de unitário, dependendo do valor de um bit clássico.

```qsharp
operation ApplyIfElseBCA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj + Ctl), trueInput : 'T), (falseOp : ('U => Unit is Adj + Ctl), falseInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Dado um pouco `bit` , o aplica a operação `trueOp` com `trueInput` como sua entrada quando `bit` está `true` e se aplica `falseOp(falseInput)` quando `bit` é `false` .

## <a name="input"></a>Entrada

### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

O valor booliano usado para determinar se `trueOp` ou `falseOp` é aplicado.


### <a name="trueop--t--unit--is-adj--ctl"></a>trueOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

A operação unitário a ser aplicada quando `bit` é `true` .


### <a name="trueinput--t"></a>trueInput: ' t

A entrada a ser fornecida para `trueOp` quando `bit` é `true` .


### <a name="falseop--u--unit--is-adj--ctl"></a>falseOp: ' U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

A operação unitário a ser aplicada quando `bit` é `false` .


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