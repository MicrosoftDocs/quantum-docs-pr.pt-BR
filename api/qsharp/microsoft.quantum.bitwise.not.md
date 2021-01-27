---
uid: Microsoft.Quantum.Bitwise.Not
title: Não função
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Not
qsharp.summary: Returns the bitwise NOT of an integer. This performs the same computation as the built-in `~~~` operator.
ms.openlocfilehash: 9c7642770c4f1db4878ccc1aba288fb9254e017e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842110"
---
# <a name="not-function"></a>Não função

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna a não-bit que não é um inteiro.
Isso executa a mesma computação que o `~~~` operador interno.

```qsharp
function Not (a : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>Exemplo

```qsharp
let a = 248;
let x = Not(a); // x : Int = -249, due to two's complement representation.
```

## <a name="remarks"></a>Comentários

Consulte o [operador C# ~](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/bitwise-complement-operator) para obter mais detalhes.