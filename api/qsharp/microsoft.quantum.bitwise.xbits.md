---
uid: Microsoft.Quantum.Bitwise.XBits
title: Função XBits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: ddaace8df6e4c47c4affe2eeffb8d8ce31f37327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845241"
---
# <a name="xbits-function"></a>Função XBits

Namespace: [Microsoft. Quantum. Nonbit](xref:Microsoft.Quantum.Bitwise)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retorna um inteiro que representa os X bits de uma matriz de operadores Pauli.

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Entrada

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Uma matriz de operadores Pauli a ser representada como um inteiro.



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Um inteiro $x $ com representação binária $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, em que $p _i = $0 se `paulis[i]` for `PauliI` ou `PauliZ` e onde $p _i = $1 se `paulis[i]` for `PauliX` ou `PauliY` .

## <a name="remarks"></a>Comentários

A função gerará se o comprimento da `paulis` matriz for maior que 63.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. bit-a-ZBits](xref:Microsoft.Quantum.Bitwise.ZBits)