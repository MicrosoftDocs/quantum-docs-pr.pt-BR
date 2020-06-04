---
title: 'Expressões de tipo em Q #'
description: 'Entenda como especificar, referenciar e combinar constantes, variáveis, operadores, operações e funções como expressões em Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
ms.openlocfilehash: c4b2cc0bed44ffdfb191ba522d6526959e7c6708
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327298"
---
# <a name="type-expressions-in-q"></a><span data-ttu-id="479a2-103">Expressões de tipo em Q #</span><span class="sxs-lookup"><span data-stu-id="479a2-103">Type Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="479a2-104">Expressões numéricas</span><span class="sxs-lookup"><span data-stu-id="479a2-104">Numeric Expressions</span></span>

<span data-ttu-id="479a2-105">Expressões numéricas são expressões do tipo `Int` , `BigInt` ou `Double` .</span><span class="sxs-lookup"><span data-stu-id="479a2-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="479a2-106">Ou seja, eles são números inteiros ou de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="479a2-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="479a2-107">`Int`os literais em Q # são escritos simplesmente como uma sequência de dígitos.</span><span class="sxs-lookup"><span data-stu-id="479a2-107">`Int` literals in Q# are written simply as a sequence of digits.</span></span>
<span data-ttu-id="479a2-108">Os inteiros hexadecimais e binários têm suporte com `0x` um `0b` prefixo e, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="479a2-108">Hexadecimal and binary integers are supported with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="479a2-109">`BigInt`os literais em Q # são gravados com um `l` sufixo ou à direita `L` .</span><span class="sxs-lookup"><span data-stu-id="479a2-109">`BigInt` literals in Q# are written with a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="479a2-110">Há suporte para inteiros grandes hexadecimais com um prefixo "0x".</span><span class="sxs-lookup"><span data-stu-id="479a2-110">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="479a2-111">Portanto, veja a seguir todos os usos válidos de `BigInt` literais:</span><span class="sxs-lookup"><span data-stu-id="479a2-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="479a2-112">`Double`literais em Q # são números de ponto flutuante gravados usando dígitos decimais.</span><span class="sxs-lookup"><span data-stu-id="479a2-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="479a2-113">Eles podem ser escritos com um ponto decimal, `.` e/ou uma parte exponencial indicada com ' e ' ou ' e ' (após o qual apenas um possível sinal negativo e dígitos decimais são válidos).</span><span class="sxs-lookup"><span data-stu-id="479a2-113">They can be written with a decimal point, `.`, and/or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="479a2-114">Os seguintes são `Double` literais válidos: `0.0` , `1.2e5` , `1e-5` .</span><span class="sxs-lookup"><span data-stu-id="479a2-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="479a2-115">Dada uma expressão de matriz de qualquer tipo de elemento, uma `Int` expressão pode ser formada usando a [`Length`](xref:microsoft.quantum.core.length) função interna, com a expressão de matriz entre parênteses `(` e `)` .</span><span class="sxs-lookup"><span data-stu-id="479a2-115">Given an array expression of any element type, an `Int` expression may be formed using the [`Length`](xref:microsoft.quantum.core.length) built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="479a2-116">Por exemplo, se `a` estiver associado a uma matriz, `Length(a)` será uma expressão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="479a2-116">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="479a2-117">Se `b` é uma matriz de matrizes de inteiros, `Int[][]` , `Length(b)` é o número de submatrizes em `b` e `Length(b[1])` é o número de inteiros na segunda submatriz no `b` .</span><span class="sxs-lookup"><span data-stu-id="479a2-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="479a2-118">Dadas duas expressões numéricas do mesmo tipo, os operadores binários,, `+` `-` `*` e `/` podem ser usados para formar uma nova expressão numérica.</span><span class="sxs-lookup"><span data-stu-id="479a2-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="479a2-119">O tipo da nova expressão será o mesmo que os tipos das expressões constituintes.</span><span class="sxs-lookup"><span data-stu-id="479a2-119">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="479a2-120">Dadas duas expressões de inteiro, o operador binário `^` (potência) pode ser usado para formar uma nova expressão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="479a2-120">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="479a2-121">Da mesma forma, `^` pode ser usado com duas expressões duplas para formar uma nova expressão Double.</span><span class="sxs-lookup"><span data-stu-id="479a2-121">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="479a2-122">Por fim, `^` pode ser usado com um inteiro grande à esquerda e um inteiro à direita para formar uma nova expressão de inteiro grande.</span><span class="sxs-lookup"><span data-stu-id="479a2-122">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="479a2-123">Nesse caso, o segundo parâmetro deve caber em 32 bits; caso contrário, um erro de tempo de execução será gerado.</span><span class="sxs-lookup"><span data-stu-id="479a2-123">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="479a2-124">Dadas duas expressões de inteiro ou grandes inteiros, um novo inteiro ou uma expressão de inteiro grande pode ser formada usando os `%` operadores (módulo), `&&&` (bit e), (OR-bit or `|||` ) ou `^^^` (XOR).</span><span class="sxs-lookup"><span data-stu-id="479a2-124">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="479a2-125">Dado um inteiro ou uma expressão de inteiro grande à esquerda e uma expressão de inteiro à direita, os `<<<` operadores (deslocamento aritmético à esquerda) ou `>>>` (deslocamento aritmético à direita) podem ser usados para criar uma nova expressão com o mesmo tipo que a expressão esquerda.</span><span class="sxs-lookup"><span data-stu-id="479a2-125">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="479a2-126">O segundo parâmetro (o valor de deslocamento) para a operação de deslocamento deve ser maior ou igual a zero; o comportamento para valores de deslocamento negativos é indefinido.</span><span class="sxs-lookup"><span data-stu-id="479a2-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="479a2-127">O valor de deslocamento para uma das operações de deslocamento também deve se ajustar a 32 bits; caso contrário, um erro de tempo de execução será gerado.</span><span class="sxs-lookup"><span data-stu-id="479a2-127">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="479a2-128">Se o número a ser deslocado for um inteiro, o valor de deslocamento será interpretado `mod 64` ; ou seja, um deslocamento de 1 e um deslocamento de 65 terão o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="479a2-128">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="479a2-129">Para os valores inteiros e inteiros grandes, as turnos são aritméticas.</span><span class="sxs-lookup"><span data-stu-id="479a2-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="479a2-130">A mudança de um valor negativo para a esquerda ou direita resultará em um número negativo.</span><span class="sxs-lookup"><span data-stu-id="479a2-130">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="479a2-131">Ou seja, mudar uma etapa para a esquerda ou para a direita é exatamente o mesmo que multiplicar ou dividir por 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="479a2-131">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="479a2-132">Divisão de inteiros e módulo de inteiro seguem o mesmo comportamento para números negativos em C#.</span><span class="sxs-lookup"><span data-stu-id="479a2-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="479a2-133">Ou seja, `a % b` sempre terá o mesmo sinal de `a` e `b * (a / b) + a % b` sempre será igual `a` .</span><span class="sxs-lookup"><span data-stu-id="479a2-133">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="479a2-134">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="479a2-134">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="479a2-135">5</span><span class="sxs-lookup"><span data-stu-id="479a2-135">5</span></span> | <span data-ttu-id="479a2-136">2</span><span class="sxs-lookup"><span data-stu-id="479a2-136">2</span></span> | <span data-ttu-id="479a2-137">2</span><span class="sxs-lookup"><span data-stu-id="479a2-137">2</span></span> | <span data-ttu-id="479a2-138">1</span><span class="sxs-lookup"><span data-stu-id="479a2-138">1</span></span>
 <span data-ttu-id="479a2-139">5</span><span class="sxs-lookup"><span data-stu-id="479a2-139">5</span></span> | <span data-ttu-id="479a2-140">-2</span><span class="sxs-lookup"><span data-stu-id="479a2-140">-2</span></span> | <span data-ttu-id="479a2-141">-2</span><span class="sxs-lookup"><span data-stu-id="479a2-141">-2</span></span> | <span data-ttu-id="479a2-142">1</span><span class="sxs-lookup"><span data-stu-id="479a2-142">1</span></span>
 <span data-ttu-id="479a2-143">-5</span><span class="sxs-lookup"><span data-stu-id="479a2-143">-5</span></span> | <span data-ttu-id="479a2-144">2</span><span class="sxs-lookup"><span data-stu-id="479a2-144">2</span></span> | <span data-ttu-id="479a2-145">-2</span><span class="sxs-lookup"><span data-stu-id="479a2-145">-2</span></span> | <span data-ttu-id="479a2-146">-1</span><span class="sxs-lookup"><span data-stu-id="479a2-146">-1</span></span>
 <span data-ttu-id="479a2-147">-5</span><span class="sxs-lookup"><span data-stu-id="479a2-147">-5</span></span> | <span data-ttu-id="479a2-148">-2</span><span class="sxs-lookup"><span data-stu-id="479a2-148">-2</span></span> | <span data-ttu-id="479a2-149">2</span><span class="sxs-lookup"><span data-stu-id="479a2-149">2</span></span> | <span data-ttu-id="479a2-150">-1</span><span class="sxs-lookup"><span data-stu-id="479a2-150">-1</span></span>

