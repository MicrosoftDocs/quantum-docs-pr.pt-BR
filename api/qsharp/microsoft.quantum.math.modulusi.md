---
uid: Microsoft.Quantum.Math.ModulusI
title: Função de móduloi
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 7bad044db9e2229c85cb3909dc4802bceaee6382
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847302"
---
# <a name="modulusi-function"></a>Função de móduloi

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Computa o residue canônico do `value` módulo `modulus` .

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="value--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

O valor do qual residue é computado


### <a name="modulus--int"></a>módulo: [int](xref:microsoft.quantum.lang-ref.int)

O módulo pelo qual residues são tomadas, deve ser positivo



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Integer $r $ entre 0 e `modulus - 1` isso `value - r` é divisível por módulo

## <a name="remarks"></a>Comentários

Essa função se comporta de forma diferente de como o operador `%` se comporta em C# e Q # como no resultado é sempre um inteiro não negativo entre 0 e `modulus - 1` , mesmo se o valor for negativo.