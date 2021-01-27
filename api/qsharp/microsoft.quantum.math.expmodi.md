---
uid: Microsoft.Quantum.Math.ExpModI
title: Função ExpModI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: dd4fc7d98275f6a02e3b13163b92f0812c92a82f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857043"
---
# <a name="expmodi-function"></a>Função ExpModI

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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