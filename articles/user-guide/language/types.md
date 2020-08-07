---
title: Tipos emQ#
description: Saiba mais sobre os diferentes tipos usados na Q# linguagem de programação.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
no-loc:
- Q#
- $$v
ms.openlocfilehash: b034af0b1d3b967b5680403341813407e4412f93
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869589"
---
# <a name="types-in-no-locq"></a><span data-ttu-id="54269-103">Tipos emQ#</span><span class="sxs-lookup"><span data-stu-id="54269-103">Types in Q#</span></span>

<span data-ttu-id="54269-104">Este artigo descreve o Q# modelo de tipo e a sintaxe para especificar e trabalhar com tipos.</span><span class="sxs-lookup"><span data-stu-id="54269-104">This article describes the Q# type model and the syntax for specifying and working with types.</span></span> <span data-ttu-id="54269-105">Para obter detalhes sobre como criar e operar em expressões desses tipos, consulte [expressões de tipo](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="54269-105">For details on how to create and operate on expressions of these types, see [Type Expressions](xref:microsoft.quantum.guide.expressions).</span></span>

<span data-ttu-id="54269-106">Observe que Q# é uma linguagem *fortemente tipada* , de modo que o uso cuidadoso desses tipos pode ajudar o compilador a fornecer fortes garantias sobre os Q# programas em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="54269-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="54269-107">Para fornecer as garantias mais fortes possíveis, as conversões entre os tipos no Q# devem ser explícitas usando chamadas para funções que expressam essa conversão.</span><span class="sxs-lookup"><span data-stu-id="54269-107">To provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> 
<span data-ttu-id="54269-108">Q#fornece uma variedade de funções desse tipo como parte do <xref:microsoft.quantum.convert> namespace.</span><span class="sxs-lookup"><span data-stu-id="54269-108">Q# provides a variety of such functions as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="54269-109">Por outro lado, os upcasts para tipos compatíveis ocorrem implicitamente.</span><span class="sxs-lookup"><span data-stu-id="54269-109">Upcasts to compatible types, on the other hand, happen implicitly.</span></span> 

<span data-ttu-id="54269-110">Q#fornece os dois tipos primitivos, que são usados diretamente e várias maneiras de produzir novos tipos de outros tipos.</span><span class="sxs-lookup"><span data-stu-id="54269-110">Q# provides both primitive types, which are used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="54269-111">Descrevemos cada um no restante deste artigo.</span><span class="sxs-lookup"><span data-stu-id="54269-111">We describe each in the rest of this article.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="54269-112">Tipos primitivos</span><span class="sxs-lookup"><span data-stu-id="54269-112">Primitive Types</span></span>

<span data-ttu-id="54269-113">A Q# linguagem fornece os seguintes *tipos primitivos*, todos os quais você pode usar diretamente em Q# programas.</span><span class="sxs-lookup"><span data-stu-id="54269-113">The Q# language provides the following *primitive types*, all of which you can use directly in Q# programs.</span></span> <span data-ttu-id="54269-114">Você também pode usar esses tipos primitivos para construir novos tipos.</span><span class="sxs-lookup"><span data-stu-id="54269-114">You can also use these primitive types to construct new types.</span></span>

- <span data-ttu-id="54269-115">O `Int` tipo representa um inteiro com sinal de 64 bits, por exemplo,,, `2` `107` `-5` .</span><span class="sxs-lookup"><span data-stu-id="54269-115">The `Int` type represents a 64-bit signed integer, for example, `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="54269-116">O `BigInt` tipo representa um inteiro assinado de tamanho arbitrário, por exemplo,,, `2L` `107L` `-5L` .</span><span class="sxs-lookup"><span data-stu-id="54269-116">The `BigInt` type represents a signed integer of arbitrary size, for example, `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="54269-117">Esse tipo é baseado no .NET<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="54269-117">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="54269-118">Escreva.</span><span class="sxs-lookup"><span data-stu-id="54269-118">type.</span></span>

