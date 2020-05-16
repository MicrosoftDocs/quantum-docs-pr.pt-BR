---
title: 'Tipos em p #'
description: 'Saiba mais sobre os diferentes tipos usados na linguagem de programação Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: 58370193bd62e306197a9e07c28f8611f043e55c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431131"
---
# <a name="types-in-q"></a><span data-ttu-id="f1316-103">Tipos em p #</span><span class="sxs-lookup"><span data-stu-id="f1316-103">Types in Q#</span></span>

<span data-ttu-id="f1316-104">Esta página cria o modelo de tipo Q # e descreve a sintaxe para especificar e trabalhar com tipos.</span><span class="sxs-lookup"><span data-stu-id="f1316-104">This page lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="f1316-105">A próxima página, [digite expressões](xref:microsoft.quantum.guide.expressions), detalha como criar e operar em expressões desses tipos.</span><span class="sxs-lookup"><span data-stu-id="f1316-105">The next page, [Type Expressions](xref:microsoft.quantum.guide.expressions), details how to create and operate on expressions of these types.</span></span>

<span data-ttu-id="f1316-106">Observe que Q # é uma linguagem *fortemente tipada* , de modo que o uso cuidadoso desses tipos pode ajudar o compilador a fornecer fortes garantias sobre programas do Q # no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="f1316-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="f1316-107">Para fornecer as garantias mais fortes possíveis, as conversões entre os tipos em Q # devem ser explícitas usando chamadas para funções que expressam essa conversão.</span><span class="sxs-lookup"><span data-stu-id="f1316-107">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="f1316-108">Uma variedade dessas funções é fornecida como parte do <xref:microsoft.quantum.convert> namespace.</span><span class="sxs-lookup"><span data-stu-id="f1316-108">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="f1316-109">Os upcasts para tipos compatíveis, por outro lado, acontecem implicitamente.</span><span class="sxs-lookup"><span data-stu-id="f1316-109">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="f1316-110">O Q # fornece os dois tipos primitivos, que podem ser usados diretamente e várias maneiras de produzir novos tipos de outros tipos.</span><span class="sxs-lookup"><span data-stu-id="f1316-110">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="f1316-111">Descrevemos cada um no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="f1316-111">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="f1316-112">Tipos primitivos</span><span class="sxs-lookup"><span data-stu-id="f1316-112">Primitive Types</span></span>

