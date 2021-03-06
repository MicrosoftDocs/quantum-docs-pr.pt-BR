---
uid: Microsoft.Quantum.Math.BitSizeI
title: Função BitSizeI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7edf37a81571dfa1d4cb755493e1863a44c694e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857692"
---
# <a name="bitsizei-function"></a>Função BitSizeI

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Para um inteiro não negativo `a` , retorna o número de bits necessários para representar `a` .

Ou seja, retorna o menor $n $, que $a < 2 ^ n $.

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

O inteiro cujo tamanho de bit deve ser calculado.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

O tamanho de bit de `a` .