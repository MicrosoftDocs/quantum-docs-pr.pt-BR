---
uid: Microsoft.Quantum.Logical.LessThanD
title: Função LessThanD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 40f059e49affbb1b5af7dc349f6ee53dfb357873
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197731"
---
# <a name="lessthand-function"></a>Função LessThanD

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna true se e somente se um número for menor que outro número.

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--double"></a>r: [duplo](xref:microsoft.quantum.lang-ref.double)

O primeiro valor a ser comparado.


### <a name="b--double"></a>b: [duplo](xref:microsoft.quantum.lang-ref.double)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` for estritamente menor que `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let cond = a < b;
let cond = LessThanD(a, b);
```