<span data-ttu-id="479a2-151">Divisão de inteiro grande e módulo funciona da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="479a2-151">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="479a2-152">Dada qualquer expressão numérica, uma nova expressão pode ser formada usando o `-` operador unário.</span><span class="sxs-lookup"><span data-stu-id="479a2-152">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="479a2-153">A nova expressão será o mesmo tipo da expressão constituinte.</span><span class="sxs-lookup"><span data-stu-id="479a2-153">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="479a2-154">Devido a qualquer inteiro ou expressão de inteiro grande, uma nova expressão do mesmo tipo pode ser formada usando o `~~~` operador unário (complemento de bits).</span><span class="sxs-lookup"><span data-stu-id="479a2-154">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="479a2-155">Expressões boolianas</span><span class="sxs-lookup"><span data-stu-id="479a2-155">Boolean Expressions</span></span>

<span data-ttu-id="479a2-156">Os dois `Bool` valores literais são `true` e `false` .</span><span class="sxs-lookup"><span data-stu-id="479a2-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="479a2-157">Dadas as duas expressões do mesmo tipo primitivo, os `==` `!=` operadores binários e podem ser usados para construir uma `Bool` expressão.</span><span class="sxs-lookup"><span data-stu-id="479a2-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="479a2-158">A expressão será true se as duas expressões forem iguais e false se não.</span><span class="sxs-lookup"><span data-stu-id="479a2-158">The expression will be true if the two expressions are equal, and false if not.</span></span>

<span data-ttu-id="479a2-159">Os valores de tipos definidos pelo usuário não podem ser comparados, apenas seus valores não encapsulados podem ser comparados.</span><span class="sxs-lookup"><span data-stu-id="479a2-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="479a2-160">Por exemplo, usando o operador "sem encapsulamento" `!` (explicado em detalhes em [tipos em Q #](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span><span class="sxs-lookup"><span data-stu-id="479a2-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="479a2-161">A comparação de igualdade para `Qubit` valores é igualdade de identidade; ou seja, se as duas expressões identificam o mesmo qubit.</span><span class="sxs-lookup"><span data-stu-id="479a2-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="479a2-162">O estado dos dois qubits não são comparados, acessados, medidos ou modificados por essa comparação.</span><span class="sxs-lookup"><span data-stu-id="479a2-162">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="479a2-163">A comparação de igualdade para `Double` valores pode ser enganosa devido a efeitos de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="479a2-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="479a2-164">Por exemplo, `49.0 * (1.0/49.0) != 1.0` .</span><span class="sxs-lookup"><span data-stu-id="479a2-164">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="479a2-165">Dadas quaisquer duas expressões numéricas, os operadores binários,, `>` `<` `>=` e `<=` podem ser usados para construir uma nova expressão booliana que seja verdadeira se a primeira expressão for maior que, menor que, maior ou igual ou menor ou igual à segunda expressão.</span><span class="sxs-lookup"><span data-stu-id="479a2-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="479a2-166">Dadas quaisquer duas expressões booleanas, os `and` `or` operadores binários e podem ser usados para construir uma nova expressão booliana que seja verdadeira se ambos (resp. ou ambos) as duas expressões forem true.</span><span class="sxs-lookup"><span data-stu-id="479a2-166">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="479a2-167">Dada qualquer expressão booliana, o `not` operador unário pode ser usado para construir uma nova expressão booliana que seja verdadeira se a expressão constituinte for falsa.</span><span class="sxs-lookup"><span data-stu-id="479a2-167">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="479a2-168">Expressões de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="479a2-168">String Expressions</span></span>

<span data-ttu-id="479a2-169">Q # permite que as cadeias de caracteres sejam usadas na `fail` instrução (explicada em [fluxo de controle](xref:microsoft.quantum.guide.controlflow#fail-statement)) e na [`Message`](xref:microsoft.quantum.intrinsic.message) função padrão.</span><span class="sxs-lookup"><span data-stu-id="479a2-169">Q# allows strings to be used in the `fail` statement (explained at [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:microsoft.quantum.intrinsic.message) standard function.</span></span>
<span data-ttu-id="479a2-170">O comportamento específico do segundo depende do simulador que está sendo usado, mas normalmente grava uma mensagem no console do host quando chamado durante um programa Q #.</span><span class="sxs-lookup"><span data-stu-id="479a2-170">The specific behavior of the latter depends on the simulator being used, but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="479a2-171">Cadeias de caracteres em Q # são literais ou cadeias de caracteres interpoladas.</span><span class="sxs-lookup"><span data-stu-id="479a2-171">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="479a2-172">Literais de cadeia de caracteres são semelhantes a literais de cadeia de caracteres simples na maioria dos idiomas: uma sequência de caracteres Unicode entre aspas duplas, `"` .</span><span class="sxs-lookup"><span data-stu-id="479a2-172">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="479a2-173">Dentro de uma cadeia de caracteres, o caractere de barra invertida `\` pode ser usado para escapar de um caractere de aspas duplas e para inserir uma linha nova como `\n` , um retorno de carro como `\r` e uma tabulação como `\t` .</span><span class="sxs-lookup"><span data-stu-id="479a2-173">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="479a2-174">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="479a2-174">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="479a2-175">Cadeias de caracteres interpoladas</span><span class="sxs-lookup"><span data-stu-id="479a2-175">Interpolated strings</span></span>

<span data-ttu-id="479a2-176">A sintaxe de Q # para interpolações de cadeia de caracteres é um subconjunto da sintaxe do C#, mas resumimos aqui os pontos principais conforme eles pertencem a Q #.</span><span class="sxs-lookup"><span data-stu-id="479a2-176">The Q# syntax for string interpolations is a subset of the C# syntax, but we summarize here the key points as they pertain to Q#.</span></span>
<span data-ttu-id="479a2-177">As distinções principais são discutidas abaixo.</span><span class="sxs-lookup"><span data-stu-id="479a2-177">The main distinctions are discussed below.</span></span>

