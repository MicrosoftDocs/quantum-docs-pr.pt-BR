---
uid: Microsoft.Quantum.Math.ModulusL
title: Função de módulo
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: e7e692059051fde295634c37892ec54e2cf1b095
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697037"
---
# <a name="modulusl-function"></a>Função de módulo

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Agrupa [](https://nuget.org/packages/)


Computa o residue canônico do `value` módulo `modulus` .

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a>Entrada

### <a name="value--bigint"></a>valor: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O valor do qual residue é computado


### <a name="modulus--bigint"></a>módulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)

O módulo pelo qual residues são tomadas, deve ser positivo



## <a name="output--bigint"></a>Saída: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Integer $r $ entre 0 e `modulus - 1` isso `value - r` é divisível por módulo

## <a name="remarks"></a>Comentários

Essa função se comporta de forma diferente de como o operador `%` se comporta em C# e Q # como no resultado é sempre um inteiro positivo entre 0 e `modulus - 1` , mesmo se o valor for negativo.