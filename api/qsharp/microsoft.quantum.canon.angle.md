---
uid: Microsoft.Quantum.Canon.Angle
title: Função Angle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 0528f21b2d9c98b6497e28741964e6497d4d0fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842046"
---
# <a name="angle-function"></a>Função Angle

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retornará 1, se `index` tiver um número ímpar de 1s e-1, se `index` tiver um número par de 1s.

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a>Descrição

O valor corresponde ao sinal do coeficiente do Rademacher-Walsh espectro da variável n e da função para uma determinada Atribuição que decide o ângulo da rotação.

## <a name="input"></a>Entrada

### <a name="index--int"></a>índice: [int](xref:microsoft.quantum.lang-ref.int)

Atribuição de entrada como um inteiro (de 0 a 2 ^ n-1)



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