<span data-ttu-id="479a2-178">Para identificar uma literal de cadeia de caracteres como uma cadeia de caracteres interpolada, preceda-o com o símbolo `$`.</span><span class="sxs-lookup"><span data-stu-id="479a2-178">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span>
<span data-ttu-id="479a2-179">Você não pode ter nenhum espaço em branco entre o `$` e o `"` que inicia uma cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="479a2-179">You cannot have any white space between the `$`and the `"` that starts a string literal.</span></span>

<span data-ttu-id="479a2-180">Veja a seguir um exemplo básico usando a [`Message`](xref:microsoft.quantum.intrinsic.message) função para gravar o resultado de uma medida no console, juntamente com outras expressões Q #.</span><span class="sxs-lookup"><span data-stu-id="479a2-180">The following is a basic example using the [`Message`](xref:microsoft.quantum.intrinsic.message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```
<span data-ttu-id="479a2-181">Qualquer expressão Q # válida pode aparecer em uma cadeia de caracteres interpolada.</span><span class="sxs-lookup"><span data-stu-id="479a2-181">Any valid Q# expression may appear in an interpolated string.</span></span>

<span data-ttu-id="479a2-182">Mais detalhes sobre a sintaxe do C# podem ser encontrados em [*cadeias de caracteres interpoladas*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span><span class="sxs-lookup"><span data-stu-id="479a2-182">Further details on the C# syntax can be found at [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>
<span data-ttu-id="479a2-183">A distinção mais notável é que Q # não oferece suporte a cadeias de caracteres interpoladas (várias linhas) textuais.</span><span class="sxs-lookup"><span data-stu-id="479a2-183">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="479a2-184">As expressões dentro de uma cadeia de caracteres interpolada seguem a sintaxe Q #, e não a sintaxe C#.</span><span class="sxs-lookup"><span data-stu-id="479a2-184">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="479a2-185">Expressões de intervalo</span><span class="sxs-lookup"><span data-stu-id="479a2-185">Range Expressions</span></span>

<span data-ttu-id="479a2-186">Dadas as três `Int` expressões `start` , `step` e `stop` , `start .. step .. stop` é uma expressão de intervalo cujo primeiro elemento é `start` , o segundo elemento é, o `start+step` terceiro elemento é `start+step+step` , etc., até que `stop` seja passado.</span><span class="sxs-lookup"><span data-stu-id="479a2-186">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="479a2-187">Um intervalo pode estar vazio se, por exemplo, `step` for positivo e `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="479a2-187">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="479a2-188">O último elemento do intervalo será `stop` se a diferença entre `start` e `stop` for um múltiplo integral de `step` ; ou seja, o intervalo é inclusivo em ambas as extremidades.</span><span class="sxs-lookup"><span data-stu-id="479a2-188">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="479a2-189">Dadas as duas `Int` expressões `start` e `stop` , `start .. stop` é uma expressão de intervalo igual a `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="479a2-189">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="479a2-190">Observe que o implícito `step` é + 1, mesmo se `stop` for menor que `start` ; nesse caso, o intervalo estará vazio.</span><span class="sxs-lookup"><span data-stu-id="479a2-190">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="479a2-191">Alguns intervalos de exemplo são:</span><span class="sxs-lookup"><span data-stu-id="479a2-191">Some example ranges are:</span></span>

- <span data-ttu-id="479a2-192">`1..3`é o intervalo 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="479a2-192">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="479a2-193">`2..2..5`é o intervalo de 2, 4.</span><span class="sxs-lookup"><span data-stu-id="479a2-193">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="479a2-194">`2..2..6`é o intervalo de 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="479a2-194">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="479a2-195">`6..-2..2`é o intervalo de 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="479a2-195">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="479a2-196">`2..1`é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="479a2-196">`2..1` is the empty range.</span></span>
- <span data-ttu-id="479a2-197">`2..6..7`é o intervalo 2.</span><span class="sxs-lookup"><span data-stu-id="479a2-197">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="479a2-198">`2..2..1`é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="479a2-198">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="479a2-199">`1..-1..2`é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="479a2-199">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="479a2-200">Expressões qubit</span><span class="sxs-lookup"><span data-stu-id="479a2-200">Qubit Expressions</span></span>

<span data-ttu-id="479a2-201">As únicas `Qubit` expressões são símbolos que são associados a `Qubit` valores ou elementos de matriz de `Qubit` matrizes.</span><span class="sxs-lookup"><span data-stu-id="479a2-201">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="479a2-202">Não há `Qubit` literais.</span><span class="sxs-lookup"><span data-stu-id="479a2-202">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="479a2-203">Expressões Pauli</span><span class="sxs-lookup"><span data-stu-id="479a2-203">Pauli Expressions</span></span>

<span data-ttu-id="479a2-204">Os quatro `Pauli` valores, `PauliI` , `PauliX` , `PauliY` e `PauliZ` , são expressões válidas `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="479a2-204">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="479a2-205">Além disso, as únicas `Pauli` expressões são símbolos associados a `Pauli` valores ou elementos de matriz de `Pauli` matrizes.</span><span class="sxs-lookup"><span data-stu-id="479a2-205">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="479a2-206">Expressões de resultado</span><span class="sxs-lookup"><span data-stu-id="479a2-206">Result Expressions</span></span>

<span data-ttu-id="479a2-207">Os dois `Result` valores, `One` e `Zero` , são expressões válidas `Result` .</span><span class="sxs-lookup"><span data-stu-id="479a2-207">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="479a2-208">Além disso, as únicas `Result` expressões são símbolos associados a `Result` valores ou elementos de matriz de `Result` matrizes.</span><span class="sxs-lookup"><span data-stu-id="479a2-208">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="479a2-209">Em particular, observe que `One` não é o mesmo que o inteiro `1` , e não há nenhuma conversão direta entre eles.</span><span class="sxs-lookup"><span data-stu-id="479a2-209">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="479a2-210">O mesmo é verdadeiro para `Zero` e `0` .</span><span class="sxs-lookup"><span data-stu-id="479a2-210">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="479a2-211">Expressões de tupla</span><span class="sxs-lookup"><span data-stu-id="479a2-211">Tuple Expressions</span></span>

<span data-ttu-id="479a2-212">Um literal de tupla é uma sequência de expressões de elemento do tipo apropriado, separados por vírgulas, colocadas em `(` e `)` .</span><span class="sxs-lookup"><span data-stu-id="479a2-212">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="479a2-213">Por exemplo, `(1, One)` é uma `(Int, Result)` expressão.</span><span class="sxs-lookup"><span data-stu-id="479a2-213">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="479a2-214">Além de literais, as únicas expressões de tupla são símbolos associados a valores de tupla, elementos de matriz de matrizes de tupla e invocações que retornam tuplas.</span><span class="sxs-lookup"><span data-stu-id="479a2-214">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="479a2-215">Expressões de tipo definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="479a2-215">User-Defined Type Expressions</span></span>

<span data-ttu-id="479a2-216">Um literal de um tipo definido pelo usuário consiste no nome do tipo seguido por um literal de tupla do tipo de tupla base do tipo.</span><span class="sxs-lookup"><span data-stu-id="479a2-216">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="479a2-217">Por exemplo, se `IntPair` for um tipo definido pelo usuário com base em `(Int, Int)` , `IntPair(2, 3)` seria um literal válido desse tipo.</span><span class="sxs-lookup"><span data-stu-id="479a2-217">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="479a2-218">Além de literais, as únicas expressões de um tipo definido pelo usuário são símbolos que são associados a valores desse tipo, elementos da matriz de matrizes desse tipo e invocações que retornam esse tipo.</span><span class="sxs-lookup"><span data-stu-id="479a2-218">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="479a2-219">Desencapsular expressões</span><span class="sxs-lookup"><span data-stu-id="479a2-219">Unwrap Expressions</span></span>

<span data-ttu-id="479a2-220">Em Q #, o operador de desencapsulamento é um ponto de exclamação à direita `!` .</span><span class="sxs-lookup"><span data-stu-id="479a2-220">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="479a2-221">Por exemplo, se `IntPair` é um tipo definido pelo usuário com o tipo subjacente `(Int, Int)` e `s` era uma variável com valor `IntPair(2, 3)` , `s!` seria `(2, 3)` .</span><span class="sxs-lookup"><span data-stu-id="479a2-221">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2, 3)`, then `s!` would be `(2, 3)`.</span></span>

