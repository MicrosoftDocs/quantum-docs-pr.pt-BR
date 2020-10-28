---
uid: Microsoft.Quantum.Math.ExpModI
title: Função ExpModI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: e31273702a9850d0162f160ca412ff6d50f38b28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696789"
---
# <a name="expmodi-function"></a>Função ExpModI

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Agrupa [](https://nuget.org/packages/)


Retorna um número inteiro elevado a uma determinada potência, com relação a um determinado módulo.

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a>Descrição

Deixe-nos indicar expBase por $x $, Power by $p $ e módulo por $N $.
A função retorna $x ^ p \operatorname{mod} N $.

Supomos que $N $, $x $ são positivos e a energia não é negativa.

## <a name="input"></a>Entrada

### <a name="expbase--int"></a>expBase: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="power--int"></a>potência: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="modulus--int"></a>módulo: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="remarks"></a>Comentários

Leva tempo proporcional ao número de bits em `power` , e não ao `power` próprio.