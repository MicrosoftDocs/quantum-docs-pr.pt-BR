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
# <a name="type-conversions"></a><span data-ttu-id="84282-103">Conversões de tipo</span><span class="sxs-lookup"><span data-stu-id="84282-103">Type Conversions</span></span> #

<span data-ttu-id="84282-104">Q#é uma linguagem **fortemente tipada** .</span><span class="sxs-lookup"><span data-stu-id="84282-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="84282-105">Em particular, não Q# é implicitamente convertido entre tipos distintos.</span><span class="sxs-lookup"><span data-stu-id="84282-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="84282-106">Por exemplo, `1 + 2.0` não é uma Q# expressão válida.</span><span class="sxs-lookup"><span data-stu-id="84282-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="84282-107">Em vez disso, Q# o fornece uma variedade de funções de conversão de tipo para construir novos valores de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="84282-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="84282-108">Por exemplo, <xref:microsoft.quantum.core.length> tem um tipo de saída de `Int` , portanto, sua saída deve primeiro ser convertida para um `Double` antes que possa ser usada como parte de uma expressão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="84282-108">For example, <xref:microsoft.quantum.core.length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="84282-109">Isso pode ser feito usando a <xref:microsoft.quantum.convert.intasdouble> função:</span><span class="sxs-lookup"><span data-stu-id="84282-109">This can be done using the <xref:microsoft.quantum.convert.intasdouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="84282-110">O <xref:microsoft.quantum.convert> namespace fornece funções de conversão de tipo comuns para trabalhar com os tipos internos básicos, como `Int` ,, `Double` , `BigInt` `Result` e `Bool` :</span><span class="sxs-lookup"><span data-stu-id="84282-110">The <xref:microsoft.quantum.convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="84282-111">O <xref:microsoft.quantum.convert> namespace também fornece algumas conversões mais exóticas, como `FunctionAsOperation` , que converte as funções `'T -> 'U` em novas operações `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="84282-111">The <xref:microsoft.quantum.convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="84282-112">Por fim, a Q# biblioteca padrão fornece vários tipos definidos pelo usuário, como <xref:microsoft.quantum.math.complex> e <xref:microsoft.quantum.arithmetic.littleendian> .</span><span class="sxs-lookup"><span data-stu-id="84282-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:microsoft.quantum.math.complex> and <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>
<span data-ttu-id="84282-113">Juntamente com esses tipos, a biblioteca padrão fornece funções como <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> :</span><span class="sxs-lookup"><span data-stu-id="84282-113">Along with these types, the standard library provides functions such as <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span></span>

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
