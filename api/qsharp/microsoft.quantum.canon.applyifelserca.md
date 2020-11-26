---
uid: Microsoft.Quantum.Canon.ApplyIfElseRCA
title: Operação ApplyIfElseRCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical result.
ms.openlocfilehash: dfd1c16a25a2da507024813a380386c8f4e49d30
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218743"
---
# <a name="applyifelserca-operation"></a>Operação ApplyIfElseRCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma das duas operações de unitário, dependendo do valor de um resultado clássico.

```qsharp
operation ApplyIfElseRCA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj + Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Adj + Ctl), oneInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Dado um resultado `result` , o aplica a operação `zeroOp` com `zeroInput` como sua entrada quando `result` é igual a `Zero` e se aplica `oneOp(oneInput)` quando `result == One` .

## <a name="input"></a>Entrada

### <a name="result--__invalidresult__"></a>resultado: __inválido <Result>__

O resultado da medida usado para determinar se `zeroOp` ou `oneOp` é aplicado.


### <a name="zeroop--t--unit--is-adj--ctl"></a>zeroOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL

A operação unitário a ser aplicada quando `result == Zero` .


### <a name="zeroinput--t"></a>zeroInput: ' t

A entrada a ser fornecida a `zeroOp` quando `result == Zero` .


### <a name="oneop--u--unit--is-adj--ctl"></a>oneOp: ' U => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

A operação unitário a ser aplicada quando `result == One` .


### <a name="oneinput--u"></a>oneInput: ' U

A entrada a ser fornecida a `oneOp` quando `result == One` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação `zeroOp` a ser aplicada condicionalmente.
### <a name="u"></a>' U

O tipo de entrada da operação `oneOp` a ser aplicada condicionalmente.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyIfZero](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Microsoft. Quantum. Canon. ApplyIfOne](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Microsoft. Quantum. Canon. ApplyIfElseRC](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Microsoft. Quantum. Canon. ApplyIfElseRA](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Microsoft. Quantum. Canon. ApplyIfElseRCA](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)