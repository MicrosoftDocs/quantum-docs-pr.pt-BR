---
title: Conversões de tipo nas Q# bibliotecas padrão
description: Saiba mais sobre as funções de conversão de tipo comuns e definidas pelo usuário nas Q# bibliotecas padrão.
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2319bf453f5fbf6bd068859ea65562423d3ff4d0
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868501"
---
# <a name="type-conversions"></a>Conversões de tipo #

Q#é uma linguagem **fortemente tipada** .
Em particular, não Q# é implicitamente convertido entre tipos distintos. Por exemplo, `1 + 2.0` não é uma Q# expressão válida.
Em vez disso, Q# o fornece uma variedade de funções de conversão de tipo para construir novos valores de um determinado tipo.

Por exemplo, <xref:microsoft.quantum.core.length> tem um tipo de saída de `Int` , portanto, sua saída deve primeiro ser convertida para um `Double` antes que possa ser usada como parte de uma expressão de ponto flutuante.
Isso pode ser feito usando a <xref:microsoft.quantum.convert.intasdouble> função:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

O <xref:microsoft.quantum.convert> namespace fornece funções de conversão de tipo comuns para trabalhar com os tipos internos básicos, como `Int` ,, `Double` , `BigInt` `Result` e `Bool` :

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

O <xref:microsoft.quantum.convert> namespace também fornece algumas conversões mais exóticas, como `FunctionAsOperation` , que converte as funções `'T -> 'U` em novas operações `'T => 'U` .

Por fim, a Q# biblioteca padrão fornece vários tipos definidos pelo usuário, como <xref:microsoft.quantum.math.complex> e <xref:microsoft.quantum.arithmetic.littleendian> .
Juntamente com esses tipos, a biblioteca padrão fornece funções como <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> :

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