<span data-ttu-id="f1316-113">A linguagem Q # fornece vários *tipos primitivos*, dos quais outros tipos podem ser construídos:</span><span class="sxs-lookup"><span data-stu-id="f1316-113">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="f1316-114">O `Int` tipo representa um número inteiro com sinal de 64 bits, por exemplo: `2` , `107` , `-5` .</span><span class="sxs-lookup"><span data-stu-id="f1316-114">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="f1316-115">O `BigInt` tipo representa um inteiro assinado de tamanho arbitrário, por exemplo,, `2L` `107L` `-5L` .</span><span class="sxs-lookup"><span data-stu-id="f1316-115">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="f1316-116">Esse tipo é baseado no .NET<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="f1316-116">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="f1316-117">Escreva.</span><span class="sxs-lookup"><span data-stu-id="f1316-117">type.</span></span>
- <span data-ttu-id="f1316-118">O `Double` tipo representa um número de ponto flutuante de precisão dupla, por exemplo: `0.0` , `-1.3` , `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="f1316-118">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="f1316-119">O `Bool` tipo representa um valor booliano que pode ser `true` ou `false` .</span><span class="sxs-lookup"><span data-stu-id="f1316-119">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="f1316-120">O `Range` tipo representa uma sequência de inteiros, denotada por `start..step..stop` , em que indica que a etapa é opções.</span><span class="sxs-lookup"><span data-stu-id="f1316-120">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is options.</span></span> 
   <span data-ttu-id="f1316-121">Que `start .. stop` corresponde a `start..1..stop` e, por exemplo, `1..2..7` representa a sequência $ \{ 1, 3, 5, 7 \} $.</span><span class="sxs-lookup"><span data-stu-id="f1316-121">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="f1316-122">O `String` tipo é uma sequência de caracteres Unicode que é opaca para o usuário depois de criado.</span><span class="sxs-lookup"><span data-stu-id="f1316-122">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="f1316-123">Esse tipo é usado para relatar mensagens a um host clássico no caso de um erro ou evento de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f1316-123">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="f1316-124">O `Unit` tipo é o tipo que permite apenas um valor `()` .</span><span class="sxs-lookup"><span data-stu-id="f1316-124">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="f1316-125">Esse tipo é usado para indicar que a função ou operação Q # não retorna nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="f1316-125">This type is used to indicate that Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="f1316-126">O `Qubit` tipo representa um bit quântico ou qubit.</span><span class="sxs-lookup"><span data-stu-id="f1316-126">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="f1316-127">`Qubit`os s são opacos para o usuário; a única operação possível com eles, além de passá-los para outra operação, é testar a identidade (igualdade).</span><span class="sxs-lookup"><span data-stu-id="f1316-127">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="f1316-128">Por fim, as ações em `Qubit` s são implementadas chamando instruções intrínsecas em um processador Quantum (ou em uma simulação delas).</span><span class="sxs-lookup"><span data-stu-id="f1316-128">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="f1316-129">O `Pauli` tipo representa um dos quatro operadores de Pauli de qubit único.</span><span class="sxs-lookup"><span data-stu-id="f1316-129">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="f1316-130">Esse tipo é usado para indicar a operação base para rotações e para especificar o observável que está sendo medido.</span><span class="sxs-lookup"><span data-stu-id="f1316-130">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="f1316-131">Este é um tipo enumerado que tem quatro valores possíveis: `PauliI` , `PauliX` , `PauliY` e `PauliZ` , que são constantes do tipo `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="f1316-131">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="f1316-132">O `Result` tipo representa o resultado de uma medida.</span><span class="sxs-lookup"><span data-stu-id="f1316-132">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="f1316-133">Este é um tipo enumerado com dois valores possíveis: `One` e `Zero` , que são constantes do tipo `Result` .</span><span class="sxs-lookup"><span data-stu-id="f1316-133">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="f1316-134">`Zero`indica que a eigenvalue + 1 foi medida; `One`indica o-1 eigenvalue.</span><span class="sxs-lookup"><span data-stu-id="f1316-134">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>

<span data-ttu-id="f1316-135">As constantes,,,,,, `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` e `Zero` são todos os símbolos reservados em Q #.</span><span class="sxs-lookup"><span data-stu-id="f1316-135">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="f1316-136">Tipos de matriz</span><span class="sxs-lookup"><span data-stu-id="f1316-136">Array Types</span></span>

<span data-ttu-id="f1316-137">Dado qualquer tipo válido de Q # `'T` , há um tipo que representa uma matriz de valores do tipo `'T` .</span><span class="sxs-lookup"><span data-stu-id="f1316-137">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="f1316-138">Esse tipo de matriz é representado como `'T[]` ; por exemplo, `Qubit[]` ou `Int[][]` .</span><span class="sxs-lookup"><span data-stu-id="f1316-138">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="f1316-139">Por exemplo, uma coleção de inteiros é denotada `Int[]` , enquanto uma matriz de matrizes de `(Bool, Pauli)` valores é denotada `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="f1316-139">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="f1316-140">No segundo exemplo, observe que isso representa uma matriz potencialmente irregular de matrizes e não uma matriz bidimensional retangular.</span><span class="sxs-lookup"><span data-stu-id="f1316-140">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="f1316-141">O Q # não fornece suporte para matrizes multidimensionais retangulares.</span><span class="sxs-lookup"><span data-stu-id="f1316-141">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="f1316-142">Um valor de matriz pode ser escrito em código-fonte Q # usando colchetes em volta dos elementos de uma matriz, como em `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="f1316-142">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="f1316-143">O tipo de um literal de matriz é determinado pelo tipo base comum de todos os itens na matriz.</span><span class="sxs-lookup"><span data-stu-id="f1316-143">The type of an array literal is determined by the common base type of all items in the array.</span></span> 

