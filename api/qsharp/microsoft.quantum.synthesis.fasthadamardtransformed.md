---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Função FastHadamardTransformed
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: be54413ef2d3fdaf7ddc726bc0906adb4ec382ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855462"
---
# <a name="fasthadamardtransformed-function"></a>Função FastHadamardTransformed

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Computa a transformação Hadamard de uma função booliana na {-1,1} codificação usando o método de Yates

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a>Entrada

### <a name="func--int"></a>Func: [int](xref:microsoft.quantum.lang-ref.int)[]

Tabela verdadeira em {-1,1} codificação



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)[]

Coeficientes Spectral da função

## <a name="example"></a>Exemplo

```qsharp
FastHadamardTransformed([1, 1, 1, -1]); // [2, 2, 2, -2]
```