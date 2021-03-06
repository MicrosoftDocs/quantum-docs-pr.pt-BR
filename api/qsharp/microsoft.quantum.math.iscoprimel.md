---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Função IsCoprimeL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: a48f056d138499607d32b38b1fa0970745732c41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851340"
---
# <a name="iscoprimel-function"></a>Função IsCoprimeL

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retornará true se $a $ e $b $ forem coprimos e false caso contrário.

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Entrada

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

o primeiro número de que coprimality está sendo testado


### <a name="b--bigint"></a>b: [bigint](xref:microsoft.quantum.lang-ref.bigint)

o segundo número do qual coprimality está sendo testado



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

True, se $a $ e $b $ forem coprimos (por exemplo, seu maior divisor comum é 1) e false caso contrário