> [!WARNING]
> <span data-ttu-id="f1316-144">Os elementos de uma matriz não podem ser alterados após a criação da matriz.</span><span class="sxs-lookup"><span data-stu-id="f1316-144">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="f1316-145">As [instruções UPDATE-and-REASSIGN](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) e/ou as [expressões Copy-and-Update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) podem ser usadas para construir uma matriz modificada.</span><span class="sxs-lookup"><span data-stu-id="f1316-145">[Update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) and/or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) can be used to construct a modified array.</span></span>

<span data-ttu-id="f1316-146">Como alternativa, uma matriz pode ser criada com base em seu tamanho usando a `new` palavra-chave:</span><span class="sxs-lookup"><span data-stu-id="f1316-146">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="f1316-147">Em ambos os casos, após a construção de uma matriz, a função principal `Length` pode ser usada para obter o número de elementos como um `Int` .</span><span class="sxs-lookup"><span data-stu-id="f1316-147">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="f1316-148">As matrizes podem ser subscritos usando colchetes, com subscritos que têm tipo `Int` ou tipo `Range` , para obter elementos únicos ou novas matrizes que contenham um subconjunto dos elementos de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="f1316-148">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="f1316-149">Os subscritos das matrizes são baseados em zero:</span><span class="sxs-lookup"><span data-stu-id="f1316-149">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="f1316-150">Tipos de tupla</span><span class="sxs-lookup"><span data-stu-id="f1316-150">Tuple Types</span></span>

