---
title: 'Conversões de tipo nas bibliotecas padrão do Q #'
description: 'Saiba mais sobre funções de conversão de tipo comuns e definidas pelo usuário nas bibliotecas padrão do Q #.'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: e941d7e3d76459546861410e91a03d7315183867
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274287"
---
# <a name="type-conversions"></a>Conversões de tipo #

Q # é uma linguagem **fortemente tipada** .
Em particular, a p # não é implicitamente convertida entre tipos distintos. Por exemplo, `1 + 2.0` não é uma expressão Q # válida.
Em vez disso, o Q # fornece uma variedade de funções de conversão de tipo para construir novos valores de um determinado tipo.

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

Por fim, a biblioteca padrão de Q # fornece vários tipos definidos pelo usuário, como <xref:microsoft.quantum.math.complex> e <xref:microsoft.quantum.arithmetic.littleendian> .
Juntamente com esses tipos, a biblioteca padrão fornece funções como <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> :

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
