---
uid: Microsoft.Quantum.Convert.BoolArrayAsBigInt
title: Função BoolArrayAsBigInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsBigInt
qsharp.summary: Converts a given array of Booleans to an equivalent big integer. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 75656ba188a1b822eb42e98412365bf5873bf46e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693643"
---
# <a name="boolarrayasbigint-function"></a>Função BoolArrayAsBigInt

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Agrupa [](https://nuget.org/packages/)


Converte uma determinada matriz de boolianos em um inteiro grande equivalente.
O elemento 0 da matriz é o bit menos significativo do inteiro grande.

```qsharp
function BoolArrayAsBigInt (a : Bool[]) : BigInt
```


## <a name="input"></a>Entrada

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)[]





## <a name="output--bigint"></a>Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)



## <a name="remarks"></a>Comentários

Consulte o [Construtor C# BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) para obter mais detalhes.