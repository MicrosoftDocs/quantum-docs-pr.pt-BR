---
uid: Microsoft.Quantum.Canon.ApplyIfElseBA
title: Operação ApplyIfElseBA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical bit.
ms.openlocfilehash: a85567a49df1f261b95f3553da8dc789ce924e7a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844976"
---
# <a name="applyifelseba-operation"></a>Operação ApplyIfElseBA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma das duas operações de adjointable, dependendo do valor de um bit clássico.

```qsharp
operation ApplyIfElseBA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj), trueInput : 'T), (falseOp : ('U => Unit is Adj), falseInput : 'U)) : Unit is Adj
```


## <a name="description"></a>Descrição

Dado um pouco `bit` , o aplica a operação `trueOp` com `trueInput` como sua entrada quando `bit` está `true` e se aplica `falseOp(falseInput)` quando `bit` é `false` .

## <a name="input"></a>Entrada

### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

O valor booliano usado para determinar se `trueOp` ou `falseOp` é aplicado.


### <a name="trueop--t--unit--is-adj"></a>trueOp: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

A operação de adjointable a ser aplicada quando `bit` é `true` .


### <a name="trueinput--t"></a>trueInput: ' t

A entrada a ser fornecida para `trueOp` quando `bit` é `true` .


### <a name="falseop--u--unit--is-adj"></a>falseOp: ' U = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

A operação de adjointable a ser aplicada quando `bit` é `false` .


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