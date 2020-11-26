---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: Função NotNearlyEqualD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: 23229b1630982eba4485330cc2290aed733c4d86
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197136"
---
# <a name="notnearlyequald-function"></a>Função NotNearlyEqualD

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna true se e somente se duas entradas não forem quase iguais (ou seja, não estiverem dentro de uma tolerância de 1e-12).

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--double"></a>r: [duplo](xref:microsoft.quantum.lang-ref.double)

O primeiro valor a ser comparado.


### <a name="b--double"></a>b: [duplo](xref:microsoft.quantum.lang-ref.double)

O segundo valor a ser comparado.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se `a` não for quase igual a `b` .

## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```