<span data-ttu-id="479a2-222">Para tipos definidos pelo usuário definidos em termos de outros tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="479a2-222">For user-defined types defined in terms of other user-defined types.</span></span> <span data-ttu-id="479a2-223">o operador de desencapsulamento pode ser repetido; por exemplo, `s!!` indica o valor duplo não encapsulado de `s` .</span><span class="sxs-lookup"><span data-stu-id="479a2-223">the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="479a2-224">Portanto, se `WrappedPair` for um tipo definido pelo usuário com o tipo subjacente `IntPair` , e `t` for uma variável com valor `WrappedPair(IntPair(1,2))` , será `t!!` `(1,2)` .</span><span class="sxs-lookup"><span data-stu-id="479a2-224">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="479a2-225">O `!` operador tem precedência maior do que todos os outros operadores diferentes de `[]` para indexação e divisão de matriz.</span><span class="sxs-lookup"><span data-stu-id="479a2-225">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="479a2-226">`!`e `[]` Associate posicionalmente, ou seja, `a[i]![3]` deve ser lido como `((a[i])!)[3]` : pegar o `i` ' th element ' `a` , desencapsulá-lo e, em seguida, obter o terceiro elemento do valor não encapsulado (que deve ser uma matriz).</span><span class="sxs-lookup"><span data-stu-id="479a2-226">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="479a2-227">A precedência do `!` operador tem um impacto que pode não ser óbvio.</span><span class="sxs-lookup"><span data-stu-id="479a2-227">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="479a2-228">Se uma função ou operação retorna um valor que, em seguida, é desencapsulada, a função ou a chamada de operação deve ser colocada entre parênteses para que a tupla de argumento seja associada à chamada em vez de ser desencapsulada.</span><span class="sxs-lookup"><span data-stu-id="479a2-228">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="479a2-229">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="479a2-229">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="479a2-230">Expressões de matriz</span><span class="sxs-lookup"><span data-stu-id="479a2-230">Array Expressions</span></span>

<span data-ttu-id="479a2-231">Um literal de matriz é uma sequência de uma ou mais expressões de elemento, separadas por vírgulas, colocadas em `[` e `]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-231">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="479a2-232">Todos os elementos devem ser compatíveis com o mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="479a2-232">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="479a2-233">Dadas duas matrizes do mesmo tipo, o `+` operador binário pode ser usado para formar uma nova matriz que é a concatenação das duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="479a2-233">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="479a2-234">Por exemplo, `[1,2,3] + [4,5,6]` é `[1,2,3,4,5,6]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-234">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="479a2-235">Criação de matriz</span><span class="sxs-lookup"><span data-stu-id="479a2-235">Array Creation</span></span>

<span data-ttu-id="479a2-236">Dado um tipo e uma `Int` expressão, o `new` operador pode ser usado para alocar uma nova matriz do tamanho determinado.</span><span class="sxs-lookup"><span data-stu-id="479a2-236">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="479a2-237">Por exemplo, `new Int[i + 1]` alocaria uma nova `Int` matriz com `i + 1` elementos.</span><span class="sxs-lookup"><span data-stu-id="479a2-237">For instance, `new Int[i + 1]` would allocate a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="479a2-238">Literais de matriz vazios, `[]` , não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="479a2-238">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="479a2-239">Em vez disso, o uso de `new ★[0]` , onde `★` é o espaço reservado para um tipo adequado, permite criar a matriz desejada de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="479a2-239">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>

<span data-ttu-id="479a2-240">Os elementos de uma nova matriz são inicializados para um valor padrão dependente de tipo.</span><span class="sxs-lookup"><span data-stu-id="479a2-240">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="479a2-241">Na maioria dos casos, essa é uma variação de zero.</span><span class="sxs-lookup"><span data-stu-id="479a2-241">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="479a2-242">Para qubits e callableies, que são referências a entidades, não há nenhum valor padrão razoável.</span><span class="sxs-lookup"><span data-stu-id="479a2-242">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="479a2-243">Portanto, para esses tipos, o padrão é uma referência inválida que não pode ser usada sem causar um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="479a2-243">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="479a2-244">Isso é semelhante a uma referência nula em linguagens como C# ou Java.</span><span class="sxs-lookup"><span data-stu-id="479a2-244">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="479a2-245">As matrizes que contêm qubits ou callables devem ser inicializadas corretamente com valores não padrão antes que seus elementos possam ser usados com segurança.</span><span class="sxs-lookup"><span data-stu-id="479a2-245">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="479a2-246">Rotinas de inicialização adequadas podem ser encontradas em <xref:microsoft.quantum.arrays> .</span><span class="sxs-lookup"><span data-stu-id="479a2-246">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="479a2-247">Os valores padrão para cada tipo são:</span><span class="sxs-lookup"><span data-stu-id="479a2-247">The default values for each type are:</span></span>

<span data-ttu-id="479a2-248">Type</span><span class="sxs-lookup"><span data-stu-id="479a2-248">Type</span></span> | <span data-ttu-id="479a2-249">Padrão</span><span class="sxs-lookup"><span data-stu-id="479a2-249">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="479a2-250">_qubit inválido_</span><span class="sxs-lookup"><span data-stu-id="479a2-250">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="479a2-251">O intervalo vazio,`1..1..0`</span><span class="sxs-lookup"><span data-stu-id="479a2-251">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="479a2-252">_callable inválido_</span><span class="sxs-lookup"><span data-stu-id="479a2-252">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="479a2-253">Os tipos de tupla são inicializados elemento por elemento.</span><span class="sxs-lookup"><span data-stu-id="479a2-253">Tuple types are initialized element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="479a2-254">Elementos da matriz</span><span class="sxs-lookup"><span data-stu-id="479a2-254">Array Elements</span></span>

