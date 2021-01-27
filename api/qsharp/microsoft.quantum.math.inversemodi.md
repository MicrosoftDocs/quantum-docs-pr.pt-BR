---
uid: Microsoft.Quantum.Math.InverseModI
title: Função InverseModI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 474146e644bcd042e85b917bc43135a674bedce1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846880"
---
# <a name="inversemodi-function"></a>Função InverseModI

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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