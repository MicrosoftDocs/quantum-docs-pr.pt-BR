---
uid: Microsoft.Quantum.Canon.ApplyIfElseR
title: Operação ApplyIfElseR
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseR
qsharp.summary: Applies one of two operations, depending on the value of a classical result.
ms.openlocfilehash: 0d7cc9f67f9dd0c69a9256f007a3aeab3e457907
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841807"
---
# <a name="applyifelser-operation"></a>Operação ApplyIfElseR

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma das duas operações, dependendo do valor de um resultado clássico.

```qsharp
operation ApplyIfElseR<'T, 'U> (result : Result, (zeroOp : ('T => Unit), zeroInput : 'T), (oneOp : ('U => Unit), oneInput : 'U)) : Unit
```


## <a name="description"></a>Descrição

Dado um resultado `result` , o aplica a operação `zeroOp` com `zeroInput` como sua entrada quando `result` é igual a `Zero` e se aplica `oneOp(oneInput)` quando `result == One` .

## <a name="input"></a>Entrada

### <a name="result--__invalidresult__"></a>resultado: __inválido <Result>__

O resultado da medida usado para determinar se `zeroOp` ou `oneOp` é aplicado.


### <a name="zeroop--t--unit"></a>zeroOp: t = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

A operação a ser aplicada quando `result == Zero` .


### <a name="zeroinput--t"></a>zeroInput: ' t

A entrada a ser fornecida a `zeroOp` quando `result == Zero` .


### <a name="oneop--u--unit"></a>oneOp: ' U = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

A operação a ser aplicada quando `result == One` .


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