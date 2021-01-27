---
title: Conversões de tipo nas Q# bibliotecas padrão
description: Saiba mais sobre as funções de conversão de tipo comuns e definidas pelo usuário nas Q# bibliotecas padrão.
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: 67f47339363a52097f342c8ae4e43a8a93d606a8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858016"
---
# <a name="type-conversions"></a>Conversões de tipo #

Q# é uma linguagem **fortemente tipada** .
Em particular, não Q# é implicitamente convertido entre tipos distintos. Por exemplo, `1 + 2.0` não é uma Q# expressão válida.
Em vez disso, Q# o fornece uma variedade de funções de conversão de tipo para construir novos valores de um determinado tipo.

Por exemplo, <xref:Microsoft.Quantum.Core.Length> tem um tipo de saída de `Int` , portanto, sua saída deve primeiro ser convertida para um `Double` antes que possa ser usada como parte de uma expressão de ponto flutuante.
Isso pode ser feito usando a <xref:Microsoft.Quantum.Convert.IntAsDouble> função:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

O <xref:Microsoft.Quantum.Convert> namespace fornece funções de conversão de tipo comuns para trabalhar com os tipos internos básicos, como `Int` ,, `Double` , `BigInt` `Result` e `Bool` :

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

O <xref:Microsoft.Quantum.Convert> namespace também fornece algumas conversões mais exóticas, como `FunctionAsOperation` , que converte as funções `'T -> 'U` em novas operações `'T => 'U` .

Por fim, a Q# biblioteca padrão fornece vários tipos definidos pelo usuário, como <xref:Microsoft.Quantum.Math.Complex> e <xref:Microsoft.Quantum.Arithmetic.LittleEndian> .
Juntamente com esses tipos, a biblioteca padrão fornece funções como <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian> :

```qsharp
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