- <span data-ttu-id="54269-119">O `Double` tipo representa um número de ponto flutuante de precisão dupla, por exemplo,,, `0.0` `-1.3` `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="54269-119">The `Double` type represents a double-precision floating-point number, for example, `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="54269-120">O `Bool` tipo representa um valor booliano de `true` ou `false` .</span><span class="sxs-lookup"><span data-stu-id="54269-120">The `Bool` type represents a Boolean value of either `true` or `false`.</span></span>
- <span data-ttu-id="54269-121">O `Range` tipo representa uma sequência de números inteiros, indicados por `start..step..stop` , em que a denotação da etapa é opcional.</span><span class="sxs-lookup"><span data-stu-id="54269-121">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is optional.</span></span> 
   <span data-ttu-id="54269-122">Por exemplo, `start .. stop` corresponde a `start..1..stop` e `1..2..7` representa a sequência $ \{ 1, 3, 5, 7 \} $.</span><span class="sxs-lookup"><span data-stu-id="54269-122">For example, `start .. stop` corresponds to `start..1..stop`, and `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="54269-123">O `String` tipo é uma sequência de caracteres Unicode que é opaca para o usuário depois de criado.</span><span class="sxs-lookup"><span data-stu-id="54269-123">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="54269-124">Use o `string` tipo para relatar mensagens para um host clássico no caso de um erro ou evento de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="54269-124">Use the `string` type to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="54269-125">O `Unit` tipo pode ter apenas um valor, `()` .</span><span class="sxs-lookup"><span data-stu-id="54269-125">The `Unit` type can have only one value, `()`.</span></span> 
  <span data-ttu-id="54269-126">Use esse tipo para indicar que uma Q# função ou operação não retorna nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="54269-126">Use this type to indicate that a Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="54269-127">O `Qubit` tipo representa um bit quântico ou qubit.</span><span class="sxs-lookup"><span data-stu-id="54269-127">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="54269-128">`Qubit`os s são opacos para o usuário.</span><span class="sxs-lookup"><span data-stu-id="54269-128">`Qubit`s are opaque to the user.</span></span> <span data-ttu-id="54269-129">A única operação possível com eles, além de passá-los para outra operação, é testar a identidade (igualdade).</span><span class="sxs-lookup"><span data-stu-id="54269-129">The only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="54269-130">Por fim, você implementa ações em `Qubit` s chamando instruções intrínsecas em um processador Quantum (ou um simulador Quantum).</span><span class="sxs-lookup"><span data-stu-id="54269-130">Ultimately, you implement actions on `Qubit`s by calling intrinsic instructions on a quantum processor (or a quantum simulator).</span></span>
- <span data-ttu-id="54269-131">O `Pauli` tipo representa um dos quatro operadores de Pauli de qubit único.</span><span class="sxs-lookup"><span data-stu-id="54269-131">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="54269-132">Use esse tipo para indicar a operação base para rotações e para especificar o observável que está sendo medido.</span><span class="sxs-lookup"><span data-stu-id="54269-132">Use this type to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="54269-133">É um tipo enumerado que tem quatro valores possíveis: `PauliI` ,, `PauliX` `PauliY` e `PauliZ` , que são constantes do tipo `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="54269-133">It is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="54269-134">O `Result` tipo representa o resultado de uma medida.</span><span class="sxs-lookup"><span data-stu-id="54269-134">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="54269-135">É um tipo enumerado com dois valores possíveis: `One` e `Zero` , que são constantes do tipo `Result` .</span><span class="sxs-lookup"><span data-stu-id="54269-135">It is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="54269-136">`Zero`indica que a eigenvalue + 1 foi medida; `One`indica que-1 eigenvalue foi medido.</span><span class="sxs-lookup"><span data-stu-id="54269-136">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue was measured.</span></span>

<span data-ttu-id="54269-137">As constantes,,,,,, `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` e `Zero` são todos os símbolos reservados no Q# .</span><span class="sxs-lookup"><span data-stu-id="54269-137">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="54269-138">Tipos de matriz</span><span class="sxs-lookup"><span data-stu-id="54269-138">Array Types</span></span>

* <span data-ttu-id="54269-139">Para qualquer Q# tipo válido, há um tipo que representa uma matriz de valores desse tipo.</span><span class="sxs-lookup"><span data-stu-id="54269-139">For any valid Q# type, there is a type that represents an array of values of that type.</span></span>
    <span data-ttu-id="54269-140">Por exemplo, `Qubit[]` e `(Bool, Pauli)[]` representam matrizes de `Qubit` valores e `(Bool, Pauli)` valores de tupla.</span><span class="sxs-lookup"><span data-stu-id="54269-140">For example, `Qubit[]` and `(Bool, Pauli)[]` represent arrays of `Qubit` values and `(Bool, Pauli)` tuple values.</span></span>

