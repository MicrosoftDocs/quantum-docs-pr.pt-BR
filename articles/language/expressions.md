---
title: 'Expressões Q #'
description: 'Entenda como especificar, referenciar e combinar constantes, variáveis, operadores, operações e funções como expressões em Q #.'
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: 095be52af27f827f3e52d39a70702f50d6d59ee8
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82683922"
---
# <a name="expressions"></a><span data-ttu-id="5295b-103">Expressões</span><span class="sxs-lookup"><span data-stu-id="5295b-103">Expressions</span></span>

## <a name="grouping"></a><span data-ttu-id="5295b-104">Agrupamento</span><span class="sxs-lookup"><span data-stu-id="5295b-104">Grouping</span></span>

<span data-ttu-id="5295b-105">Dada qualquer expressão, a mesma expressão entre parênteses é uma expressão do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="5295b-105">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="5295b-106">Por exemplo, `(7)` é uma `Int` expressão, `([1,2,3])` é uma expressão do tipo matriz de `Int`s e `((1,2))` é uma expressão com tipo `(Int, Int)`.</span><span class="sxs-lookup"><span data-stu-id="5295b-106">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="5295b-107">A equivalência entre valores simples e tuplas de elemento único descritos no [modelo de tipo](xref:microsoft.quantum.language.type-model#tuple-types) remove a ambiguidade entre `(6)` como um grupo e `(6)` como uma tupla de elemento único.</span><span class="sxs-lookup"><span data-stu-id="5295b-107">The equivalence between simple values and single-element tuples described in [the type model](xref:microsoft.quantum.language.type-model#tuple-types) removes the ambiguity between `(6)` as a group and `(6)` as a single-element tuple.</span></span>

## <a name="symbols"></a><span data-ttu-id="5295b-108">Símbolos</span><span class="sxs-lookup"><span data-stu-id="5295b-108">Symbols</span></span>

<span data-ttu-id="5295b-109">O nome de um símbolo associado ou atribuído a um valor do tipo `'T` é uma expressão do tipo `'T`.</span><span class="sxs-lookup"><span data-stu-id="5295b-109">The name of a symbol bound or assigned to a value of type `'T` is an expression of type `'T`.</span></span>
<span data-ttu-id="5295b-110">Por exemplo, se o símbolo `count` estiver associado ao valor `5`inteiro, `count` será uma expressão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="5295b-110">For instance, if the symbol `count` is bound to the integer value `5`, then `count` is an integer expression.</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="5295b-111">Expressões numéricas</span><span class="sxs-lookup"><span data-stu-id="5295b-111">Numeric Expressions</span></span>

<span data-ttu-id="5295b-112">Expressões numéricas são expressões do `Int`tipo `BigInt`, ou `Double`.</span><span class="sxs-lookup"><span data-stu-id="5295b-112">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="5295b-113">Ou seja, eles são números inteiros ou de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="5295b-113">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="5295b-114">`Int`os literais em Q # são idênticos aos literais inteiros em C#, exceto pelo fato de que nenhum "l" ou "L" à direita é necessário (ou permitido).</span><span class="sxs-lookup"><span data-stu-id="5295b-114">`Int` literals in Q# are identical to integer literals in C#, except that no trailing "l" or "L" is required (or allowed).</span></span>
<span data-ttu-id="5295b-115">Os inteiros hexadecimais e binários têm suporte com um prefixo "0x" e "0B", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5295b-115">Hexadecimal and binary integers are supported with a "0x" and "0b" prefix respectively.</span></span>

<span data-ttu-id="5295b-116">`BigInt`os literais em Q # são idênticos às cadeias de caracteres inteiros grandes no .NET, com um "l" ou "L" à direita.</span><span class="sxs-lookup"><span data-stu-id="5295b-116">`BigInt` literals in Q# are identical to big integer strings in .NET, with a trailing "l" or "L".</span></span>
<span data-ttu-id="5295b-117">Há suporte para inteiros grandes hexadecimais com um prefixo "0x".</span><span class="sxs-lookup"><span data-stu-id="5295b-117">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="5295b-118">Portanto, veja a seguir todos os usos válidos `BigInt` de literais:</span><span class="sxs-lookup"><span data-stu-id="5295b-118">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="5295b-119">`Double`os literais em Q # são idênticos aos literais duplos em C#, exceto pelo fato de que nenhum "d" ou "D" à direita é necessário (ou permitido).</span><span class="sxs-lookup"><span data-stu-id="5295b-119">`Double` literals in Q# are identical to double literals in C#, except that no trailing "d" or "D" is required (or allowed).</span></span>

<span data-ttu-id="5295b-120">Dada uma expressão de matriz de qualquer tipo de elemento `Int` , uma expressão pode ser formada usando a `Length` função interna, com a expressão de matriz entre parênteses `(` e `)`.</span><span class="sxs-lookup"><span data-stu-id="5295b-120">Given an array expression of any element type, an `Int` expression may be formed using the `Length` built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="5295b-121">Por exemplo, se `a` estiver associado a uma matriz, `Length(a)` será uma expressão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="5295b-121">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="5295b-122">Se `b` é uma matriz de matrizes de inteiros, `Int[][]`, `Length(b)` é o número de submatrizes em `b`e `Length(b[1])` é o número de inteiros na segunda submatriz no. `b`</span><span class="sxs-lookup"><span data-stu-id="5295b-122">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="5295b-123">Dadas duas expressões numéricas do mesmo tipo `+`, os operadores `-` `*`binários,, e `/` podem ser usados para formar uma nova expressão numérica.</span><span class="sxs-lookup"><span data-stu-id="5295b-123">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="5295b-124">O tipo da nova expressão será o mesmo que os tipos das expressões constituintes.</span><span class="sxs-lookup"><span data-stu-id="5295b-124">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="5295b-125">Dadas duas expressões de inteiro, o operador `^` binário (potência) pode ser usado para formar uma nova expressão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="5295b-125">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="5295b-126">Da mesma `^` forma, pode ser usado com duas expressões duplas para formar uma nova expressão Double.</span><span class="sxs-lookup"><span data-stu-id="5295b-126">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="5295b-127">Por fim `^` , pode ser usado com um inteiro grande à esquerda e um inteiro à direita para formar uma nova expressão de inteiro grande.</span><span class="sxs-lookup"><span data-stu-id="5295b-127">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="5295b-128">Nesse caso, o segundo parâmetro deve caber em 32 bits; caso contrário, um erro de tempo de execução será gerado.</span><span class="sxs-lookup"><span data-stu-id="5295b-128">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="5295b-129">Dadas duas expressões de inteiro ou grandes inteiros, um novo inteiro ou uma expressão de inteiro grande pode ser `%` formada usando os `&&&` operadores (módulo), `|||` (bit e), ( `^^^` OR-bit or) ou (XOR).</span><span class="sxs-lookup"><span data-stu-id="5295b-129">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="5295b-130">Dado um inteiro ou uma expressão de inteiro grande à esquerda e uma expressão de inteiro à direita, os `<<<` operadores (deslocamento aritmético à esquerda) `>>>` ou (deslocamento aritmético à direita) podem ser usados para criar uma nova expressão com o mesmo tipo que a expressão esquerda.</span><span class="sxs-lookup"><span data-stu-id="5295b-130">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="5295b-131">O segundo parâmetro (o valor de deslocamento) para a operação de deslocamento deve ser maior ou igual a zero; o comportamento para valores de deslocamento negativos é indefinido.</span><span class="sxs-lookup"><span data-stu-id="5295b-131">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="5295b-132">O valor de deslocamento para uma das operações de deslocamento também deve se ajustar a 32 bits; caso contrário, um erro de tempo de execução será gerado.</span><span class="sxs-lookup"><span data-stu-id="5295b-132">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="5295b-133">Se o número a ser deslocado for um inteiro, o valor de deslocamento será interpretado `mod 64`; ou seja, uma mudança de 1 e uma mudança de 65 têm o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="5295b-133">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="5295b-134">Para os valores inteiros e inteiros grandes, as turnos são aritméticas.</span><span class="sxs-lookup"><span data-stu-id="5295b-134">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="5295b-135">A mudança de um valor negativo para a esquerda ou direita resultará em um número negativo.</span><span class="sxs-lookup"><span data-stu-id="5295b-135">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="5295b-136">Ou seja, mudar uma etapa para a esquerda ou para a direita é exatamente o mesmo que multiplicar ou dividir por 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5295b-136">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="5295b-137">Divisão de inteiros e módulo de inteiro seguem o mesmo comportamento para números negativos em C#.</span><span class="sxs-lookup"><span data-stu-id="5295b-137">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="5295b-138">Ou seja, `a % b` sempre terá o mesmo sinal `a`de e `b * (a / b) + a % b` sempre será igual. `a`</span><span class="sxs-lookup"><span data-stu-id="5295b-138">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="5295b-139">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="5295b-139">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="5295b-140">5</span><span class="sxs-lookup"><span data-stu-id="5295b-140">5</span></span> | <span data-ttu-id="5295b-141">2</span><span class="sxs-lookup"><span data-stu-id="5295b-141">2</span></span> | <span data-ttu-id="5295b-142">2</span><span class="sxs-lookup"><span data-stu-id="5295b-142">2</span></span> | <span data-ttu-id="5295b-143">1</span><span class="sxs-lookup"><span data-stu-id="5295b-143">1</span></span>
 <span data-ttu-id="5295b-144">5</span><span class="sxs-lookup"><span data-stu-id="5295b-144">5</span></span> | <span data-ttu-id="5295b-145">-2</span><span class="sxs-lookup"><span data-stu-id="5295b-145">-2</span></span> | <span data-ttu-id="5295b-146">-2</span><span class="sxs-lookup"><span data-stu-id="5295b-146">-2</span></span> | <span data-ttu-id="5295b-147">1</span><span class="sxs-lookup"><span data-stu-id="5295b-147">1</span></span>
 <span data-ttu-id="5295b-148">-5</span><span class="sxs-lookup"><span data-stu-id="5295b-148">-5</span></span> | <span data-ttu-id="5295b-149">2</span><span class="sxs-lookup"><span data-stu-id="5295b-149">2</span></span> | <span data-ttu-id="5295b-150">-2</span><span class="sxs-lookup"><span data-stu-id="5295b-150">-2</span></span> | <span data-ttu-id="5295b-151">-1</span><span class="sxs-lookup"><span data-stu-id="5295b-151">-1</span></span>
 <span data-ttu-id="5295b-152">-5</span><span class="sxs-lookup"><span data-stu-id="5295b-152">-5</span></span> | <span data-ttu-id="5295b-153">-2</span><span class="sxs-lookup"><span data-stu-id="5295b-153">-2</span></span> | <span data-ttu-id="5295b-154">2</span><span class="sxs-lookup"><span data-stu-id="5295b-154">2</span></span> | <span data-ttu-id="5295b-155">-1</span><span class="sxs-lookup"><span data-stu-id="5295b-155">-1</span></span>

<span data-ttu-id="5295b-156">Divisão de inteiro grande e módulo funciona da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="5295b-156">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="5295b-157">Dada qualquer expressão numérica, uma nova expressão pode ser formada usando `-` o operador unário.</span><span class="sxs-lookup"><span data-stu-id="5295b-157">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="5295b-158">A nova expressão será o mesmo tipo da expressão constituinte.</span><span class="sxs-lookup"><span data-stu-id="5295b-158">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="5295b-159">Devido a qualquer inteiro ou expressão de inteiro grande, uma nova expressão do mesmo tipo pode ser formada `~~~` usando o operador unário (complemento de bits).</span><span class="sxs-lookup"><span data-stu-id="5295b-159">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="5295b-160">Expressões boolianas</span><span class="sxs-lookup"><span data-stu-id="5295b-160">Boolean Expressions</span></span>

<span data-ttu-id="5295b-161">Os dois `Bool` valores literais `true` são `false`e.</span><span class="sxs-lookup"><span data-stu-id="5295b-161">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="5295b-162">Dadas as duas expressões do mesmo tipo primitivo, os `==` operadores binários e `!=` podem ser usados para construir uma `Bool` expressão.</span><span class="sxs-lookup"><span data-stu-id="5295b-162">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="5295b-163">A expressão será true se as duas expressões forem iguais e false se não.</span><span class="sxs-lookup"><span data-stu-id="5295b-163">The expression will be true if the two expressions are equal, and false if not.</span></span>

<span data-ttu-id="5295b-164">Os valores de tipos definidos pelo usuário não podem ser comparados, apenas seus valores não encapsulados podem ser comparados.</span><span class="sxs-lookup"><span data-stu-id="5295b-164">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="5295b-165">Por exemplo, usando o operador `!` "sem encapsulamento" (explicado na [página modelo do tipo Q #](xref:microsoft.quantum.language.type-model#user-defined-types)),</span><span class="sxs-lookup"><span data-stu-id="5295b-165">For example, using the "unwrap" operator `!` (explained in the [Q# type model page](xref:microsoft.quantum.language.type-model#user-defined-types)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="5295b-166">A comparação de `Qubit` igualdade para valores é igualdade de identidade; ou seja, se as duas expressões identificam o mesmo qubit.</span><span class="sxs-lookup"><span data-stu-id="5295b-166">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="5295b-167">O estado dos dois qubits não são comparados, acessados, medidos ou modificados por essa comparação.</span><span class="sxs-lookup"><span data-stu-id="5295b-167">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="5295b-168">A comparação de `Double` igualdade para valores pode ser enganosa devido a efeitos de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="5295b-168">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="5295b-169">Por exemplo, `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="5295b-169">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="5295b-170">Dadas quaisquer duas expressões numéricas, os operadores `>` `<` `>=`binários,, `<=` e podem ser usados para construir uma nova expressão booliana que seja verdadeira se a primeira expressão for maior que, menor que, maior ou igual ou menor ou igual à segunda expressão.</span><span class="sxs-lookup"><span data-stu-id="5295b-170">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="5295b-171">Dadas quaisquer duas expressões booleanas, os `and` operadores `or` binários e podem ser usados para construir uma nova expressão booliana que seja verdadeira se ambos (resp. ou ambos) as duas expressões forem true.</span><span class="sxs-lookup"><span data-stu-id="5295b-171">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="5295b-172">Dada qualquer expressão booliana, `not` o operador unário pode ser usado para construir uma nova expressão booliana que seja verdadeira se a expressão constituinte for falsa.</span><span class="sxs-lookup"><span data-stu-id="5295b-172">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="5295b-173">Expressões de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="5295b-173">String Expressions</span></span>

<span data-ttu-id="5295b-174">Q # permite que as cadeias de caracteres `fail` sejam usadas na `Log` instrução e na função padrão.</span><span class="sxs-lookup"><span data-stu-id="5295b-174">Q# allows strings to be used in the `fail` statement and the `Log` standard function.</span></span>

<span data-ttu-id="5295b-175">Cadeias de caracteres em Q # são literais ou cadeias de caracteres interpoladas.</span><span class="sxs-lookup"><span data-stu-id="5295b-175">Strings in Q# are either literals or interpolated strings.</span></span>
<span data-ttu-id="5295b-176">Literais de cadeia de caracteres são semelhantes a literais de cadeia de caracteres simples na maioria dos idiomas: uma sequência de `"`caracteres Unicode entre aspas duplas,.</span><span class="sxs-lookup"><span data-stu-id="5295b-176">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="5295b-177">Dentro de uma cadeia de caracteres, `\` o caractere de barra invertida pode ser usado para escapar de um caractere de aspas duplas e para inserir `\n`uma linha nova como, `\r`um retorno de carro como `\t`e uma tabulação como.</span><span class="sxs-lookup"><span data-stu-id="5295b-177">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="5295b-178">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5295b-178">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```

<span data-ttu-id="5295b-179">A sintaxe de Q # para interpolações de cadeia de caracteres é um subconjunto da sintaxe C# 7,0; Q # não oferece suporte a cadeias de caracteres interpoladas (várias linhas) textuais.</span><span class="sxs-lookup"><span data-stu-id="5295b-179">The Q# syntax for string interpolations is a subset of the C# 7.0 syntax; Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="5295b-180">Consulte [*cadeias de caracteres interpoladas*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) para a sintaxe C#.</span><span class="sxs-lookup"><span data-stu-id="5295b-180">See [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) for the C# syntax.</span></span>

<span data-ttu-id="5295b-181">As expressões dentro de uma cadeia de caracteres interpolada seguem a sintaxe Q #, e não a sintaxe C#.</span><span class="sxs-lookup"><span data-stu-id="5295b-181">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>
<span data-ttu-id="5295b-182">Qualquer expressão Q # válida pode aparecer em uma cadeia de caracteres interpolada.</span><span class="sxs-lookup"><span data-stu-id="5295b-182">Any valid Q# expression may appear in an interpolated string.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="5295b-183">Expressões qubit</span><span class="sxs-lookup"><span data-stu-id="5295b-183">Qubit Expressions</span></span>

<span data-ttu-id="5295b-184">As únicas `Qubit` expressões são símbolos que são associados a `Qubit` valores ou elementos de matriz `Qubit` de matrizes.</span><span class="sxs-lookup"><span data-stu-id="5295b-184">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="5295b-185">Não há `Qubit` literais.</span><span class="sxs-lookup"><span data-stu-id="5295b-185">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="5295b-186">Expressões Pauli</span><span class="sxs-lookup"><span data-stu-id="5295b-186">Pauli Expressions</span></span>

<span data-ttu-id="5295b-187">Os quatro `Pauli` valores, `PauliI`, `PauliX` `PauliY`, e `PauliZ`, são expressões válidas `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="5295b-187">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="5295b-188">Além disso, as únicas `Pauli` expressões são símbolos associados a `Pauli` valores ou elementos de matriz de `Pauli` matrizes.</span><span class="sxs-lookup"><span data-stu-id="5295b-188">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="5295b-189">Expressões de resultado</span><span class="sxs-lookup"><span data-stu-id="5295b-189">Result Expressions</span></span>

<span data-ttu-id="5295b-190">Os dois `Result` valores, `One` e `Zero`, são expressões `Result` válidas.</span><span class="sxs-lookup"><span data-stu-id="5295b-190">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="5295b-191">Além disso, as únicas `Result` expressões são símbolos associados a `Result` valores ou elementos de matriz de `Result` matrizes.</span><span class="sxs-lookup"><span data-stu-id="5295b-191">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="5295b-192">Em particular, observe que `One` não é o mesmo que o inteiro `1`, e não há nenhuma conversão direta entre eles.</span><span class="sxs-lookup"><span data-stu-id="5295b-192">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="5295b-193">O mesmo é verdadeiro para `Zero` e `0`.</span><span class="sxs-lookup"><span data-stu-id="5295b-193">The same is true for `Zero` and `0`.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="5295b-194">Expressões de intervalo</span><span class="sxs-lookup"><span data-stu-id="5295b-194">Range Expressions</span></span>

<span data-ttu-id="5295b-195">Dadas as três `Int` expressões `start`, `step`e `stop`, `start .. step .. stop` é uma expressão de intervalo cujo primeiro elemento é `start`, o segundo elemento `start+step`é, o terceiro `start+step+step`elemento é, etc. `stop` , até que seja passado.</span><span class="sxs-lookup"><span data-stu-id="5295b-195">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="5295b-196">Um intervalo pode estar vazio se, por exemplo, `step` for positivo e `stop < start`.</span><span class="sxs-lookup"><span data-stu-id="5295b-196">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="5295b-197">O último elemento do intervalo `stop` será se a diferença entre `start` e `stop` for um múltiplo integral de; `step` ou seja, o intervalo é inclusivo em ambas as extremidades.</span><span class="sxs-lookup"><span data-stu-id="5295b-197">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="5295b-198">Dadas as duas `Int` expressões `start` e `stop`, `start .. stop` é uma expressão de intervalo igual a `start .. 1 .. stop`.</span><span class="sxs-lookup"><span data-stu-id="5295b-198">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="5295b-199">Observe que o implícito `step` é + 1, mesmo se `stop` for menor que `start`; Nesse caso, o intervalo está vazio.</span><span class="sxs-lookup"><span data-stu-id="5295b-199">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="5295b-200">Alguns intervalos de exemplo são:</span><span class="sxs-lookup"><span data-stu-id="5295b-200">Some example ranges are:</span></span>

- <span data-ttu-id="5295b-201">`1..3`é o intervalo 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="5295b-201">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="5295b-202">`2..2..5`é o intervalo de 2, 4.</span><span class="sxs-lookup"><span data-stu-id="5295b-202">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="5295b-203">`2..2..6`é o intervalo de 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="5295b-203">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="5295b-204">`6..-2..2`é o intervalo de 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="5295b-204">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="5295b-205">`2..1`é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="5295b-205">`2..1` is the empty range.</span></span>
- <span data-ttu-id="5295b-206">`2..6..7`é o intervalo 2.</span><span class="sxs-lookup"><span data-stu-id="5295b-206">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="5295b-207">`2..2..1`é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="5295b-207">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="5295b-208">`1..-1..2`é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="5295b-208">`1..-1..2` is the empty range.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="5295b-209">Expressões que podem ser chamadas</span><span class="sxs-lookup"><span data-stu-id="5295b-209">Callable Expressions</span></span>

<span data-ttu-id="5295b-210">Um literal que pôde ser chamado é o nome de uma operação ou função definida no escopo de compilação.</span><span class="sxs-lookup"><span data-stu-id="5295b-210">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="5295b-211">Por exemplo, `X` é um literal de operação que se refere à operação `X` de biblioteca padrão `Message` e é um literal de função que se refere à `Message` função de biblioteca padrão.</span><span class="sxs-lookup"><span data-stu-id="5295b-211">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="5295b-212">Se uma operação oferecer suporte `Adjoint` a functor, `Adjoint op` será uma expressão de operação.</span><span class="sxs-lookup"><span data-stu-id="5295b-212">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="5295b-213">Da mesma forma, se a operação `Controlled` oferecer suporte a `Controlled op` functor, será uma expressão de operação.</span><span class="sxs-lookup"><span data-stu-id="5295b-213">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="5295b-214">Os tipos dessas expressões são especificados em [transmissão functors](xref:microsoft.quantum.language.type-model#functors).</span><span class="sxs-lookup"><span data-stu-id="5295b-214">The types of these expressions are specified in [Functors](xref:microsoft.quantum.language.type-model#functors).</span></span>

<span data-ttu-id="5295b-215">Transmissão functors (`Adjoint` e `Controlled`) associam-se mais de todos os outros operadores, exceto para o `!` operador de desencapsulamento `[]`e a indexação de matriz com.</span><span class="sxs-lookup"><span data-stu-id="5295b-215">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[]`.</span></span>
<span data-ttu-id="5295b-216">Portanto, as seguintes são todas legais, supondo que as operações suportam o transmissão functors usado:</span><span class="sxs-lookup"><span data-stu-id="5295b-216">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

<span data-ttu-id="5295b-217">Um literal resgatável pode ser usado como um valor, digamos para atribuir a uma variável ou passar para outro callable.</span><span class="sxs-lookup"><span data-stu-id="5295b-217">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="5295b-218">Nesse caso, se o callable tiver parâmetros de tipo, eles deverão ser fornecidos como parte do valor que pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="5295b-218">In this case, if the callable has type parameters, they must be provided as part of the callable value.</span></span>
<span data-ttu-id="5295b-219">Um valor callable não pode ter nenhum parâmetro de tipo não especificado.</span><span class="sxs-lookup"><span data-stu-id="5295b-219">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="5295b-220">Por exemplo, se `Fun` é uma função com assinatura `'T1->Unit`:</span><span class="sxs-lookup"><span data-stu-id="5295b-220">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomeOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="5295b-221">Expressões de invocação que podem ser chamadas</span><span class="sxs-lookup"><span data-stu-id="5295b-221">Callable Invocation Expressions</span></span>

<span data-ttu-id="5295b-222">Dada uma expressão resgatável (operação ou função) e uma expressão de tupla do tipo de entrada da assinatura do callable, uma expressão de invocação pode ser formada acrescentando-se a expressão de tupla à expressão que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5295b-222">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="5295b-223">O tipo da expressão de invocação é o tipo de saída da assinatura do callable.</span><span class="sxs-lookup"><span data-stu-id="5295b-223">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="5295b-224">Por exemplo, se `Op` for uma operação com assinatura `((Int, Qubit) => Double)`, `Op(3, qubit1)` é uma expressão do tipo `Double`.</span><span class="sxs-lookup"><span data-stu-id="5295b-224">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="5295b-225">Da mesma forma `Sin` , se é uma função `(Double -> Double)`com `Sin(0.1)` assinatura, é uma expressão `Double`do tipo.</span><span class="sxs-lookup"><span data-stu-id="5295b-225">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="5295b-226">Por fim, `Builder` se for uma função com `(Int -> (Int -> Int))`assinatura, `Builder(3)` será uma função de em para int.</span><span class="sxs-lookup"><span data-stu-id="5295b-226">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="5295b-227">Invocar o resultado de uma expressão com valor callable requer um par extra de parênteses em volta da expressão callable.</span><span class="sxs-lookup"><span data-stu-id="5295b-227">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="5295b-228">Portanto, para invocar o resultado da `Builder` chamada do parágrafo anterior, a sintaxe correta é:</span><span class="sxs-lookup"><span data-stu-id="5295b-228">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="5295b-229">Ao invocar um callable com parâmetros de tipo, os parâmetros do tipo real podem ser especificados entre colchetes `<` angulares e `>` após a expressão que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5295b-229">When invoking a type-parameterized callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="5295b-230">Isso geralmente é desnecessário, pois o compilador Q # inferirá os tipos reais.</span><span class="sxs-lookup"><span data-stu-id="5295b-230">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="5295b-231">Ele é necessário para o aplicativo parcial (veja abaixo) se um argumento com parâmetros de tipo for deixado não especificado.</span><span class="sxs-lookup"><span data-stu-id="5295b-231">It is required for partial application (see below) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="5295b-232">Às vezes, também é útil ao passar operações com functor diferentes para um callable.</span><span class="sxs-lookup"><span data-stu-id="5295b-232">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="5295b-233">Por exemplo, se `Func` tem assinatura `('T1, 'T2, 'T1) -> 'T2` `Op1` `Op2` e tem `(Qubit[] => Unit is Adj)`assinatura e `Op3` tem assinatura `(Qubit[] => Unit)`, para invocar `Func` com `Op1` como o primeiro argumento, `Op2` como o segundo, e `Op3` como o terceiro:</span><span class="sxs-lookup"><span data-stu-id="5295b-233">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="5295b-234">A especificação de tipo é necessária `Op3` porque `Op1` e tem tipos diferentes, portanto, o compilador tratará isso como ambíguo sem a especificação.</span><span class="sxs-lookup"><span data-stu-id="5295b-234">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>

### <a name="partial-application"></a><span data-ttu-id="5295b-235">Aplicativo parcial</span><span class="sxs-lookup"><span data-stu-id="5295b-235">Partial Application</span></span>

<span data-ttu-id="5295b-236">Dada uma expressão resgatável, um novo callable pode ser criado fornecendo um subconjunto dos argumentos para o callable.</span><span class="sxs-lookup"><span data-stu-id="5295b-236">Given a callable expression, a new callable may be created by providing a subset of the arguments to the callable.</span></span>
<span data-ttu-id="5295b-237">Isso é chamado de _aplicativo parcial_.</span><span class="sxs-lookup"><span data-stu-id="5295b-237">This is called _partial application_.</span></span>

<span data-ttu-id="5295b-238">Em Q #, um resgatável aplicado parcialmente é expresso escrevendo uma expressão de invocação normal, mas usando um sublinhado, `_`, para os argumentos não especificados.</span><span class="sxs-lookup"><span data-stu-id="5295b-238">In Q#, a partially applied callable is expressed by writing a normal invocation expression, but using an underscore, `_`, for the unspecified arguments.</span></span>
<span data-ttu-id="5295b-239">O callable que resultau tem o mesmo tipo de resultado que o callable de base, e as mesmas especializações para operações.</span><span class="sxs-lookup"><span data-stu-id="5295b-239">The resulting callable has the same result type as the base callable, and the same specializations for operations.</span></span>
<span data-ttu-id="5295b-240">O tipo de entrada do aplicativo parcial é simplesmente o tipo original com os argumentos especificados removidos.</span><span class="sxs-lookup"><span data-stu-id="5295b-240">The input type of the partial application is simply the original type with the specified arguments removed.</span></span>

<span data-ttu-id="5295b-241">Se uma variável mutável for passada como um argumento especificado ao criar um aplicativo parcial, o valor atual da variável será usado.</span><span class="sxs-lookup"><span data-stu-id="5295b-241">If a mutable variable is passed as a specified argument when creating a partial application, the current value of the variable is used.</span></span>
<span data-ttu-id="5295b-242">Alterar o valor da variável subsequentemente não afetará o aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="5295b-242">Changing the value of the variable afterward will not impact the partial application.</span></span>

<span data-ttu-id="5295b-243">Por exemplo, se `Op` tiver o `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`tipo:</span><span class="sxs-lookup"><span data-stu-id="5295b-243">For example, if `Op` has type `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`:</span></span>

- <span data-ttu-id="5295b-244">`Op(5,(_,_))`tem o `(((Qubit,Qubit), Double) => Unit is Adj)`tipo e, portanto `Op(5,_)`, tem.</span><span class="sxs-lookup"><span data-stu-id="5295b-244">`Op(5,(_,_))` has type `(((Qubit,Qubit), Double) => Unit is Adj)`, and so has `Op(5,_)`.</span></span>
- <span data-ttu-id="5295b-245">`Op(_,(_,1.0))` tem o tipo `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span><span class="sxs-lookup"><span data-stu-id="5295b-245">`Op(_,(_,1.0))` has type `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span></span>
- <span data-ttu-id="5295b-246">`Op(_,((q1,q2),_))` tem o tipo `((Int,Double) => Unit is Adj)`.</span><span class="sxs-lookup"><span data-stu-id="5295b-246">`Op(_,((q1,q2),_))` has type `((Int,Double) => Unit is Adj)`.</span></span>
   <span data-ttu-id="5295b-247">Observe que aplicamos a equivalência de tupla singleton aqui.</span><span class="sxs-lookup"><span data-stu-id="5295b-247">Note that we have applied singleton tuple equivalence here.</span></span>

<span data-ttu-id="5295b-248">Se o chamado parcialmente aplicado tiver parâmetros de tipo que não podem ser inferidos pelo compilador, eles deverão ser fornecidos no site de invocação.</span><span class="sxs-lookup"><span data-stu-id="5295b-248">If the partially-applied callable has type parameters that cannot be inferred by the compiler, they must be provided at the invocation site.</span></span>
<span data-ttu-id="5295b-249">O aplicativo parcial não pode ter nenhum parâmetro de tipo não especificado.</span><span class="sxs-lookup"><span data-stu-id="5295b-249">The partial application cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="5295b-250">Por exemplo, se `Op` tiver o `(('T1, Qubit, 'T1) => Unit : Adjoint)`tipo:</span><span class="sxs-lookup"><span data-stu-id="5295b-250">For example, if `Op` has type `(('T1, Qubit, 'T1) => Unit : Adjoint)`:</span></span>

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a><span data-ttu-id="5295b-251">Recursão</span><span class="sxs-lookup"><span data-stu-id="5295b-251">Recursion</span></span>

<span data-ttu-id="5295b-252">Os chamadores do Q # podem ser recursivos direta ou indiretamente.</span><span class="sxs-lookup"><span data-stu-id="5295b-252">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="5295b-253">Ou seja, uma operação ou função pode chamar a si mesma ou chamar outro callable que chama direta ou indiretamente a operação que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5295b-253">That is, an operation or function may call itself, or it may call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="5295b-254">No entanto, há dois comentários importantes sobre o uso da recursão:</span><span class="sxs-lookup"><span data-stu-id="5295b-254">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="5295b-255">O uso da recursão nas operações provavelmente interfere em determinadas otimizações.</span><span class="sxs-lookup"><span data-stu-id="5295b-255">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="5295b-256">Isso pode ter um impacto significativo no tempo de execução do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="5295b-256">This may have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="5295b-257">Ao executar em um dispositivo Quantum real, o espaço de pilha pode ser limitado e, portanto, a recursão profunda pode levar a um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5295b-257">When executing on an actual quantum device, stack space may be limited, and so deep recursion may lead to a runtime error.</span></span>
  <span data-ttu-id="5295b-258">Em particular, o compilador e o tempo de execução do Q # não identificam e otimizam a recursão da cauda.</span><span class="sxs-lookup"><span data-stu-id="5295b-258">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="5295b-259">Expressões de tupla</span><span class="sxs-lookup"><span data-stu-id="5295b-259">Tuple Expressions</span></span>

<span data-ttu-id="5295b-260">Um literal de tupla é uma sequência de expressões de elemento do tipo apropriado, separados por vírgulas, colocadas `(` em `)`e.</span><span class="sxs-lookup"><span data-stu-id="5295b-260">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="5295b-261">Por exemplo, `(1, One)` é uma `(Int, Result)` expressão.</span><span class="sxs-lookup"><span data-stu-id="5295b-261">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="5295b-262">Além de literais, as únicas expressões de tupla são símbolos associados a valores de tupla, elementos de matriz de matrizes de tupla e invocações que retornam tuplas.</span><span class="sxs-lookup"><span data-stu-id="5295b-262">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="5295b-263">Expressões de tipo definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5295b-263">User-Defined Type Expressions</span></span>

<span data-ttu-id="5295b-264">Um literal de um tipo definido pelo usuário consiste no nome do tipo seguido por um literal de tupla do tipo de tupla base do tipo.</span><span class="sxs-lookup"><span data-stu-id="5295b-264">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="5295b-265">Por exemplo, se `IntPair` for um tipo definido pelo usuário com base `(Int, Int)`em, `IntPair(2,3)` seria um literal válido desse tipo.</span><span class="sxs-lookup"><span data-stu-id="5295b-265">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2,3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="5295b-266">Além de literais, as únicas expressões de um tipo definido pelo usuário são símbolos que são associados a valores desse tipo, elementos da matriz de matrizes desse tipo e invocações que retornam esse tipo.</span><span class="sxs-lookup"><span data-stu-id="5295b-266">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="5295b-267">Desencapsular expressões</span><span class="sxs-lookup"><span data-stu-id="5295b-267">Unwrap Expressions</span></span>

<span data-ttu-id="5295b-268">Em Q #, o operador de desencapsulamento é um ponto de exclamação `!`à direita.</span><span class="sxs-lookup"><span data-stu-id="5295b-268">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="5295b-269">Por exemplo, se `IntPair` é um tipo definido pelo usuário com o tipo `(Int, Int)`subjacente e `s` era uma variável com valor `IntPair(2,3)`, `s!` seria `(2,3)`.</span><span class="sxs-lookup"><span data-stu-id="5295b-269">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2,3)`, then `s!` would be `(2,3)`.</span></span>

<span data-ttu-id="5295b-270">Para tipos definidos pelo usuário definidos em termos de outros tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5295b-270">For user-defined types defined in terms of other user-defined types.</span></span> <span data-ttu-id="5295b-271">o operador de desencapsulamento pode ser repetido; por exemplo, `s!!` indica o valor duplo não encapsulado de `s`.</span><span class="sxs-lookup"><span data-stu-id="5295b-271">the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="5295b-272">Portanto, se `WrappedPair` for um tipo definido pelo usuário com o tipo `IntPair`subjacente, `t` e for uma variável com `WrappedPair(IntPair(1,2))`valor, `t!!` será `(1,2)`.</span><span class="sxs-lookup"><span data-stu-id="5295b-272">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="5295b-273">O `!` operador tem precedência maior do que todos os outros `[]` operadores diferentes de para indexação e divisão de matriz.</span><span class="sxs-lookup"><span data-stu-id="5295b-273">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="5295b-274">`!`e `[]` associar à posição; ou seja, `a[i]![3]` deve ser lido como `((a[i])!)[3]`: Pegue o `i`elemento ' th ' `a`, desenvolva-o e, em seguida, obtenha o terceiro elemento do valor não encapsulado (que deve ser uma matriz).</span><span class="sxs-lookup"><span data-stu-id="5295b-274">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="5295b-275">A precedência do `!` operador tem um impacto que pode não ser óbvio.</span><span class="sxs-lookup"><span data-stu-id="5295b-275">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="5295b-276">Se uma função ou operação retorna um valor que, em seguida, é desencapsulada, a função ou a chamada de operação deve ser colocada entre parênteses para que a tupla de argumento seja associada à chamada em vez de ser desencapsulada.</span><span class="sxs-lookup"><span data-stu-id="5295b-276">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="5295b-277">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="5295b-277">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="5295b-278">Expressões de matriz</span><span class="sxs-lookup"><span data-stu-id="5295b-278">Array Expressions</span></span>

<span data-ttu-id="5295b-279">Um literal de matriz é uma sequência de uma ou mais expressões de elemento, separadas por vírgulas, `[` colocadas `]`em e.</span><span class="sxs-lookup"><span data-stu-id="5295b-279">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="5295b-280">Todos os elementos devem ser compatíveis com o mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="5295b-280">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="5295b-281">Se o tipo de elemento comum for uma operação ou tipo de função, todos os elementos deverão ter os mesmos tipos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="5295b-281">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="5295b-282">O tipo de elemento da matriz dará suporte a qualquer transmissão functors que tenha suporte de todos os elementos.</span><span class="sxs-lookup"><span data-stu-id="5295b-282">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="5295b-283">Por exemplo, se `Op1`, `Op2`, e `Op3` todos forem `Qubit[] => Unit`, mas `Op1` o `Adjoint`oferecer `Op2` suporte `Controlled`a, `Op3` o oferece suporte a, e dá suporte a ambos:</span><span class="sxs-lookup"><span data-stu-id="5295b-283">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="5295b-284">`[Op1, Op2]`é uma matriz de `(Qubit[] => Unit)` operações.</span><span class="sxs-lookup"><span data-stu-id="5295b-284">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="5295b-285">`[Op1, Op3]`é uma matriz de `(Qubit[] => Unit is Adj)` operações.</span><span class="sxs-lookup"><span data-stu-id="5295b-285">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="5295b-286">`[Op2, Op3]`é uma matriz de `(Qubit[] => Unit is Ctl)` operações.</span><span class="sxs-lookup"><span data-stu-id="5295b-286">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="5295b-287">Literais de matriz vazios `[]`,, não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="5295b-287">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="5295b-288">Em vez `new ★[0]`disso, `★` o uso de, onde é o espaço reservado para um tipo adequado, permite criar a matriz desejada de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="5295b-288">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>

<span data-ttu-id="5295b-289">Dadas duas matrizes do mesmo tipo, o operador `+` binário pode ser usado para formar uma nova matriz que é a concatenação das duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="5295b-289">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="5295b-290">Por exemplo, `[1,2,3] + [4,5,6]` é `[1,2,3,4,5,6]`.</span><span class="sxs-lookup"><span data-stu-id="5295b-290">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="5295b-291">Criação de matriz</span><span class="sxs-lookup"><span data-stu-id="5295b-291">Array Creation</span></span>

<span data-ttu-id="5295b-292">Dado um tipo e uma `Int` expressão, o `new` operador pode ser usado para alocar uma nova matriz do tamanho determinado.</span><span class="sxs-lookup"><span data-stu-id="5295b-292">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="5295b-293">Por exemplo, `new Int[i+1]` alocaria uma nova `Int` matriz com `i+1` elementos.</span><span class="sxs-lookup"><span data-stu-id="5295b-293">For instance, `new Int[i+1]` would allocate a new `Int` array with `i+1` elements.</span></span>

<span data-ttu-id="5295b-294">Os elementos de uma nova matriz são inicializados para um valor padrão dependente de tipo.</span><span class="sxs-lookup"><span data-stu-id="5295b-294">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="5295b-295">Na maioria dos casos, essa é uma variação de zero.</span><span class="sxs-lookup"><span data-stu-id="5295b-295">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="5295b-296">Para qubits e callableies, que são referências a entidades, não há nenhum valor padrão razoável.</span><span class="sxs-lookup"><span data-stu-id="5295b-296">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="5295b-297">Portanto, para esses tipos, o padrão é uma referência inválida que não pode ser usada sem causar um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5295b-297">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="5295b-298">Isso é semelhante a uma referência nula em linguagens como C# ou Java.</span><span class="sxs-lookup"><span data-stu-id="5295b-298">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="5295b-299">As matrizes que contêm qubits ou callables devem ser inicializadas corretamente com valores não padrão antes que seus elementos possam ser usados com segurança.</span><span class="sxs-lookup"><span data-stu-id="5295b-299">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="5295b-300">Rotinas de inicialização adequadas podem ser <xref:microsoft.quantum.arrays>encontradas em.</span><span class="sxs-lookup"><span data-stu-id="5295b-300">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="5295b-301">Os valores padrão para cada tipo são:</span><span class="sxs-lookup"><span data-stu-id="5295b-301">The default values for each type are:</span></span>

<span data-ttu-id="5295b-302">Type</span><span class="sxs-lookup"><span data-stu-id="5295b-302">Type</span></span> | <span data-ttu-id="5295b-303">Padrão</span><span class="sxs-lookup"><span data-stu-id="5295b-303">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="5295b-304">_qubit inválido_</span><span class="sxs-lookup"><span data-stu-id="5295b-304">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="5295b-305">O intervalo vazio,`1..1..0`</span><span class="sxs-lookup"><span data-stu-id="5295b-305">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="5295b-306">_callable inválido_</span><span class="sxs-lookup"><span data-stu-id="5295b-306">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="5295b-307">Os tipos de tupla são inicializados elemento por elemento.</span><span class="sxs-lookup"><span data-stu-id="5295b-307">Tuple types are initialized element-by-element.</span></span>


### <a name="jagged-arrays"></a><span data-ttu-id="5295b-308">Matrizes denteadas</span><span class="sxs-lookup"><span data-stu-id="5295b-308">Jagged Arrays</span></span>

<span data-ttu-id="5295b-309">Uma matriz denteada, às vezes chamada de "matriz de matrizes", é uma matriz cujos elementos são matrizes.</span><span class="sxs-lookup"><span data-stu-id="5295b-309">A jagged array, sometimes called an "array of arrays", is an array whose elements are arrays.</span></span> <span data-ttu-id="5295b-310">Os elementos de uma matriz denteada podem ser de tamanhos diferentes.</span><span class="sxs-lookup"><span data-stu-id="5295b-310">The elements of a jagged array can be of different sizes.</span></span> <span data-ttu-id="5295b-311">O exemplo a seguir mostra como declarar e inicializar uma matriz denteada que representa uma tabela de multiplicação.</span><span class="sxs-lookup"><span data-stu-id="5295b-311">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

```qsharp
let N = 4;
mutable multiplicationTable = new Int[][N];
for (i in 1..N) {

    mutable row = new Int[i];
    for (j in 1..i) {
        set row w/= j-1 <- i * j;
    }
    set multiplicationTable w/= i-1 <- row;
}
```


### <a name="array-slices"></a><span data-ttu-id="5295b-312">Fatias de matriz</span><span class="sxs-lookup"><span data-stu-id="5295b-312">Array Slices</span></span>

<span data-ttu-id="5295b-313">Dada uma expressão de matriz e `Range` uma expressão, uma nova expressão pode ser formada `[` usando `]` o operador matriz de fatia e.</span><span class="sxs-lookup"><span data-stu-id="5295b-313">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="5295b-314">A nova expressão será do mesmo tipo que a matriz e conterá os itens de matriz indexados pelos elementos de `Range`, na ordem definida pelo. `Range`</span><span class="sxs-lookup"><span data-stu-id="5295b-314">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="5295b-315">Por exemplo, se `a` estiver associado a uma matriz de `Double`s, `a[3..-1..0]` será uma `Double[]` expressão que contém os quatro primeiros elementos de `a` , mas na ordem inversa, conforme aparecem. `a`</span><span class="sxs-lookup"><span data-stu-id="5295b-315">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="5295b-316">Se o `Range` estiver vazio, a fatia da matriz resultante será de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="5295b-316">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="5295b-317">Se a expressão de matriz não for um identificador simples, ela deverá ser colocada entre parênteses, para fatiar.</span><span class="sxs-lookup"><span data-stu-id="5295b-317">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="5295b-318">Por exemplo, se `a` e `b` forem ambas matrizes `Int`de s, uma fatia da concatenação seria expressa como:</span><span class="sxs-lookup"><span data-stu-id="5295b-318">For instance, if `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

<span data-ttu-id="5295b-319">Todas as matrizes em Q # são baseadas em zero.</span><span class="sxs-lookup"><span data-stu-id="5295b-319">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="5295b-320">Ou seja, o primeiro elemento de uma matriz `a` é sempre `a[0]`.</span><span class="sxs-lookup"><span data-stu-id="5295b-320">That is, the first element of an array `a` is always `a[0]`.</span></span>

<span data-ttu-id="5295b-321">A partir da nossa versão 0,8, damos suporte a expressões contextuais para divisão de intervalo.</span><span class="sxs-lookup"><span data-stu-id="5295b-321">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="5295b-322">Em particular, os valores de início e término do intervalo podem ser omitidos no contexto de uma expressão de divisão do intervalo.</span><span class="sxs-lookup"><span data-stu-id="5295b-322">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="5295b-323">Nesse caso, o compilador aplicará as regras a seguir para inferir os delimitadores pretendidos para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="5295b-323">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="5295b-324">Por exemplo, se o valor de início do intervalo for omitido, o valor inicial inferido</span><span class="sxs-lookup"><span data-stu-id="5295b-324">For example, if the range start value is omitted, then the inferred start value</span></span> 
- <span data-ttu-id="5295b-325">será zero se nenhuma etapa for especificada ou a etapa especificada for positiva e</span><span class="sxs-lookup"><span data-stu-id="5295b-325">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="5295b-326">é o comprimento da matriz segmentada menos uma se a etapa especificada for negativa.</span><span class="sxs-lookup"><span data-stu-id="5295b-326">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="5295b-327">Se o valor final do intervalo for omitido, o valor final inferido</span><span class="sxs-lookup"><span data-stu-id="5295b-327">If the range end value is omitted, then the inferred end value</span></span> 
- <span data-ttu-id="5295b-328">é o comprimento da matriz segmentada menos uma se nenhuma etapa for especificada ou a etapa especificada for positiva e</span><span class="sxs-lookup"><span data-stu-id="5295b-328">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="5295b-329">será zero se a etapa especificada for negativa.</span><span class="sxs-lookup"><span data-stu-id="5295b-329">is zero if the specified step is negative.</span></span> 

```qsharp
let arr = [1,2,3,4,5,6];
let slice1  = arr[3...];      // slice1 is [4,5,6];
let slice2  = arr[0..2...];   // slice2 is [1,3,5];
let slice3  = arr[...2];      // slice3 is [1,2,3];
let slice4  = arr[...2..3];   // slice4 is [1,3];
let slice5  = arr[...2...];   // slice5 is [1,3,5];
let slice7  = arr[4..-2...];  // slice7 is [5,3,1];
let slice8  = arr[...-1..3];  // slice8 is [6,5,4];
let slice9  = arr[...-1...];  // slice9 is [6,5,4,3,2,1];
let slice10 = arr[...];       // slice10 is [1,2,3,4,5,6];
```

## <a name="array-element-expressions"></a><span data-ttu-id="5295b-330">Expressões de elementos de matriz</span><span class="sxs-lookup"><span data-stu-id="5295b-330">Array Element Expressions</span></span>

<span data-ttu-id="5295b-331">Dada uma expressão de matriz e `Int` uma expressão, uma nova expressão pode ser formada `[` usando `]` o operador de elemento de matriz e.</span><span class="sxs-lookup"><span data-stu-id="5295b-331">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="5295b-332">A nova expressão será do mesmo tipo que o tipo de elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="5295b-332">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="5295b-333">Por exemplo, se `a` estiver associado a uma matriz de `Double`s, `a[4]` será uma `Double` expressão.</span><span class="sxs-lookup"><span data-stu-id="5295b-333">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="5295b-334">Se a expressão de matriz não for um identificador simples, ela deverá ser colocada entre parênteses para selecionar um elemento.</span><span class="sxs-lookup"><span data-stu-id="5295b-334">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to select an element.</span></span>
<span data-ttu-id="5295b-335">Por exemplo, se `a` e `b` forem ambas matrizes `Int`de s, um elemento da concatenação seria expresso como:</span><span class="sxs-lookup"><span data-stu-id="5295b-335">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[13]
```

<span data-ttu-id="5295b-336">Todas as matrizes em Q # são baseadas em zero.</span><span class="sxs-lookup"><span data-stu-id="5295b-336">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="5295b-337">Ou seja, o primeiro elemento de uma matriz `a` é sempre `a[0]`.</span><span class="sxs-lookup"><span data-stu-id="5295b-337">That is, the first element of an array `a` is always `a[0]`.</span></span>


## <a name="copy-and-update-expressions"></a><span data-ttu-id="5295b-338">Expressões Copy-and-Update</span><span class="sxs-lookup"><span data-stu-id="5295b-338">Copy-and-Update Expressions</span></span>

<span data-ttu-id="5295b-339">Novas matrizes podem ser criadas a partir de existentes por meio de expressões de copiar e atualizar.</span><span class="sxs-lookup"><span data-stu-id="5295b-339">New arrays can be created from existing ones via copy-and-update expressions.</span></span>
<span data-ttu-id="5295b-340">Uma expressão `expression1 w/ expression2 <- expression3`de copiar e atualizar é uma expressão do formulário, onde `expression1` deve ser do tipo `T[]` para algum tipo. `T`</span><span class="sxs-lookup"><span data-stu-id="5295b-340">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span> <span data-ttu-id="5295b-341">O segundo `expression2` define os índices dos elementos a serem modificados em comparação com a matriz em `expression1` e deve ser do tipo `Int` ou do tipo. `Range`</span><span class="sxs-lookup"><span data-stu-id="5295b-341">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span> <span data-ttu-id="5295b-342">Se `expression2` for do tipo `Int`, `expression3` deve ser do tipo `T`.</span><span class="sxs-lookup"><span data-stu-id="5295b-342">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="5295b-343">Se `expression2` for do tipo `Range`, `expression3` deve ser do tipo `T[]`.</span><span class="sxs-lookup"><span data-stu-id="5295b-343">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="5295b-344">Uma expressão `arr w/ idx <- value` de copiar e atualizar constrói uma nova matriz com todos os elementos definidos para o elemento correspondente no `arr`, exceto para os elementos em `idx`, que são definidos como os (s) em. `value`</span><span class="sxs-lookup"><span data-stu-id="5295b-344">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="5295b-345">Por exemplo, se `arr` contiver uma `[0,1,2,3]`matriz,</span><span class="sxs-lookup"><span data-stu-id="5295b-345">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="5295b-346">`arr w/ 0 <- 10`é a matriz `[10,1,2,3]`.</span><span class="sxs-lookup"><span data-stu-id="5295b-346">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="5295b-347">`arr w/ 2 <- 10`é a matriz `[0,1,10,3]`.</span><span class="sxs-lookup"><span data-stu-id="5295b-347">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="5295b-348">`arr w/ 0..2..3 <- [10,12]`é a matriz `[10,1,12,3]`.</span><span class="sxs-lookup"><span data-stu-id="5295b-348">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

<span data-ttu-id="5295b-349">Existem expressões semelhantes para itens nomeados em tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5295b-349">Similar expressions exist for named items in user-defined types.</span></span> <span data-ttu-id="5295b-350">Considere, por exemplo, o tipo</span><span class="sxs-lookup"><span data-stu-id="5295b-350">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="5295b-351">Se `c` contiver o valor do `Complex(1.,-1.)`tipo, `c w/ Re <- 0.` será uma expressão do tipo `Complex` que é avaliada `Complex(0.,-1.)`como.</span><span class="sxs-lookup"><span data-stu-id="5295b-351">If `c` contains the value of type `Complex(1.,-1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0.,-1.)`.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="5295b-352">Expressões condicionais</span><span class="sxs-lookup"><span data-stu-id="5295b-352">Conditional Expressions</span></span>

<span data-ttu-id="5295b-353">Dadas duas outras expressões do mesmo tipo e uma expressão booliana, a expressão condicional pode ser formada usando o ponto `?` de interrogação e `|`a barra vertical.</span><span class="sxs-lookup"><span data-stu-id="5295b-353">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="5295b-354">Por exemplo, `a==b ? c | d`.</span><span class="sxs-lookup"><span data-stu-id="5295b-354">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="5295b-355">Neste exemplo, o valor da expressão condicional será `c` se `a==b` for true e `d` se for false.</span><span class="sxs-lookup"><span data-stu-id="5295b-355">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

<span data-ttu-id="5295b-356">As duas expressões podem ser avaliadas como operações que têm as mesmas entradas e saídas, mas dão suporte a diferentes transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="5295b-356">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="5295b-357">Nesse caso, o tipo da expressão condicional é uma operação com as entradas e saídas que dão suporte a qualquer transmissão functors com suporte em ambas as expressões.</span><span class="sxs-lookup"><span data-stu-id="5295b-357">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="5295b-358">Por exemplo, se `Op1`, `Op2`, e `Op3` todos forem `Qubit[]=>Unit`, mas `Op1` o `Adjoint`oferecer `Op2` suporte `Controlled`a, `Op3` o oferece suporte a, e dá suporte a ambos:</span><span class="sxs-lookup"><span data-stu-id="5295b-358">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="5295b-359">`flag ? Op1 | Op2`é uma `(Qubit[] => Unit)` operação.</span><span class="sxs-lookup"><span data-stu-id="5295b-359">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="5295b-360">`flag ? Op1 | Op3`é uma `(Qubit[] => Unit is Adj)` operação.</span><span class="sxs-lookup"><span data-stu-id="5295b-360">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="5295b-361">`flag ? Op2 | Op3`é uma `(Qubit[] => Unit is Ctl)` operação.</span><span class="sxs-lookup"><span data-stu-id="5295b-361">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="5295b-362">Se qualquer uma das duas expressões de resultado possíveis incluir uma função ou uma chamada de operação, essa chamada só ocorrerá se o resultado for aquele que será o valor da chamada.</span><span class="sxs-lookup"><span data-stu-id="5295b-362">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="5295b-363">Por exemplo `a==b ? C(qs) | D(qs)`, no caso, se `a==b` for true, a `C` operação será invocada e, se for false, somente `D` será invocada.</span><span class="sxs-lookup"><span data-stu-id="5295b-363">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="5295b-364">Isso é semelhante ao curto circuito em outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="5295b-364">This is similar to short-circuiting in other languages.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="5295b-365">Precedência de operador</span><span class="sxs-lookup"><span data-stu-id="5295b-365">Operator Precedence</span></span>

<span data-ttu-id="5295b-366">Todos os operadores binários são associativos à direita, `^`exceto para.</span><span class="sxs-lookup"><span data-stu-id="5295b-366">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="5295b-367">`[` Colchetes e `]`, para a divisão e a indexação de matriz, associe antes de qualquer operador.</span><span class="sxs-lookup"><span data-stu-id="5295b-367">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="5295b-368">A transmissão functors `Adjoint` e `Controlled` a associação após a indexação da matriz, mas antes de todos os outros operadores.</span><span class="sxs-lookup"><span data-stu-id="5295b-368">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="5295b-369">Parênteses para operação e invocação de função também são associados antes de qualquer operador, mas após a indexação de matriz e transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="5295b-369">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="5295b-370">Operadores em ordem de precedência, do mais alto ao mais baixo:</span><span class="sxs-lookup"><span data-stu-id="5295b-370">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="5295b-371">Operador</span><span class="sxs-lookup"><span data-stu-id="5295b-371">Operator</span></span> | <span data-ttu-id="5295b-372">Arity</span><span class="sxs-lookup"><span data-stu-id="5295b-372">Arity</span></span> | <span data-ttu-id="5295b-373">Descrição</span><span class="sxs-lookup"><span data-stu-id="5295b-373">Description</span></span> | <span data-ttu-id="5295b-374">Tipos de operando</span><span class="sxs-lookup"><span data-stu-id="5295b-374">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="5295b-375">à direita`!`</span><span class="sxs-lookup"><span data-stu-id="5295b-375">trailing `!`</span></span> | <span data-ttu-id="5295b-376">Unário</span><span class="sxs-lookup"><span data-stu-id="5295b-376">Unary</span></span> | <span data-ttu-id="5295b-377">Desencapsular</span><span class="sxs-lookup"><span data-stu-id="5295b-377">Unwrap</span></span> | <span data-ttu-id="5295b-378">Qualquer tipo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5295b-378">Any user-defined type</span></span>
 <span data-ttu-id="5295b-379">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="5295b-379">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="5295b-380">Unário</span><span class="sxs-lookup"><span data-stu-id="5295b-380">Unary</span></span> | <span data-ttu-id="5295b-381">Numérico negativo, complemento de bit-nte, negação lógica</span><span class="sxs-lookup"><span data-stu-id="5295b-381">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="5295b-382">`Int`, `BigInt` ou `Double` para `-`, `Int` ou `BigInt` para `~~~`, `Bool` para`not`</span><span class="sxs-lookup"><span data-stu-id="5295b-382">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="5295b-383">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-383">Binary</span></span> | <span data-ttu-id="5295b-384">Potência de inteiro</span><span class="sxs-lookup"><span data-stu-id="5295b-384">Integer power</span></span> | <span data-ttu-id="5295b-385">`Int`ou `BigInt` para a base, `Int` para o expoente</span><span class="sxs-lookup"><span data-stu-id="5295b-385">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="5295b-386">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="5295b-386">`/`, `*`, `%`</span></span> | <span data-ttu-id="5295b-387">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-387">Binary</span></span> | <span data-ttu-id="5295b-388">Divisão, multiplicação, módulo de inteiro</span><span class="sxs-lookup"><span data-stu-id="5295b-388">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="5295b-389">`Int`, `BigInt` ou `Double` para `/` e `*`, `Int` ou `BigInt` para`%`</span><span class="sxs-lookup"><span data-stu-id="5295b-389">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="5295b-390">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="5295b-390">`+`, `-`</span></span> | <span data-ttu-id="5295b-391">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-391">Binary</span></span> | <span data-ttu-id="5295b-392">Adição ou concatenação de cadeia de caracteres e matriz, subtração</span><span class="sxs-lookup"><span data-stu-id="5295b-392">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="5295b-393">`Int`, `BigInt` ou `Double`, além `String` disso, ou qualquer tipo de matriz para`+`</span><span class="sxs-lookup"><span data-stu-id="5295b-393">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="5295b-394">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="5295b-394">`<<<`, `>>>`</span></span> | <span data-ttu-id="5295b-395">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-395">Binary</span></span> | <span data-ttu-id="5295b-396">Deslocamento à esquerda, deslocamento à direita</span><span class="sxs-lookup"><span data-stu-id="5295b-396">Left shift, right shift</span></span> | <span data-ttu-id="5295b-397">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5295b-397">`Int` or `BigInt`</span></span>
 <span data-ttu-id="5295b-398">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="5295b-398">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="5295b-399">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-399">Binary</span></span> | <span data-ttu-id="5295b-400">Comparações de menor que, menor que ou igual a, maior que, maior que ou igual a</span><span class="sxs-lookup"><span data-stu-id="5295b-400">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="5295b-401">`Int``BigInt` ou`Double`</span><span class="sxs-lookup"><span data-stu-id="5295b-401">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="5295b-402">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="5295b-402">`==`, `!=`</span></span> | <span data-ttu-id="5295b-403">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-403">Binary</span></span> | <span data-ttu-id="5295b-404">comparações iguais, não iguais</span><span class="sxs-lookup"><span data-stu-id="5295b-404">equal, not-equal comparisons</span></span> | <span data-ttu-id="5295b-405">qualquer tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="5295b-405">any primitive type</span></span>
 `&&&` | <span data-ttu-id="5295b-406">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-406">Binary</span></span> | <span data-ttu-id="5295b-407">AND bit a bit</span><span class="sxs-lookup"><span data-stu-id="5295b-407">Bitwise AND</span></span> | <span data-ttu-id="5295b-408">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5295b-408">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="5295b-409">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-409">Binary</span></span> | <span data-ttu-id="5295b-410">XOR bit a bit</span><span class="sxs-lookup"><span data-stu-id="5295b-410">Bitwise XOR</span></span> | <span data-ttu-id="5295b-411">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5295b-411">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="5295b-412">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-412">Binary</span></span> | <span data-ttu-id="5295b-413">OR bit a bit</span><span class="sxs-lookup"><span data-stu-id="5295b-413">Bitwise OR</span></span> | <span data-ttu-id="5295b-414">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5295b-414">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="5295b-415">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-415">Binary</span></span> | <span data-ttu-id="5295b-416">AND lógico</span><span class="sxs-lookup"><span data-stu-id="5295b-416">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="5295b-417">Binário</span><span class="sxs-lookup"><span data-stu-id="5295b-417">Binary</span></span> | <span data-ttu-id="5295b-418">OR lógico</span><span class="sxs-lookup"><span data-stu-id="5295b-418">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="5295b-419">Binary/ternário</span><span class="sxs-lookup"><span data-stu-id="5295b-419">Binary/Ternary</span></span> | <span data-ttu-id="5295b-420">Operador de intervalo</span><span class="sxs-lookup"><span data-stu-id="5295b-420">Range operator</span></span> | `Int`
 <span data-ttu-id="5295b-421">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="5295b-421">`?` `|`</span></span> | <span data-ttu-id="5295b-422">Ternário</span><span class="sxs-lookup"><span data-stu-id="5295b-422">Ternary</span></span> | <span data-ttu-id="5295b-423">Condicional</span><span class="sxs-lookup"><span data-stu-id="5295b-423">Conditional</span></span> | <span data-ttu-id="5295b-424">`Bool`para o lado esquerdo</span><span class="sxs-lookup"><span data-stu-id="5295b-424">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="5295b-425">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="5295b-425">`w/` `<-`</span></span> | <span data-ttu-id="5295b-426">Ternário</span><span class="sxs-lookup"><span data-stu-id="5295b-426">Ternary</span></span> | <span data-ttu-id="5295b-427">Copiar e atualizar</span><span class="sxs-lookup"><span data-stu-id="5295b-427">Copy-and-update</span></span> | <span data-ttu-id="5295b-428">consulte [expressões de copiar e atualizar](#copy-and-update-expressions)</span><span class="sxs-lookup"><span data-stu-id="5295b-428">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>
