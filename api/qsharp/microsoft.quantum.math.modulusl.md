---
uid: Microsoft.Quantum.Math.ModulusL
title: Função de módulo
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6be2edb052cf55f8e8465c76b5dcadeb61ff11ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842737"
---
# <a name="modulusl-function"></a>Função de módulo

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

Essa função se comporta de forma diferente de como o operador `%` se comporta em C# e Q # como no resultado é sempre um inteiro não negativo entre 0 e `modulus - 1` , mesmo se o valor for negativo.