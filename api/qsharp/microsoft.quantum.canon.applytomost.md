---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Operação ApplyToMost
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a3918233e101f3d8956601dcc7d85edcf6196ac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850601"
---
# <a name="applytomost-operation"></a>Operação ApplyToMost

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação a todos, exceto ao último elemento de uma matriz.

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a>Descrição

Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Most(targets))` .

## <a name="input"></a>Entrada

### <a name="op--t--unit"></a>op: ' t [] = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Uma operação a ser aplicada.


### <a name="targets--t"></a>destinos: ' t []

Uma matriz de destinos, das quais todos, exceto o último, será aplicado `op` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser aplicada.

## <a name="example"></a>Exemplo

Os seguintes trechos de código Q # são equivalentes:

```qsharp
ApplyToMost(ApplyCNOTChain, register);
ApplyCNOTChain(Most(register));
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToMostA](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [Microsoft. Quantum. Canon. ApplyToMostC](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [Microsoft. Quantum. Canon. ApplyToMostCA](xref:Microsoft.Quantum.Canon.ApplyToMostCA)