* <span data-ttu-id="54269-141">Uma matriz de matrizes também é válida.</span><span class="sxs-lookup"><span data-stu-id="54269-141">An array of arrays is also valid.</span></span> <span data-ttu-id="54269-142">Expandindo no exemplo anterior, uma matriz de `(Bool, Pauli)` matrizes é denotada `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="54269-142">Expanding on the previous example, an array of `(Bool, Pauli)` arrays is denoted `(Bool, Pauli)[][]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="54269-143">Este exemplo, `(Bool, Pauli)[][]` , representa uma matriz potencialmente irregular de matrizes e não uma matriz bidimensional retangular.</span><span class="sxs-lookup"><span data-stu-id="54269-143">This example, `(Bool, Pauli)[][]`, represents a potentially jagged array of arrays and not a rectangular two-dimensional array.</span></span> <span data-ttu-id="54269-144">Q#não oferece suporte a matrizes multidimensionais retangulares.</span><span class="sxs-lookup"><span data-stu-id="54269-144">Q# does not support rectangular multi-dimensional arrays.</span></span>

* <span data-ttu-id="54269-145">Um valor de matriz pode ser escrito no Q# código-fonte usando colchetes em volta dos elementos de uma matriz, como em `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="54269-145">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="54269-146">O tipo de base comum de todos os itens na matriz determina o tipo de um literal de matriz.</span><span class="sxs-lookup"><span data-stu-id="54269-146">The common base type of all items in the array determines the type of an array literal.</span></span> <span data-ttu-id="54269-147">Portanto, construir uma matriz com elementos que não têm nenhum tipo base comum gera um erro.</span><span class="sxs-lookup"><span data-stu-id="54269-147">Hence, constructing an array with elements that have no common base type raises an error.</span></span>  
<span data-ttu-id="54269-148">Para obter um exemplo, consulte [matrizes de callablefiles](xref:microsoft.quantum.guide.expressions#arrays-of-callables).</span><span class="sxs-lookup"><span data-stu-id="54269-148">For an example, see [arrays of callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables).</span></span>

    > [!WARNING]
    > <span data-ttu-id="54269-149">Depois de criados, os elementos de uma matriz não podem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="54269-149">Once created, the elements of an array cannot be changed.</span></span>
    > <span data-ttu-id="54269-150">Para construir uma matriz modificada, use as [instruções UPDATE-and-REASSIGN](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) ou as [expressões Copy-and-Update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="54269-150">To construct a modified array, use [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span>

* <span data-ttu-id="54269-151">Como alternativa, uma matriz pode ser criada com base em seu tamanho usando a `new` palavra-chave:</span><span class="sxs-lookup"><span data-stu-id="54269-151">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* <span data-ttu-id="54269-152">Use a função principal `Length` para obter o número de elementos de uma matriz como um `Int` .</span><span class="sxs-lookup"><span data-stu-id="54269-152">Use the core function `Length` to obtain the number of elements from an array as an `Int`.</span></span>
* <span data-ttu-id="54269-153">Matrizes podem ser inscrições para obter um único elemento ou novas matrizes que contenham um subconjunto dos elementos de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="54269-153">Arrays can be subscripted to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="54269-154">Os subscritos das matrizes são baseados em zero e devem ser do tipo `Int` ou tipo `Range` :</span><span class="sxs-lookup"><span data-stu-id="54269-154">The subscripts of arrays are zero-based and must be type `Int` or type `Range`:</span></span>

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a><span data-ttu-id="54269-155">Tipos de tupla</span><span class="sxs-lookup"><span data-stu-id="54269-155">Tuple Types</span></span>

<span data-ttu-id="54269-156">As tuplas são um conceito poderoso usado em todo Q# o mundo para coletar valores juntos em um único valor, facilitando sua passagem.</span><span class="sxs-lookup"><span data-stu-id="54269-156">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="54269-157">Em particular, usando a notação de tupla, você pode expressar que cada operação e que pode ser chamado leva exatamente uma entrada e retorna exatamente uma saída.</span><span class="sxs-lookup"><span data-stu-id="54269-157">In particular, using tuple notation, you can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

* <span data-ttu-id="54269-158">Dado zero ou mais tipos diferentes `T0` , `T1` ,..., `Tn` você pode indicar um novo *tipo de tupla* como `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="54269-158">Given zero or more different types `T0`, `T1`, ..., `Tn`, you can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="54269-159">Os tipos usados para construir um novo tipo de tupla podem ser tuplas, como em `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="54269-159">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="54269-160">No entanto, esse aninhamento é sempre finito, pois os tipos de tupla não podem, sob nenhuma circunstância, conter.</span><span class="sxs-lookup"><span data-stu-id="54269-160">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

* <span data-ttu-id="54269-161">Os valores do novo tipo de tupla são tuplas formadas por sequências de valores de cada tipo na tupla.</span><span class="sxs-lookup"><span data-stu-id="54269-161">The values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="54269-162">Por exemplo, `(3, false)` é uma tupla cujo tipo é o tipo de tupla `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="54269-162">For example, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="54269-163">É possível criar matrizes de tuplas, tuplas de matrizes, tuplas de subtuplas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="54269-163">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, and so on.</span></span>

* <span data-ttu-id="54269-164">A partir de Q# 0,3, `Unit` é o nome do *tipo* da tupla vazia; `()` é usado para o *valor* da tupla vazia.</span><span class="sxs-lookup"><span data-stu-id="54269-164">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the *value* of the empty tuple.</span></span>

* <span data-ttu-id="54269-165">As instâncias de tupla são imutáveis.</span><span class="sxs-lookup"><span data-stu-id="54269-165">Tuple instances are immutable.</span></span>
<span data-ttu-id="54269-166">Q#não fornece um mecanismo para alterar o conteúdo de uma tupla depois de criada.</span><span class="sxs-lookup"><span data-stu-id="54269-166">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>



### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="54269-167">Equivalência de tupla singleton</span><span class="sxs-lookup"><span data-stu-id="54269-167">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="54269-168">É possível criar uma tupla singleton (elemento único) `('T1)` , como `(5)` ou `([1,2,3])` .</span><span class="sxs-lookup"><span data-stu-id="54269-168">It is possible to create a singleton (single-element) tuple `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="54269-169">No entanto, Q# trata uma tupla singleton como equivalente a um valor do tipo incluído.</span><span class="sxs-lookup"><span data-stu-id="54269-169">However, Q# treats a singleton tuple as equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="54269-170">Ou seja, não há nenhuma diferença entre `5` e `(5)` , ou entre `5` e `(((5)))` , ou entre `(5, (6))` e `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="54269-170">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="54269-171">Ele é tão válido para gravar `(5)+3` como é para gravação `5+3` ; as duas expressões são avaliadas como `8` .</span><span class="sxs-lookup"><span data-stu-id="54269-171">It is just as valid to write `(5)+3` as it is to write `5+3`; both expressions evaluate to `8`.</span></span>

<span data-ttu-id="54269-172">Essa equivalência aplica-se a todas as finalidades, incluindo atribuições e expressões.</span><span class="sxs-lookup"><span data-stu-id="54269-172">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="54269-173">Dada qualquer expressão, a mesma expressão entre parênteses é uma expressão do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="54269-173">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="54269-174">Por exemplo, `(7)` é uma expressão do tipo `Int` , `([1,2,3])` é uma expressão do tipo `Int[]` e `((1,2))` é uma expressão do tipo `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="54269-174">For example, `(7)` is an expression of type `Int`, `([1,2,3])` is an expression of type `Int[]`, and `((1,2))` is an expression of type `(Int, Int)`.</span></span>

<span data-ttu-id="54269-175">Em particular, isso significa que você pode exibir uma operação ou função cuja tupla de entrada ou tipo de tupla de saída tem um campo como pegar um único argumento ou retornar um único valor.</span><span class="sxs-lookup"><span data-stu-id="54269-175">In particular, this means that you can view an operation or function whose input tuple or output tuple type has one field as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="54269-176">Nós nos referimos a essa propriedade como _equivalência de tupla singleton_.</span><span class="sxs-lookup"><span data-stu-id="54269-176">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="54269-177">Tipos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="54269-177">User-Defined Types</span></span>

<span data-ttu-id="54269-178">Uma declaração de tipo definida pelo usuário consiste na palavra-chave `newtype` , seguida pelo nome do tipo definido pelo usuário, uma `=` especificação de tipo válida e um ponto-e-vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="54269-178">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="54269-179">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="54269-179">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* <span data-ttu-id="54269-180">Cada Q# arquivo de origem pode declarar qualquer número de tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="54269-180">Each Q# source file may declare any number of user-defined types.</span></span>
* <span data-ttu-id="54269-181">Os nomes de tipo devem ser exclusivos em um namespace e podem não entrar em conflito com os nomes de operação e de função.</span><span class="sxs-lookup"><span data-stu-id="54269-181">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>
* <span data-ttu-id="54269-182">Os tipos definidos pelo usuário são distintos, mesmo que os tipos base sejam idênticos.</span><span class="sxs-lookup"><span data-stu-id="54269-182">User-defined types are distinct, even if the base types are identical.</span></span>
<span data-ttu-id="54269-183">Em particular, não há conversão automática entre os valores de dois tipos definidos pelo usuário, mesmo que os tipos subjacentes sejam idênticos.</span><span class="sxs-lookup"><span data-stu-id="54269-183">In particular, there is no automatic conversion between the values of two user-defined types, even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="54269-184">Itens nomeados vs. anônimos</span><span class="sxs-lookup"><span data-stu-id="54269-184">Named vs. anonymous items</span></span>

<span data-ttu-id="54269-185">Um Q# arquivo pode definir um novo tipo nomeado contendo um único valor de qualquer tipo legal.</span><span class="sxs-lookup"><span data-stu-id="54269-185">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="54269-186">Para qualquer tipo de tupla `T` , você pode declarar um novo tipo definido pelo usuário que seja um subtipo de `T` com a `newtype` instrução.</span><span class="sxs-lookup"><span data-stu-id="54269-186">For any tuple type `T`, you can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="54269-187">No @"microsoft.quantum.math" namespace, por exemplo, números complexos são definidos como um tipo definido pelo usuário:</span><span class="sxs-lookup"><span data-stu-id="54269-187">In the @"microsoft.quantum.math" namespace, for example, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="54269-188">Essa instrução cria um novo tipo com dois itens anônimos do tipo `Double` .</span><span class="sxs-lookup"><span data-stu-id="54269-188">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="54269-189">Além de itens anônimos, os tipos definidos pelo usuário também dão suporte a *itens nomeados* a partir da Q# versão 0,7 ou superior.</span><span class="sxs-lookup"><span data-stu-id="54269-189">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="54269-190">Por exemplo, você pode nomear os itens para `Re` para o duplo que representa a parte real de um número complexo e `Im` para a parte imaginária:</span><span class="sxs-lookup"><span data-stu-id="54269-190">For example, you could name the items to `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="54269-191">Nomear um item em um tipo definido pelo usuário não significa que todos os itens precisam ser nomeados-qualquer combinação de itens nomeados e sem nome é suportada.</span><span class="sxs-lookup"><span data-stu-id="54269-191">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="54269-192">Além disso, os itens internos também podem ser nomeados.</span><span class="sxs-lookup"><span data-stu-id="54269-192">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="54269-193">O tipo `Nested` , conforme definido abaixo, por exemplo, tem um tipo subjacente `(Double, (Int, String))` , do qual apenas o item do tipo `Int` é nomeado e todos os outros itens são anônimos.</span><span class="sxs-lookup"><span data-stu-id="54269-193">The type `Nested`, as defined below for example, has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named, and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="54269-194">Os itens nomeados têm a vantagem de que eles podem ser acessados diretamente por meio do *operador de acesso* `::` .</span><span class="sxs-lookup"><span data-stu-id="54269-194">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="54269-195">Além de fornecer aliases curtos para tipos de tupla potencialmente complicadas, uma vantagem significativa de definir esses tipos é que eles podem documentar a intenção de um valor específico.</span><span class="sxs-lookup"><span data-stu-id="54269-195">In addition to providing short aliases for potentially complicated tuple types, a significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="54269-196">Retornando ao exemplo de `Complex` , um também poderia ter definido as coordenadas polares 2D como um tipo definido pelo usuário:</span><span class="sxs-lookup"><span data-stu-id="54269-196">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="54269-197">Embora ambos `Complex` `Polar` tenham um tipo subjacente `(Double, Double)` , os dois tipos são totalmente incompatíveis no Q# , minimizando o risco de chamar acidentalmente uma função matemática complexa com coordenadas polares e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="54269-197">Even though both `Complex` and `Polar` both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="54269-198">Acessar itens anônimos com o operador de desencapsulamento</span><span class="sxs-lookup"><span data-stu-id="54269-198">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="54269-199">Para acessar itens anônimos, primeiro extraia o valor encapsulado usando o operador de sufixo `!` .</span><span class="sxs-lookup"><span data-stu-id="54269-199">To access anonymous items, first extract the wrapped value using the postfix operator `!`.</span></span>
<span data-ttu-id="54269-200">Com o operador "sem encapsulamento", `!` você pode extrair o valor contido em um tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="54269-200">With the "unwrap" operator, `!`, you can extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="54269-201">O tipo dessa expressão de "desencapsulamento" é o tipo subjacente do tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="54269-201">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="54269-202">Um único operador de desencapsulamento desencapsula uma camada de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="54269-202">A single unwrap operator unwraps one layer of wrapping.</span></span> <span data-ttu-id="54269-203">Use vários operadores de desencapsulamento para acessar um valor com disposição multiplicada.</span><span class="sxs-lookup"><span data-stu-id="54269-203">Use multiple unwrap operators to access a multiply-wrapped value.</span></span>

<span data-ttu-id="54269-204">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="54269-204">For example:</span></span>

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

<span data-ttu-id="54269-205">Para obter mais detalhes sobre o operador de desencapsulamento, consulte [expressões de tipo em Q# ](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="54269-205">For more details on the unwrap operator, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="54269-206">Criando valores de tipos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="54269-206">Creating values of user-defined types</span></span>

<span data-ttu-id="54269-207">Crie valores de um tipo definido pelo usuário chamando o construtor de tipo correspondente:</span><span class="sxs-lookup"><span data-stu-id="54269-207">Create values of a user-defined type by calling the corresponding type constructor:</span></span>

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="54269-208">Como alternativa, você pode criar novos valores de existentes usando [expressões de copiar e atualizar](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="54269-208">Alternatively, you can create new values from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="54269-209">Assim como acontece com matrizes, as expressões Copy-and-Update copiam todos os valores de item da expressão original, exceto os itens nomeados especificados.</span><span class="sxs-lookup"><span data-stu-id="54269-209">Just as they do with arrays, copy-and-update expressions copy all item values of the original expression, except for the specified named items.</span></span> <span data-ttu-id="54269-210">Para essas exceções, os valores desses itens são os valores definidos no lado direito da expressão.</span><span class="sxs-lookup"><span data-stu-id="54269-210">For these exceptions, the values of these items are the values defined on the right-hand side of the expression.</span></span> <span data-ttu-id="54269-211">Qualquer outra construção de linguagem que esteja disponível para itens de matriz, por exemplo, [atualizar e reatribuir instruções](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), existir para itens nomeados em tipos definidos pelo usuário também.</span><span class="sxs-lookup"><span data-stu-id="54269-211">Any other language constructs that are available for array items, for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), exist for named-items in user-defined types as well.</span></span>

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

* <span data-ttu-id="54269-212">Você pode usar tipos definidos pelo usuário em qualquer lugar em que usar qualquer outro tipo.</span><span class="sxs-lookup"><span data-stu-id="54269-212">You can use user-defined types anywhere you use any other types.</span></span>
<span data-ttu-id="54269-213">Em particular, é possível definir uma matriz de um tipo definido pelo usuário e incluir um tipo definido pelo usuário como um elemento de um tipo de tupla.</span><span class="sxs-lookup"><span data-stu-id="54269-213">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

* <span data-ttu-id="54269-214">Não é possível criar estruturas de tipo recursiva.</span><span class="sxs-lookup"><span data-stu-id="54269-214">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="54269-215">Ou seja, o tipo que define um tipo definido pelo usuário não pode ser um tipo de tupla que inclua um elemento do tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="54269-215">That is, the type that defines a user-defined type cannot be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="54269-216">Em geral, os tipos definidos pelo usuário podem não ter dependências cíclicas entre si, portanto, o seguinte conjunto de definições de tipo é inválido:</span><span class="sxs-lookup"><span data-stu-id="54269-216">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions are invalid:</span></span>

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a><span data-ttu-id="54269-217">Operação e tipos de função</span><span class="sxs-lookup"><span data-stu-id="54269-217">Operation and Function Types</span></span>

<span data-ttu-id="54269-218">Considerando os tipos `'Tinput` e `'Tresult` :</span><span class="sxs-lookup"><span data-stu-id="54269-218">Given the types `'Tinput` and `'Tresult`:</span></span>

* <span data-ttu-id="54269-219">`('Tinput => 'Tresult)`é o tipo básico para qualquer *operação*, por exemplo `((Qubit, Pauli) => Result)` .</span><span class="sxs-lookup"><span data-stu-id="54269-219">`('Tinput => 'Tresult)` is the basic type for any *operation*, for example `((Qubit, Pauli) => Result)`.</span></span>
* <span data-ttu-id="54269-220">`('Tinput -> 'Tresult)`é o tipo básico para qualquer *função*, por exemplo `(Int -> Int)` .</span><span class="sxs-lookup"><span data-stu-id="54269-220">`('Tinput -> 'Tresult)` is the basic type for any *function*, for example `(Int -> Int)`.</span></span> 

<span data-ttu-id="54269-221">Eles são chamados de *assinatura* do callable.</span><span class="sxs-lookup"><span data-stu-id="54269-221">These are called the *signature* of the callable.</span></span>

* <span data-ttu-id="54269-222">Todos os Q# chamados usam um único valor como entrada e retornam um único valor como saída.</span><span class="sxs-lookup"><span data-stu-id="54269-222">All Q# callables take a single value as input and return a single value as output.</span></span>
* <span data-ttu-id="54269-223">Você pode usar tuplas para os valores de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="54269-223">You can use tuples for both the input and output values.</span></span>
* <span data-ttu-id="54269-224">Chamadores que não têm resultado, retornam `Unit` .</span><span class="sxs-lookup"><span data-stu-id="54269-224">Callables that have no result, return `Unit`.</span></span>
* <span data-ttu-id="54269-225">Os chamadores que não têm nenhuma entrada usam a tupla vazia como entrada.</span><span class="sxs-lookup"><span data-stu-id="54269-225">Callables that have no input take the empty tuple as input.</span></span>

### <a name="functors"></a><span data-ttu-id="54269-226">Transmissão functors</span><span class="sxs-lookup"><span data-stu-id="54269-226">Functors</span></span>

<span data-ttu-id="54269-227">Os tipos de *função* são completamente especificados por sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="54269-227">*Function* types are completely specified by their signature.</span></span> <span data-ttu-id="54269-228">Por exemplo, uma função que computa o seno de um ângulo teria tipo `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="54269-228">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span> 

<span data-ttu-id="54269-229">*As operações* têm determinadas características adicionais que são expressas como parte do tipo de operação.</span><span class="sxs-lookup"><span data-stu-id="54269-229">*Operations* have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="54269-230">Essas características incluem informações sobre a qual *transmissão functors* a operação dá suporte.</span><span class="sxs-lookup"><span data-stu-id="54269-230">Such characteristics include information about which *functors* the operation supports.</span></span>
<span data-ttu-id="54269-231">Por exemplo, se a execução da operação depender do estado de outros qubits, ela deverá dar suporte a `Controlled` functor; se a operação tiver um inverso, ela deverá dar suporte ao `Adjoint` functor.</span><span class="sxs-lookup"><span data-stu-id="54269-231">For example, if the execution of the operation relies on the state of other qubits, then it should support the `Controlled` functor; if the operation has an inverse, then it should support the `Adjoint` functor.</span></span>

> [!NOTE]
> <span data-ttu-id="54269-232">Este artigo aborda apenas como transmissão functors a alteração da assinatura de operação.</span><span class="sxs-lookup"><span data-stu-id="54269-232">This article only discuss how functors alter the operation signature.</span></span> <span data-ttu-id="54269-233">Para obter mais detalhes sobre transmissão functors e operações, consulte [operações e funções Q# no ](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="54269-233">For more details about functors and operations, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span> 

<span data-ttu-id="54269-234">Para exigir suporte para o `Controlled` e/ou `Adjoint` functor em um tipo de operação, você precisa adicionar uma anotação que indica as características correspondentes.</span><span class="sxs-lookup"><span data-stu-id="54269-234">To require support for the `Controlled` and/or `Adjoint` functor in an operation type, you need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="54269-235">A anotação `is Ctl` (por exemplo, `(Qubit => Unit is Ctl)` ) indica que a operação é controlável.</span><span class="sxs-lookup"><span data-stu-id="54269-235">The annotation `is Ctl` (for example, `(Qubit => Unit is Ctl)`) indicates that the operation is controllable.</span></span> <span data-ttu-id="54269-236">Ou seja, sua execução depende do estado de outro qubit ou qubits.</span><span class="sxs-lookup"><span data-stu-id="54269-236">That is, its execution relies on the state of another qubit or qubits.</span></span> <span data-ttu-id="54269-237">Da mesma forma, a anotação `is Adj` indica que a operação tem um erro, ou seja, pode ser "invertida", de forma que a aplicação sucessiva de uma operação e, em seguida, o estado adjacente a um State deixa o estado inalterado.</span><span class="sxs-lookup"><span data-stu-id="54269-237">Similarly, the annotation `is Adj` indicates that the operation has an adjoint, that is, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="54269-238">Se você quiser exigir que uma operação desse tipo dê suporte a `Adjoint` e functor, `Controlled` você pode expressar isso como `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="54269-238">If you want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor you can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="54269-239">Por exemplo, a operação Pauli interna <xref:microsoft.quantum.intrinsic.x> tem o tipo `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="54269-239">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="54269-240">Um tipo de operação que não dá suporte a nenhum transmissão functors é especificado por seu tipo de entrada e saída sozinho, sem anotação adicional.</span><span class="sxs-lookup"><span data-stu-id="54269-240">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="54269-241">Funções e operações com parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="54269-241">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="54269-242">Tipos chamáveis podem conter *parâmetros de tipo*.</span><span class="sxs-lookup"><span data-stu-id="54269-242">Callable types may contain *type parameters*.</span></span>
<span data-ttu-id="54269-243">Use um símbolo prefixado por uma aspa simples para indicar um parâmetro de tipo; por exemplo, `'A` é um parâmetro de tipo legal.</span><span class="sxs-lookup"><span data-stu-id="54269-243">Use a symbol prefixed by a single quote to indicated a type parameter; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="54269-244">Para obter mais informações e detalhes sobre como definir os chamadores com parâmetros de tipo, consulte [operações e funções Q# no ](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).</span><span class="sxs-lookup"><span data-stu-id="54269-244">For more information and details on how to define type-parameterized callables, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).</span></span>

<span data-ttu-id="54269-245">Um parâmetro de tipo pode aparecer mais de uma vez em uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="54269-245">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="54269-246">Por exemplo, uma função que aplica outra função a cada elemento de uma matriz e retorna os resultados coletados tem a assinatura `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="54269-246">For example, a function that applies another function to each element of an array and returns the collected results has the signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="54269-247">Da mesma forma, uma função que retorna a composição de duas operações tem a assinatura `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="54269-247">Similarly, a function that returns the composition of two operations has the signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="54269-248">Quando você invoca um callable-parametrizado de tipo, todos os argumentos que têm o mesmo parâmetro de tipo devem ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="54269-248">When you invoke a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="54269-249">Q#não fornece um mecanismo para restringir os possíveis tipos que um usuário pode substituir por um parâmetro de tipo.</span><span class="sxs-lookup"><span data-stu-id="54269-249">Q# does not provide a mechanism for constraining the possible types that a user might substitute for a type parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="54269-250">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="54269-250">Next steps</span></span>

<span data-ttu-id="54269-251">Agora que você viu todos os tipos que compõem a Q# linguagem, consulte [expressões de tipo no Q# ](xref:microsoft.quantum.guide.expressions) para saber como criar e manipular expressões desses vários tipos.</span><span class="sxs-lookup"><span data-stu-id="54269-251">Now that you've seen all the types which comprise the Q# language, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to learn how to create and manipulate expressions of these various types.</span></span>
