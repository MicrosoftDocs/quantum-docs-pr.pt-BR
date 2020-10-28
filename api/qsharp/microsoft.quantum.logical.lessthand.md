---
uid: Microsoft.Quantum.Logical.LessThanD
title: Função LessThanD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 8cd274d5e299df2f556006baf7457d54aebcd071
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696807"
---
# <a name="lessthand-function"></a>Função LessThanD

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Agrupa [](https://nuget.org/packages/)


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