<span data-ttu-id="f1316-151">Dado zero ou mais tipos diferentes `T0` , `T1` ,..., `Tn` , podemos indicar um novo *tipo de tupla* como `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="f1316-151">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="f1316-152">Os tipos usados para construir um novo tipo de tupla podem ser tuplas, como em `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="f1316-152">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="f1316-153">No entanto, esse aninhamento é sempre finito, pois os tipos de tupla não podem, sob nenhuma circunstância, conter.</span><span class="sxs-lookup"><span data-stu-id="f1316-153">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="f1316-154">Os valores do novo tipo de tupla são tuplas formadas por sequências de valores de cada tipo na tupla.</span><span class="sxs-lookup"><span data-stu-id="f1316-154">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="f1316-155">Por exemplo, `(3, false)` é uma tupla cujo tipo é o tipo de tupla `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="f1316-155">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="f1316-156">É possível criar matrizes de tuplas, tuplas de matrizes, tuplas de subtuplas, etc.</span><span class="sxs-lookup"><span data-stu-id="f1316-156">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="f1316-157">A partir de Q # 0,3, `Unit` é o nome do *tipo* da tupla vazia; `()` é usado para o *valor*de tupla vazio.</span><span class="sxs-lookup"><span data-stu-id="f1316-157">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="f1316-158">As instâncias de tupla são imutáveis.</span><span class="sxs-lookup"><span data-stu-id="f1316-158">Tuple instances are immutable.</span></span>
<span data-ttu-id="f1316-159">O Q # não fornece um mecanismo para alterar o conteúdo de uma tupla depois de criada.</span><span class="sxs-lookup"><span data-stu-id="f1316-159">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="f1316-160">As tuplas são um conceito poderoso usado em toda a p # para coletar valores juntos em um único valor, facilitando sua passagem.</span><span class="sxs-lookup"><span data-stu-id="f1316-160">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="f1316-161">Em particular, usando a notação de tupla, podemos expressar que cada operação e que pode ser chamado leva exatamente uma entrada e retorna exatamente uma saída.</span><span class="sxs-lookup"><span data-stu-id="f1316-161">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="f1316-162">Equivalência de tupla singleton</span><span class="sxs-lookup"><span data-stu-id="f1316-162">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="f1316-163">É possível criar uma tupla singleton (elemento único), como `('T1)` `(5)` ou `([1,2,3])` .</span><span class="sxs-lookup"><span data-stu-id="f1316-163">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="f1316-164">No entanto, Q # trata uma tupla singleton como totalmente equivalente a um valor do tipo incluído.</span><span class="sxs-lookup"><span data-stu-id="f1316-164">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="f1316-165">Ou seja, não há nenhuma diferença entre `5` e `(5)` , ou entre `5` e `(((5)))` , ou entre `(5, (6))` e `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="f1316-165">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="f1316-166">Ele é tão válido para gravar `(5)+3` como gravar `5+3` e as duas expressões serão avaliadas como `8` .</span><span class="sxs-lookup"><span data-stu-id="f1316-166">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>

<span data-ttu-id="f1316-167">Essa equivalência aplica-se a todas as finalidades, incluindo atribuições e expressões.</span><span class="sxs-lookup"><span data-stu-id="f1316-167">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="f1316-168">Dada qualquer expressão, a mesma expressão entre parênteses é uma expressão do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="f1316-168">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="f1316-169">Por exemplo, `(7)` é uma `Int` expressão, `([1,2,3])` é uma expressão do tipo matriz de `Int` s e `((1,2))` é uma expressão com tipo `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="f1316-169">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="f1316-170">Em particular, isso significa que uma operação ou função cuja tupla de entrada ou tipo de tupla de saída tem um campo pode ser considerada como um único argumento ou retornando um único valor.</span><span class="sxs-lookup"><span data-stu-id="f1316-170">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="f1316-171">Nós nos referimos a essa propriedade como _equivalência de tupla singleton_.</span><span class="sxs-lookup"><span data-stu-id="f1316-171">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="f1316-172">Tipos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="f1316-172">User-Defined Types</span></span>

<span data-ttu-id="f1316-173">Uma declaração de tipo definida pelo usuário consiste na palavra-chave `newtype` , seguida pelo nome do tipo definido pelo usuário, uma `=` especificação de tipo válida e um ponto-e-vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="f1316-173">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="f1316-174">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f1316-174">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="f1316-175">Cada arquivo de origem Q # pode declarar qualquer número de tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f1316-175">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="f1316-176">Os nomes de tipo devem ser exclusivos em um namespace e podem não entrar em conflito com os nomes de operação e de função.</span><span class="sxs-lookup"><span data-stu-id="f1316-176">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="f1316-177">Os tipos definidos pelo usuário são distintos mesmo se os tipos base forem idênticos.</span><span class="sxs-lookup"><span data-stu-id="f1316-177">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="f1316-178">Em particular, não há conversão automática entre valores de dois tipos definidos pelo usuário, mesmo que os tipos subjacentes sejam idênticos.</span><span class="sxs-lookup"><span data-stu-id="f1316-178">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="f1316-179">Itens nomeados vs. anônimos</span><span class="sxs-lookup"><span data-stu-id="f1316-179">Named vs. anonymous items</span></span>

<span data-ttu-id="f1316-180">Um arquivo Q # pode definir um novo tipo nomeado contendo um único valor de qualquer tipo legal.</span><span class="sxs-lookup"><span data-stu-id="f1316-180">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="f1316-181">Para qualquer tipo de tupla `T` , podemos declarar um novo tipo definido pelo usuário que seja um subtipo de `T` com a `newtype` instrução.</span><span class="sxs-lookup"><span data-stu-id="f1316-181">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="f1316-182">No @"microsoft.quantum.math" namespace, por exemplo, números complexos são definidos como um tipo definido pelo usuário:</span><span class="sxs-lookup"><span data-stu-id="f1316-182">In the @"microsoft.quantum.math" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="f1316-183">Essa instrução cria um novo tipo com dois itens anônimos do tipo `Double` .</span><span class="sxs-lookup"><span data-stu-id="f1316-183">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="f1316-184">Além de itens anônimos, os tipos definidos pelo usuário também dão suporte a *itens nomeados* a partir do Q # versão 0,7 ou superior.</span><span class="sxs-lookup"><span data-stu-id="f1316-184">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="f1316-185">Por exemplo, poderíamos ter nomeado o to Items `Re` para o Double representando a parte real de um número complexo e `Im` para a parte imaginária:</span><span class="sxs-lookup"><span data-stu-id="f1316-185">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="f1316-186">Nomear um item em um tipo definido pelo usuário não significa que todos os itens precisam ser nomeados-qualquer combinação de itens nomeados e sem nome é suportada.</span><span class="sxs-lookup"><span data-stu-id="f1316-186">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="f1316-187">Além disso, os itens internos também podem ser nomeados.</span><span class="sxs-lookup"><span data-stu-id="f1316-187">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="f1316-188">O tipo `Nested` conforme definido abaixo, por exemplo, tem um tipo subjacente `(Double, (Int, String))` , do qual apenas o item do tipo `Int` é nomeado e todos os outros itens são anônimos.</span><span class="sxs-lookup"><span data-stu-id="f1316-188">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="f1316-189">Os itens nomeados têm a vantagem de que eles podem ser acessados diretamente por meio do *operador de acesso* `::` .</span><span class="sxs-lookup"><span data-stu-id="f1316-189">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="f1316-190">Além de fornecer aliases curtos para tipos de tupla potencialmente complicadas, uma vantagem significativa de definir esses tipos é que eles podem documentar a intenção de um valor específico.</span><span class="sxs-lookup"><span data-stu-id="f1316-190">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="f1316-191">Retornando ao exemplo de `Complex` , um também poderia ter definido as coordenadas polares 2D como um tipo definido pelo usuário:</span><span class="sxs-lookup"><span data-stu-id="f1316-191">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="f1316-192">Embora ambos `Complex` `Polar` tenham um tipo subjacente `(Double, Double)` , os dois tipos são totalmente incompatíveis em Q #, minimizando o risco de chamar acidentalmente uma função matemática complexa com coordenadas polares e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="f1316-192">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="f1316-193">Dessa forma, os tipos definidos pelo usuário têm uma função semelhante à de registros em F #, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="f1316-193">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="f1316-194">Acessar itens anônimos com o operador de desencapsulamento</span><span class="sxs-lookup"><span data-stu-id="f1316-194">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="f1316-195">Para acessar itens anônimos por outro lado, o valor encapsulado primeiro precisa ser extraído usando o operador de sufixo `!` .</span><span class="sxs-lookup"><span data-stu-id="f1316-195">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="f1316-196">O operador "Unwrap", `!` , permite extrair o valor contido em um tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f1316-196">The "unwrap" operator, `!`, allows to extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="f1316-197">O tipo dessa expressão de "desencapsulamento" é o tipo subjacente do tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f1316-197">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="f1316-198">O operador de desencapsulamento não encapsula exatamente uma camada de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="f1316-198">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="f1316-199">Vários operadores de desencapsulamento podem ser usados para acessar um valor com disposição multiplicada.</span><span class="sxs-lookup"><span data-stu-id="f1316-199">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="f1316-200">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f1316-200">For instance:</span></span>

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

<span data-ttu-id="f1316-201">Mais detalhes sobre o operador de desencapsulamento podem ser encontrados em [expressões de tipo em Q #](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="f1316-201">More details on the unwrap operator can be found at [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="f1316-202">Criando valores de tipos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="f1316-202">Creating values of user-defined types</span></span>

<span data-ttu-id="f1316-203">Os valores de um tipo definido pelo usuário podem ser criados chamando o construtor de tipo correspondente:</span><span class="sxs-lookup"><span data-stu-id="f1316-203">Values of a user-defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="f1316-204">Como alternativa, novos valores podem ser criados de existentes usando [expressões de copiar e atualizar](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="f1316-204">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="f1316-205">Assim como para matrizes, essas expressões copiam todos os valores de item da expressão original, com exceção dos itens nomeados especificados.</span><span class="sxs-lookup"><span data-stu-id="f1316-205">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="f1316-206">Para esses valores são definidos como aqueles definidos no lado direito da expressão.</span><span class="sxs-lookup"><span data-stu-id="f1316-206">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="f1316-207">Qualquer outra construção de linguagem, como por exemplo, [atualizar e reatribuir instruções](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), que estão disponíveis para itens de matriz existem para itens nomeados em tipos definidos pelo usuário também.</span><span class="sxs-lookup"><span data-stu-id="f1316-207">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), that are available for array items exist for named-items in user-defined types as well.</span></span>

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

<span data-ttu-id="f1316-208">Tipos definidos pelo usuário podem ser usados em qualquer lugar que qualquer outro tipo possa ser usado.</span><span class="sxs-lookup"><span data-stu-id="f1316-208">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="f1316-209">Em particular, é possível definir uma matriz de um tipo definido pelo usuário e incluir um tipo definido pelo usuário como um elemento de um tipo de tupla.</span><span class="sxs-lookup"><span data-stu-id="f1316-209">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="f1316-210">Observação não é possível criar estruturas de tipo recursiva.</span><span class="sxs-lookup"><span data-stu-id="f1316-210">Note is not possible to create recursive type structures.</span></span>
<span data-ttu-id="f1316-211">Ou seja, o tipo que define um tipo definido pelo usuário pode não ser um tipo de tupla que inclua um elemento do tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f1316-211">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="f1316-212">Em geral, os tipos definidos pelo usuário podem não ter dependências cíclicas entre si, portanto, o seguinte conjunto de definições de tipo seria ilegal:</span><span class="sxs-lookup"><span data-stu-id="f1316-212">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```


## <a name="operation-and-function-types"></a><span data-ttu-id="f1316-213">Operação e tipos de função</span><span class="sxs-lookup"><span data-stu-id="f1316-213">Operation and Function Types</span></span>

<span data-ttu-id="f1316-214">O tipo básico para qualquer callable é escrito como `('Tinput => 'Tresult)` ou `('Tinput -> 'Tresult)` , onde ambos `'Tinput` e `'Tresult` são tipos.</span><span class="sxs-lookup"><span data-stu-id="f1316-214">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="f1316-215">Eles são chamados de *assinatura* do callable.</span><span class="sxs-lookup"><span data-stu-id="f1316-215">These are called the *signature* of the callable.</span></span>

<span data-ttu-id="f1316-216">Todos os chamadores de Q # são considerados para pegar um único valor como entrada e retornar um único valor como saída.</span><span class="sxs-lookup"><span data-stu-id="f1316-216">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="f1316-217">Os valores de entrada e saída podem ser tuplas.</span><span class="sxs-lookup"><span data-stu-id="f1316-217">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="f1316-218">Chamadores que não têm nenhum retorno de resultado `Unit` .</span><span class="sxs-lookup"><span data-stu-id="f1316-218">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="f1316-219">Os chamadores que não têm nenhuma entrada usam a tupla vazia como entrada.</span><span class="sxs-lookup"><span data-stu-id="f1316-219">Callables that have no input take the empty tuple as input.</span></span>

> [!NOTE]
> <span data-ttu-id="f1316-220">O primeiro formulário, com `=>` , é usado para operações; o segundo formulário, com `->` , para funções.</span><span class="sxs-lookup"><span data-stu-id="f1316-220">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
> <span data-ttu-id="f1316-221">Por exemplo, `((Qubit, Pauli) => Result)` representa a assinatura de uma possível operação de medição de qubit único.</span><span class="sxs-lookup"><span data-stu-id="f1316-221">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>
<span data-ttu-id="f1316-222">Os tipos de *função* são completamente especificados por sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="f1316-222">*Function* types are completely specified by their signature.</span></span>
<span data-ttu-id="f1316-223">Por exemplo, uma função que computa o seno de um ângulo teria tipo `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="f1316-223">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="f1316-224">*As operações*---, mas não funções---têm determinadas características adicionais que são expressas como parte do tipo de operação.</span><span class="sxs-lookup"><span data-stu-id="f1316-224">*Operations*---but not functions---have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="f1316-225">Essas características incluem informações sobre o que *transmissão functors* a operação dá suporte.</span><span class="sxs-lookup"><span data-stu-id="f1316-225">Such characteristics include information about what *functors* the operation supports.</span></span>
<span data-ttu-id="f1316-226">Por exemplo, se a execução da operação puder ser condicionada no estado de outros qubits, ela deverá dar suporte a `Controlled` functor; se a operação tiver um inverso, ela deverá dar suporte ao `Adjoint` functor.</span><span class="sxs-lookup"><span data-stu-id="f1316-226">For example, if execution of the operation can be conditioned on the state of other qubits, it should support the `Controlled` functor; if the operation has an inverse, it should support the `Adjoint` functor.</span></span> <span data-ttu-id="f1316-227">Transmissão functors e operações são discutidas em detalhes em [operações e funções em Q #](xref:microsoft.quantum.guide.operationsfunctions), mas aqui simplesmente discutimos como isso altera a assinatura da operação.</span><span class="sxs-lookup"><span data-stu-id="f1316-227">Functors and operations are discussed in detail at [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions), but here we simply discuss how this alters the operation signature.</span></span>

<span data-ttu-id="f1316-228">Para exigir suporte para o `Controlled` e/ou `Adjoint` functor em um tipo de operação, precisamos adicionar uma anotação que indica as características correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f1316-228">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="f1316-229">Uma anotação `is Ctl` (por exemplo, `(Qubit => Unit is Ctl)` ) indica que a operação é controlável---ou seja, é uma condição de execução no estado de outro qubit ou qubits.</span><span class="sxs-lookup"><span data-stu-id="f1316-229">An annotation `is Ctl` (e.g. `(Qubit => Unit is Ctl)`) indicates that the operation is controllable---that is, it's execution conditioned on the state of another qubit or qubits.</span></span> <span data-ttu-id="f1316-230">Da mesma forma, `is Adj` indica que a operação tem um erro; ou simplesmente, pode ser "invertida", de forma que a aplicação sucessiva de uma operação e, em seguida, seu adjacente a um estado deixa o estado inalterado.</span><span class="sxs-lookup"><span data-stu-id="f1316-230">Similarly, `is Adj` indicates that the operation has an adjoint; or simply, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="f1316-231">Se quisermos exigir que uma operação desse tipo dê suporte a `Adjoint` e `Controlled` functor, podemos expressar isso como `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="f1316-231">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="f1316-232">Por exemplo, a operação Pauli interna <xref:microsoft.quantum.intrinsic.x> tem o tipo `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="f1316-232">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="f1316-233">Um tipo de operação que não dá suporte a nenhum transmissão functors é especificado por seu tipo de entrada e saída sozinho, sem anotação adicional.</span><span class="sxs-lookup"><span data-stu-id="f1316-233">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="f1316-234">Funções e operações com parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f1316-234">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="f1316-235">Tipos chamáveis podem conter parâmetros de tipo.</span><span class="sxs-lookup"><span data-stu-id="f1316-235">Callable types may contain type parameters.</span></span>
<span data-ttu-id="f1316-236">Os parâmetros de tipo são indicados por um símbolo prefixado por uma aspa simples; por exemplo, `'A` é um parâmetro de tipo legal.</span><span class="sxs-lookup"><span data-stu-id="f1316-236">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="f1316-237">Detalhes sobre a definição de chamadores com parâmetros de tipo são fornecidos nas [operações e funções na página de Q #](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) .</span><span class="sxs-lookup"><span data-stu-id="f1316-237">Details on defining type-parameterized callables are provided on the [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) page.</span></span>

<span data-ttu-id="f1316-238">Um parâmetro de tipo pode aparecer mais de uma vez em uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="f1316-238">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="f1316-239">Por exemplo, uma função que aplica outra função a cada elemento de uma matriz e retorna os resultados coletados teriam assinatura `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="f1316-239">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="f1316-240">Da mesma forma, uma função que retorna a composição de duas operações pode ter assinatura `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="f1316-240">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="f1316-241">Ao invocar um callable-parametrizado de tipo, todos os argumentos que têm o mesmo parâmetro de tipo devem ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="f1316-241">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="f1316-242">O Q # não fornece um mecanismo para restringir os possíveis tipos que podem ser substituídos por um parâmetro de tipo.</span><span class="sxs-lookup"><span data-stu-id="f1316-242">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

## <a name="whats-next"></a><span data-ttu-id="f1316-243">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="f1316-243">What's Next?</span></span>
<span data-ttu-id="f1316-244">Agora que você viu todos os tipos que compõem a linguagem Q #, você pode se encabeçar para [digitar expressões em Q #](xref:microsoft.quantum.guide.expressions) para ver como criar e manipular expressões desses vários tipos.</span><span class="sxs-lookup"><span data-stu-id="f1316-244">Now that you've seen all the types which comprise the Q# language, you can head to [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to see how to create and manipulate expressions of these various types.</span></span>


