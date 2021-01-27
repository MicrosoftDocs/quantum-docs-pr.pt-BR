---
uid: Microsoft.Quantum.Bitwise.And
title: Função and
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: And
qsharp.summary: Returns the bitwise AND of two integers. This performs the same computation as the built-in `&&&` operator.
ms.openlocfilehash: 56eae4ef222a6593fd97966a9af21d559f613bc3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842158"
---
# <a name="and-function"></a>Função and

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna o bit e de dois inteiros.
Isso executa a mesma computação que o `&&&` operador interno.

```qsharp
function And (a : Int, b : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>Exemplo

```qsharp
let a = 248;       //                11111000₂
let b = 63;        //                00111111₂
let x = And(a, b); // x : Int = 56 = 00111000₂.
```

## <a name="remarks"></a>Comentários

Consulte o [ &amp; operador C#](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/and-operator) (Binary) para obter mais detalhes.