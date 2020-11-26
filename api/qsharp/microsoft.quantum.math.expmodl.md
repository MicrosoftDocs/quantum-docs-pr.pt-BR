---
uid: Microsoft.Quantum.Math.ExpModL
title: Função ExpModL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 07da113caeb9f6f3f3f3f92f13478f33021bfa14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210736"
---
# <a name="expmodl-function"></a>Função ExpModL

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna um número inteiro elevado a uma determinada potência, com relação a um determinado módulo.

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a>Descrição

Deixe-nos indicar expBase por $x $, Power by $p $ e módulo por $N $.
A função retorna $x ^ p \operatorname{mod} N $.

Supomos que $N $, $x $ são positivos e a energia não é negativa.

## <a name="input"></a>Entrada

### <a name="expbase--bigint"></a>expBase: [bigint](xref:microsoft.quantum.lang-ref.bigint)




### <a name="power--bigint"></a>potência: [bigint](xref:microsoft.quantum.lang-ref.bigint)




### <a name="modulus--bigint"></a>módulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigint"></a>Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)



## <a name="remarks"></a>Comentários

Leva tempo proporcional ao número de bits em `power` , e não ao `power` próprio.