<span data-ttu-id="479a2-255">Dada uma expressão de matriz e uma `Int` expressão, uma nova expressão pode ser formada usando o `[` operador de elemento de matriz e `]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-255">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="479a2-256">A nova expressão será do mesmo tipo que o tipo de elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="479a2-256">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="479a2-257">Por exemplo, se `a` estiver associado a uma matriz de `Double` s, `a[4]` será uma `Double` expressão.</span><span class="sxs-lookup"><span data-stu-id="479a2-257">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="479a2-258">Se a expressão de matriz não for um identificador simples, ela deverá ser colocada entre parênteses para selecionar um elemento.</span><span class="sxs-lookup"><span data-stu-id="479a2-258">If the array expression is not a simple identifier, it must be enclosed in parentheses in order to select an element.</span></span>
<span data-ttu-id="479a2-259">Por exemplo, se `a` e `b` forem ambas matrizes de `Int` s, um elemento da concatenação seria expresso como:</span><span class="sxs-lookup"><span data-stu-id="479a2-259">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="479a2-260">Todas as matrizes em Q # são baseadas em zero.</span><span class="sxs-lookup"><span data-stu-id="479a2-260">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="479a2-261">Ou seja, o primeiro elemento de uma matriz `a` é sempre `a[0]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-261">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="479a2-262">Fatias de matriz</span><span class="sxs-lookup"><span data-stu-id="479a2-262">Array Slices</span></span>

<span data-ttu-id="479a2-263">Dada uma expressão de matriz e uma `Range` expressão, uma nova expressão pode ser formada usando o `[` `]` operador matriz de fatia e.</span><span class="sxs-lookup"><span data-stu-id="479a2-263">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="479a2-264">A nova expressão será do mesmo tipo que a matriz e conterá os itens de matriz indexados pelos elementos de `Range` , na ordem definida pelo `Range` .</span><span class="sxs-lookup"><span data-stu-id="479a2-264">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="479a2-265">Por exemplo, se `a` estiver associado a uma matriz de `Double` s, `a[3..-1..0]` será uma `Double[]` expressão que contém os quatro primeiros elementos de, `a` mas na ordem inversa, conforme aparecem `a` .</span><span class="sxs-lookup"><span data-stu-id="479a2-265">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="479a2-266">Se o `Range` estiver vazio, a fatia da matriz resultante será de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="479a2-266">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="479a2-267">Assim como ocorre com a referência de elementos de matriz, se a expressão de matriz não for um identificador simples, ela deverá ser colocada entre parênteses, para fatiar.</span><span class="sxs-lookup"><span data-stu-id="479a2-267">Just as with referencing array elements, if the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="479a2-268">Se `a` e `b` forem ambas matrizes de `Int` s, uma fatia da concatenação seria expressa como:</span><span class="sxs-lookup"><span data-stu-id="479a2-268">If `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="479a2-269">Valores de início/término inferidos</span><span class="sxs-lookup"><span data-stu-id="479a2-269">Inferred start/end values</span></span>

<span data-ttu-id="479a2-270">A partir da nossa versão 0,8, damos suporte a expressões contextuais para divisão de intervalo.</span><span class="sxs-lookup"><span data-stu-id="479a2-270">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="479a2-271">Em particular, os valores de início e término do intervalo podem ser omitidos no contexto de uma expressão de divisão do intervalo.</span><span class="sxs-lookup"><span data-stu-id="479a2-271">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="479a2-272">Nesse caso, o compilador aplicará as regras a seguir para inferir os delimitadores pretendidos para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="479a2-272">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="479a2-273">Por exemplo, se o valor de início do intervalo for omitido, o valor inicial inferido</span><span class="sxs-lookup"><span data-stu-id="479a2-273">For example, if the range start value is omitted,  then the inferred start value</span></span> 
- <span data-ttu-id="479a2-274">será zero se nenhuma etapa for especificada ou a etapa especificada for positiva e</span><span class="sxs-lookup"><span data-stu-id="479a2-274">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="479a2-275">é o comprimento da matriz segmentada menos uma se a etapa especificada for negativa.</span><span class="sxs-lookup"><span data-stu-id="479a2-275">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="479a2-276">Se o valor final do intervalo for omitido, o valor final inferido</span><span class="sxs-lookup"><span data-stu-id="479a2-276">If the range end value is omitted,  then the inferred end value</span></span> 
- <span data-ttu-id="479a2-277">é o comprimento da matriz segmentada menos uma se nenhuma etapa for especificada ou a etapa especificada for positiva e</span><span class="sxs-lookup"><span data-stu-id="479a2-277">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="479a2-278">será zero se a etapa especificada for negativa.</span><span class="sxs-lookup"><span data-stu-id="479a2-278">is zero if the specified step is negative.</span></span> 

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

### <a name="copy-and-update-expressions"></a><span data-ttu-id="479a2-279">Expressões Copy-and-Update</span><span class="sxs-lookup"><span data-stu-id="479a2-279">Copy-and-Update Expressions</span></span>

<span data-ttu-id="479a2-280">Como todos os tipos de Q # são tipos de valor — com o qubits usando uma função especial, formalmente, uma "cópia" é criada quando um valor é associado a um símbolo ou quando um símbolo é reassociado.</span><span class="sxs-lookup"><span data-stu-id="479a2-280">Since all Q# types are value types — with the qubits taking a somewhat special role —formally a "copy" is created when a value is bound to a symbol, or when a symbol is rebound.</span></span> <span data-ttu-id="479a2-281">Isso significa que o comportamento de Q # é o mesmo que se uma cópia fosse criada na atribuição.</span><span class="sxs-lookup"><span data-stu-id="479a2-281">That is to say, the behavior of Q# is the same as if a copy were created on assignment.</span></span>
<span data-ttu-id="479a2-282">É claro que, na prática, apenas as partes relevantes são, na verdade, recriadas, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="479a2-282">Of course in practice only the relevant pieces are actually recreated as needed.</span></span> 

<span data-ttu-id="479a2-283">Isso, em particular, também inclui matrizes.</span><span class="sxs-lookup"><span data-stu-id="479a2-283">This in particular also includes arrays.</span></span>
<span data-ttu-id="479a2-284">Em particular, não é possível atualizar itens de matriz.</span><span class="sxs-lookup"><span data-stu-id="479a2-284">In particular, it is not possible to update array items.</span></span> <span data-ttu-id="479a2-285">Para modificar uma matriz existente, é necessário aproveitar um mecanismo de *copiar e atualizar* .</span><span class="sxs-lookup"><span data-stu-id="479a2-285">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="479a2-286">Novas matrizes podem ser criadas a partir de existentes por meio de expressões *de copiar e atualizar* .</span><span class="sxs-lookup"><span data-stu-id="479a2-286">New arrays can be created from existing ones via *copy-and-update* expressions.</span></span>
<span data-ttu-id="479a2-287">Uma expressão de copiar e atualizar é uma expressão do formulário `expression1 w/ expression2 <- expression3` , onde `expression1` deve ser do tipo `T[]` para algum tipo `T` .</span><span class="sxs-lookup"><span data-stu-id="479a2-287">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span>
<span data-ttu-id="479a2-288">O segundo `expression2` define os índices dos elementos a serem modificados em comparação com a matriz em `expression1` e deve ser do tipo `Int` ou do tipo `Range` .</span><span class="sxs-lookup"><span data-stu-id="479a2-288">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span>
<span data-ttu-id="479a2-289">Se `expression2` for do tipo `Int` , `expression3` deve ser do tipo `T` .</span><span class="sxs-lookup"><span data-stu-id="479a2-289">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="479a2-290">Se `expression2` for do tipo `Range` , `expression3` deve ser do tipo `T[]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-290">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="479a2-291">Uma expressão de copiar e atualizar `arr w/ idx <- value` constrói uma nova matriz com todos os elementos definidos para o elemento correspondente no `arr` , exceto para os elementos em `idx` , que são definidos como os (s) em `value` .</span><span class="sxs-lookup"><span data-stu-id="479a2-291">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="479a2-292">Por exemplo, se `arr` contiver uma matriz `[0,1,2,3]` ,</span><span class="sxs-lookup"><span data-stu-id="479a2-292">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="479a2-293">`arr w/ 0 <- 10`é a matriz `[10,1,2,3]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-293">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="479a2-294">`arr w/ 2 <- 10`é a matriz `[0,1,10,3]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-294">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="479a2-295">`arr w/ 0..2..3 <- [10,12]`é a matriz `[10,1,12,3]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-295">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="479a2-296">Copiar e atualizar expressões para itens nomeados</span><span class="sxs-lookup"><span data-stu-id="479a2-296">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="479a2-297">Existem expressões semelhantes para itens nomeados em tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="479a2-297">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="479a2-298">Considere, por exemplo, o tipo</span><span class="sxs-lookup"><span data-stu-id="479a2-298">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="479a2-299">Se `c` contiver o valor do tipo `Complex(1., -1.)` , `c w/ Re <- 0.` será uma expressão do tipo `Complex` que é avaliada como `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="479a2-299">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="479a2-300">Matrizes denteadas</span><span class="sxs-lookup"><span data-stu-id="479a2-300">Jagged Arrays</span></span>

