---
uid: Microsoft.Quantum.Math.ExpModL
title: Função ExpModL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696841"
---
# <a name="expmodl-function"></a>Função ExpModL

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Agrupa [](https://nuget.org/packages/)


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