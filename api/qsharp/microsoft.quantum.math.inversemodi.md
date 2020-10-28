---
uid: Microsoft.Quantum.Math.InverseModI
title: Função InverseModI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 6efc9da5f5ebb64065a90e749daa629dc2dce9cf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696828"
---
# <a name="inversemodi-function"></a>Função InverseModI

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Agrupa [](https://nuget.org/packages/)


Retorna $b $, que $a \cdot b = 1 (\operatorname{mod} \texttt{Modulus}) $.

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

O número que está sendo invertido


### <a name="modulus--int"></a>módulo: [int](xref:microsoft.quantum.lang-ref.int)

O módulo de acordo com o qual os números são invertidos



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Inteiro $b $, que $a \cdot b = 1 (\operatorname{mod} \texttt{Modulus}) $.