<span data-ttu-id="479a2-301">Uma matriz denteada, às vezes chamada de "matriz de matrizes", é uma matriz cujos elementos são matrizes.</span><span class="sxs-lookup"><span data-stu-id="479a2-301">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="479a2-302">Os elementos de uma matriz denteada podem ser de tamanhos diferentes.</span><span class="sxs-lookup"><span data-stu-id="479a2-302">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="479a2-303">O exemplo a seguir mostra como declarar e inicializar uma matriz denteada que representa uma tabela de multiplicação.</span><span class="sxs-lookup"><span data-stu-id="479a2-303">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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

### <a name="arrays-of-callables"></a><span data-ttu-id="479a2-304">Matrizes de callablefiles</span><span class="sxs-lookup"><span data-stu-id="479a2-304">Arrays of callables</span></span> 

<span data-ttu-id="479a2-305">Observe que mais detalhes sobre os tipos callable podem ser encontrados abaixo, bem como na próxima página, [operações e funções em Q #](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="479a2-305">Note that more details on callable types can be found below, as well as on the next page, [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

<span data-ttu-id="479a2-306">Se o tipo de elemento comum for uma operação ou tipo de função, todos os elementos deverão ter os mesmos tipos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="479a2-306">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="479a2-307">O tipo de elemento da matriz dará suporte a qualquer transmissão functors que tenha suporte de todos os elementos.</span><span class="sxs-lookup"><span data-stu-id="479a2-307">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="479a2-308">Por exemplo, se `Op1` , `Op2` , e `Op3` todos forem `Qubit[] => Unit` , mas o oferecer suporte a, o oferece suporte a `Op1` `Adjoint` `Op2` `Controlled` , e `Op3` dá suporte a ambos:</span><span class="sxs-lookup"><span data-stu-id="479a2-308">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="479a2-309">`[Op1, Op2]`é uma matriz de `(Qubit[] => Unit)` operações.</span><span class="sxs-lookup"><span data-stu-id="479a2-309">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="479a2-310">`[Op1, Op3]`é uma matriz de `(Qubit[] => Unit is Adj)` operações.</span><span class="sxs-lookup"><span data-stu-id="479a2-310">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="479a2-311">`[Op2, Op3]`é uma matriz de `(Qubit[] => Unit is Ctl)` operações.</span><span class="sxs-lookup"><span data-stu-id="479a2-311">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="479a2-312">No entanto, enquanto `(Qubit[] => Unit is Adj)` `(Qubit[] => Unit is Ctl)` as operações têm o tipo base comum de `(Qubit[] => Unit)` , observe *of* que as matrizes desses operadores não compartilham um tipo base comum.</span><span class="sxs-lookup"><span data-stu-id="479a2-312">However, while `(Qubit[] => Unit is Adj)` and  `(Qubit[] => Unit is Ctl)` operations have the common base type of `(Qubit[] => Unit)`, note that arrays *of* these operators do not share a common base type.</span></span> <span data-ttu-id="479a2-313">Por exemplo, `[[Op1], [Op2]]` no momento, o geraria um erro porque ele está tentando criar uma matriz dos tipos de matriz incompatíveis `(Qubit[] => Unit is Adj)[]` e `(Qubit[] => Unit is Ctl)[]` .</span><span class="sxs-lookup"><span data-stu-id="479a2-313">For example, `[[Op1], [Op2]]` would currently raise an error because it is attempting to create an array of the incompatible array types `(Qubit[] => Unit is Adj)[]` and `(Qubit[] => Unit is Ctl)[]`.</span></span>


## <a name="conditional-expressions"></a><span data-ttu-id="479a2-314">Expressões condicionais</span><span class="sxs-lookup"><span data-stu-id="479a2-314">Conditional Expressions</span></span>

<span data-ttu-id="479a2-315">Dadas duas outras expressões do mesmo tipo e uma expressão booliana, a expressão condicional pode ser formada usando o ponto de interrogação `?` e a barra vertical `|` .</span><span class="sxs-lookup"><span data-stu-id="479a2-315">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="479a2-316">Por exemplo, `a==b ? c | d` .</span><span class="sxs-lookup"><span data-stu-id="479a2-316">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="479a2-317">Neste exemplo, o valor da expressão condicional será `c` se `a==b` for true e `d` se for false.</span><span class="sxs-lookup"><span data-stu-id="479a2-317">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="479a2-318">Expressões condicionais com callablefiles</span><span class="sxs-lookup"><span data-stu-id="479a2-318">Conditional expressions with callables</span></span>

<span data-ttu-id="479a2-319">As duas expressões podem ser avaliadas como operações que têm as mesmas entradas e saídas, mas dão suporte a diferentes transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="479a2-319">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="479a2-320">Nesse caso, o tipo da expressão condicional é uma operação com as entradas e saídas que dão suporte a qualquer transmissão functors com suporte em ambas as expressões.</span><span class="sxs-lookup"><span data-stu-id="479a2-320">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="479a2-321">Por exemplo, se `Op1` , `Op2` , e `Op3` todos forem `Qubit[]=>Unit` , mas o oferecer suporte a, o oferece suporte a `Op1` `Adjoint` `Op2` `Controlled` , e `Op3` dá suporte a ambos:</span><span class="sxs-lookup"><span data-stu-id="479a2-321">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="479a2-322">`flag ? Op1 | Op2`é uma `(Qubit[] => Unit)` operação.</span><span class="sxs-lookup"><span data-stu-id="479a2-322">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="479a2-323">`flag ? Op1 | Op3`é uma `(Qubit[] => Unit is Adj)` operação.</span><span class="sxs-lookup"><span data-stu-id="479a2-323">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="479a2-324">`flag ? Op2 | Op3`é uma `(Qubit[] => Unit is Ctl)` operação.</span><span class="sxs-lookup"><span data-stu-id="479a2-324">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="479a2-325">Se qualquer uma das duas expressões de resultado possíveis incluir uma função ou uma chamada de operação, essa chamada só ocorrerá se o resultado for aquele que será o valor da chamada.</span><span class="sxs-lookup"><span data-stu-id="479a2-325">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="479a2-326">Por exemplo, no caso `a==b ? C(qs) | D(qs)` , se `a==b` for true, a `C` operação será invocada e, se for false, somente `D` será invocada.</span><span class="sxs-lookup"><span data-stu-id="479a2-326">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="479a2-327">Isso é semelhante ao curto circuito em outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="479a2-327">This is similar to short-circuiting in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="479a2-328">Expressões que podem ser chamadas</span><span class="sxs-lookup"><span data-stu-id="479a2-328">Callable Expressions</span></span>

<span data-ttu-id="479a2-329">Um literal que pôde ser chamado é o nome de uma operação ou função definida no escopo de compilação.</span><span class="sxs-lookup"><span data-stu-id="479a2-329">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="479a2-330">Por exemplo, `X` é um literal de operação que se refere à operação de biblioteca padrão `X` e `Message` é um literal de função que se refere à função de biblioteca padrão `Message` .</span><span class="sxs-lookup"><span data-stu-id="479a2-330">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="479a2-331">Se uma operação oferecer suporte a `Adjoint` functor, `Adjoint op` será uma expressão de operação.</span><span class="sxs-lookup"><span data-stu-id="479a2-331">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="479a2-332">Da mesma forma, se a operação oferecer suporte a `Controlled` functor, `Controlled op` será uma expressão de operação.</span><span class="sxs-lookup"><span data-stu-id="479a2-332">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="479a2-333">Os tipos dessas expressões são especificados na [chamada de especializações de operação](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span><span class="sxs-lookup"><span data-stu-id="479a2-333">The types of these expressions are specified at [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="479a2-334">Transmissão functors ( `Adjoint` e `Controlled` ) associam-se mais de todos os outros operadores, exceto para o operador de desencapsulamento `!` e indexação de matriz com [] ".</span><span class="sxs-lookup"><span data-stu-id="479a2-334">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with []\`.</span></span>
<span data-ttu-id="479a2-335">Portanto, as seguintes são todas legais, supondo que as operações suportam o transmissão functors usado:</span><span class="sxs-lookup"><span data-stu-id="479a2-335">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="479a2-336">Expressões callable parametrizadas de tipo</span><span class="sxs-lookup"><span data-stu-id="479a2-336">Type-parameterized callable expressions</span></span>

<span data-ttu-id="479a2-337">Um literal resgatável pode ser usado como um valor, digamos para atribuir a uma variável ou passar para outro callable.</span><span class="sxs-lookup"><span data-stu-id="479a2-337">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="479a2-338">Nesse caso, se o callable tiver [parâmetros de tipo](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), eles deverão ser fornecidos como parte do valor que pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="479a2-338">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), they must be provided as part of the callable value.</span></span>
<span data-ttu-id="479a2-339">Um valor callable não pode ter nenhum parâmetro de tipo não especificado.</span><span class="sxs-lookup"><span data-stu-id="479a2-339">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="479a2-340">Por exemplo, se `Fun` é uma função com assinatura `'T1->Unit` :</span><span class="sxs-lookup"><span data-stu-id="479a2-340">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="479a2-341">Expressões de invocação que podem ser chamadas</span><span class="sxs-lookup"><span data-stu-id="479a2-341">Callable Invocation Expressions</span></span>

<span data-ttu-id="479a2-342">Dada uma expressão resgatável (operação ou função) e uma expressão de tupla do tipo de entrada da assinatura do callable, uma expressão de invocação pode ser formada acrescentando-se a expressão de tupla à expressão que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="479a2-342">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="479a2-343">O tipo da expressão de invocação é o tipo de saída da assinatura do callable.</span><span class="sxs-lookup"><span data-stu-id="479a2-343">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="479a2-344">Por exemplo, se `Op` for uma operação com assinatura `((Int, Qubit) => Double)` , `Op(3, qubit1)` é uma expressão do tipo `Double` .</span><span class="sxs-lookup"><span data-stu-id="479a2-344">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="479a2-345">Da mesma forma, se `Sin` é uma função com assinatura `(Double -> Double)` , `Sin(0.1)` é uma expressão do tipo `Double` .</span><span class="sxs-lookup"><span data-stu-id="479a2-345">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="479a2-346">Por fim, se `Builder` for uma função com assinatura `(Int -> (Int -> Int))` , `Builder(3)` será uma função de em para int.</span><span class="sxs-lookup"><span data-stu-id="479a2-346">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="479a2-347">Invocar o resultado de uma expressão com valor callable requer um par extra de parênteses em volta da expressão callable.</span><span class="sxs-lookup"><span data-stu-id="479a2-347">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="479a2-348">Portanto, para invocar o resultado da chamada `Builder` do parágrafo anterior, a sintaxe correta é:</span><span class="sxs-lookup"><span data-stu-id="479a2-348">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="479a2-349">Ao invocar um callable [com parâmetros de tipo](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) , os parâmetros do tipo real podem ser especificados entre colchetes angulares `<` e `>` após a expressão que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="479a2-349">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="479a2-350">Isso geralmente é desnecessário, pois o compilador Q # inferirá os tipos reais.</span><span class="sxs-lookup"><span data-stu-id="479a2-350">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="479a2-351">No entanto, ele *será* necessário para o [aplicativo parcial](xref:microsoft.quantum.guide.operationsfunctions#partial-application) se um argumento de tipo parametrizado for deixado não especificado.</span><span class="sxs-lookup"><span data-stu-id="479a2-351">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="479a2-352">Às vezes, também é útil ao passar operações com functor diferentes para um callable.</span><span class="sxs-lookup"><span data-stu-id="479a2-352">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="479a2-353">Por exemplo, se `Func` tem assinatura `('T1, 'T2, 'T1) -> 'T2` `Op1` e tem assinatura e `Op2` `(Qubit[] => Unit is Adj)` `Op3` tem assinatura `(Qubit[] => Unit)` , para invocar `Func` com `Op1` como o primeiro argumento, `Op2` como o segundo, e `Op3` como o terceiro:</span><span class="sxs-lookup"><span data-stu-id="479a2-353">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="479a2-354">A especificação de tipo é necessária porque `Op3` e `Op1` tem tipos diferentes, portanto, o compilador tratará isso como ambíguo sem a especificação.</span><span class="sxs-lookup"><span data-stu-id="479a2-354">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="479a2-355">Precedência de operador</span><span class="sxs-lookup"><span data-stu-id="479a2-355">Operator Precedence</span></span>

<span data-ttu-id="479a2-356">Todos os operadores binários são associativos à direita, exceto para `^` .</span><span class="sxs-lookup"><span data-stu-id="479a2-356">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="479a2-357">Colchetes e `[` `]` , para a divisão e a indexação de matriz, associe antes de qualquer operador.</span><span class="sxs-lookup"><span data-stu-id="479a2-357">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="479a2-358">A transmissão functors `Adjoint` e a `Controlled` Associação após a indexação da matriz, mas antes de todos os outros operadores.</span><span class="sxs-lookup"><span data-stu-id="479a2-358">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="479a2-359">Parênteses para operação e invocação de função também são associados antes de qualquer operador, mas após a indexação de matriz e transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="479a2-359">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="479a2-360">Operadores em ordem de precedência, do mais alto ao mais baixo:</span><span class="sxs-lookup"><span data-stu-id="479a2-360">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="479a2-361">Operador</span><span class="sxs-lookup"><span data-stu-id="479a2-361">Operator</span></span> | <span data-ttu-id="479a2-362">Arity</span><span class="sxs-lookup"><span data-stu-id="479a2-362">Arity</span></span> | <span data-ttu-id="479a2-363">Descrição</span><span class="sxs-lookup"><span data-stu-id="479a2-363">Description</span></span> | <span data-ttu-id="479a2-364">Tipos de operando</span><span class="sxs-lookup"><span data-stu-id="479a2-364">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="479a2-365">à direita`!`</span><span class="sxs-lookup"><span data-stu-id="479a2-365">trailing `!`</span></span> | <span data-ttu-id="479a2-366">Unário</span><span class="sxs-lookup"><span data-stu-id="479a2-366">Unary</span></span> | <span data-ttu-id="479a2-367">Desencapsular</span><span class="sxs-lookup"><span data-stu-id="479a2-367">Unwrap</span></span> | <span data-ttu-id="479a2-368">Qualquer tipo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="479a2-368">Any user-defined type</span></span>
 <span data-ttu-id="479a2-369">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="479a2-369">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="479a2-370">Unário</span><span class="sxs-lookup"><span data-stu-id="479a2-370">Unary</span></span> | <span data-ttu-id="479a2-371">Numérico negativo, complemento de bit-nte, negação lógica</span><span class="sxs-lookup"><span data-stu-id="479a2-371">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="479a2-372">`Int`, `BigInt` ou `Double` para `-` , `Int` ou `BigInt` para `~~~` , `Bool` para`not`</span><span class="sxs-lookup"><span data-stu-id="479a2-372">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="479a2-373">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-373">Binary</span></span> | <span data-ttu-id="479a2-374">Potência de inteiro</span><span class="sxs-lookup"><span data-stu-id="479a2-374">Integer power</span></span> | <span data-ttu-id="479a2-375">`Int`ou `BigInt` para a base, `Int` para o expoente</span><span class="sxs-lookup"><span data-stu-id="479a2-375">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="479a2-376">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="479a2-376">`/`, `*`, `%`</span></span> | <span data-ttu-id="479a2-377">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-377">Binary</span></span> | <span data-ttu-id="479a2-378">Divisão, multiplicação, módulo de inteiro</span><span class="sxs-lookup"><span data-stu-id="479a2-378">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="479a2-379">`Int`, `BigInt` ou `Double` para `/` e `*` , `Int` ou `BigInt` para`%`</span><span class="sxs-lookup"><span data-stu-id="479a2-379">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="479a2-380">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="479a2-380">`+`, `-`</span></span> | <span data-ttu-id="479a2-381">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-381">Binary</span></span> | <span data-ttu-id="479a2-382">Adição ou concatenação de cadeia de caracteres e matriz, subtração</span><span class="sxs-lookup"><span data-stu-id="479a2-382">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="479a2-383">`Int`, `BigInt` ou `Double` , além disso, `String` ou qualquer tipo de matriz para`+`</span><span class="sxs-lookup"><span data-stu-id="479a2-383">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="479a2-384">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="479a2-384">`<<<`, `>>>`</span></span> | <span data-ttu-id="479a2-385">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-385">Binary</span></span> | <span data-ttu-id="479a2-386">Deslocamento à esquerda, deslocamento à direita</span><span class="sxs-lookup"><span data-stu-id="479a2-386">Left shift, right shift</span></span> | <span data-ttu-id="479a2-387">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="479a2-387">`Int` or `BigInt`</span></span>
 <span data-ttu-id="479a2-388">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="479a2-388">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="479a2-389">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-389">Binary</span></span> | <span data-ttu-id="479a2-390">Comparações de menor que, menor que ou igual a, maior que, maior que ou igual a</span><span class="sxs-lookup"><span data-stu-id="479a2-390">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="479a2-391">`Int``BigInt`ou`Double`</span><span class="sxs-lookup"><span data-stu-id="479a2-391">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="479a2-392">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="479a2-392">`==`, `!=`</span></span> | <span data-ttu-id="479a2-393">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-393">Binary</span></span> | <span data-ttu-id="479a2-394">comparações iguais, não iguais</span><span class="sxs-lookup"><span data-stu-id="479a2-394">equal, not-equal comparisons</span></span> | <span data-ttu-id="479a2-395">qualquer tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="479a2-395">any primitive type</span></span>
 `&&&` | <span data-ttu-id="479a2-396">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-396">Binary</span></span> | <span data-ttu-id="479a2-397">AND bit a bit</span><span class="sxs-lookup"><span data-stu-id="479a2-397">Bitwise AND</span></span> | <span data-ttu-id="479a2-398">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="479a2-398">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="479a2-399">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-399">Binary</span></span> | <span data-ttu-id="479a2-400">XOR bit a bit</span><span class="sxs-lookup"><span data-stu-id="479a2-400">Bitwise XOR</span></span> | <span data-ttu-id="479a2-401">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="479a2-401">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="479a2-402">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-402">Binary</span></span> | <span data-ttu-id="479a2-403">OR bit a bit</span><span class="sxs-lookup"><span data-stu-id="479a2-403">Bitwise OR</span></span> | <span data-ttu-id="479a2-404">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="479a2-404">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="479a2-405">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-405">Binary</span></span> | <span data-ttu-id="479a2-406">AND lógico</span><span class="sxs-lookup"><span data-stu-id="479a2-406">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="479a2-407">Binário</span><span class="sxs-lookup"><span data-stu-id="479a2-407">Binary</span></span> | <span data-ttu-id="479a2-408">OR lógico</span><span class="sxs-lookup"><span data-stu-id="479a2-408">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="479a2-409">Binary/ternário</span><span class="sxs-lookup"><span data-stu-id="479a2-409">Binary/Ternary</span></span> | <span data-ttu-id="479a2-410">Operador de intervalo</span><span class="sxs-lookup"><span data-stu-id="479a2-410">Range operator</span></span> | `Int`
 <span data-ttu-id="479a2-411">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="479a2-411">`?` `|`</span></span> | <span data-ttu-id="479a2-412">Ternário</span><span class="sxs-lookup"><span data-stu-id="479a2-412">Ternary</span></span> | <span data-ttu-id="479a2-413">Condicional</span><span class="sxs-lookup"><span data-stu-id="479a2-413">Conditional</span></span> | <span data-ttu-id="479a2-414">`Bool`para o lado esquerdo</span><span class="sxs-lookup"><span data-stu-id="479a2-414">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="479a2-415">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="479a2-415">`w/` `<-`</span></span> | <span data-ttu-id="479a2-416">Ternário</span><span class="sxs-lookup"><span data-stu-id="479a2-416">Ternary</span></span> | <span data-ttu-id="479a2-417">Copiar e atualizar</span><span class="sxs-lookup"><span data-stu-id="479a2-417">Copy-and-update</span></span> | <span data-ttu-id="479a2-418">consulte [expressões de copiar e atualizar](#copy-and-update-expressions)</span><span class="sxs-lookup"><span data-stu-id="479a2-418">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="next-steps"></a><span data-ttu-id="479a2-419">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="479a2-419">Next steps</span></span>

<span data-ttu-id="479a2-420">Agora que você pode trabalhar com expressões em Q #, você pode ir para [operações e funções em q #](xref:microsoft.quantum.guide.operationsfunctions) para saber como definir e chamar operações e funções.</span><span class="sxs-lookup"><span data-stu-id="479a2-420">Now that you can work with expressions in Q#, you can head to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
