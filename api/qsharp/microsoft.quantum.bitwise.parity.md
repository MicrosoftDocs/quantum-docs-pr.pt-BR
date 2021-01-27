---
uid: Microsoft.Quantum.Bitwise.Parity
title: Função de paridade
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Parity
qsharp.summary: Returns the bitwise PARITY of an integer (1 if its binary representation contains odd number of ones and 0 otherwise).
ms.openlocfilehash: b34ef36b0336ec1dea7fdbd878c6d695b38d623e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842124"
---
# <a name="parity-function"></a>Função de paridade

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna a paridade de um número inteiro de bits (1 se sua representação binária contiver um número ímpar de uns e 0 caso contrário).

```qsharp
function Parity (a : Int) : Int
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>Exemplo

```qsharp
let a = 248;
let x = Parity(a); // x : Int = 1.
```