---
title: Expressões em Q#
description: Entenda como especificar, referenciar e combinar constantes, variáveis, operadores, operações e funções como expressões no Q# .
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9bf28e3854eae1892692d7ca840e1860de2e2934
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835835"
---
# <a name="expressions-in-no-locq"></a><span data-ttu-id="5e244-103">Expressões em Q#</span><span class="sxs-lookup"><span data-stu-id="5e244-103">Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="5e244-104">Expressões numéricas</span><span class="sxs-lookup"><span data-stu-id="5e244-104">Numeric Expressions</span></span>

<span data-ttu-id="5e244-105">Expressões numéricas são expressões do tipo `Int` , `BigInt` ou `Double` .</span><span class="sxs-lookup"><span data-stu-id="5e244-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="5e244-106">Ou seja, eles são números inteiros ou de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="5e244-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="5e244-107">`Int` os literais no Q# são gravados como uma sequência de dígitos.</span><span class="sxs-lookup"><span data-stu-id="5e244-107">`Int` literals in Q# are written as a sequence of digits.</span></span>
<span data-ttu-id="5e244-108">Os inteiros hexadecimais e binários têm suporte e são gravados com um `0x` `0b` prefixo e, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5e244-108">Hexadecimal and binary integers are supported and written with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="5e244-109">`BigInt` os literais no Q# têm um `l` sufixo ou à direita `L` .</span><span class="sxs-lookup"><span data-stu-id="5e244-109">`BigInt` literals in Q# have a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="5e244-110">Há suporte para inteiros grandes hexadecimais e gravados com um prefixo "0x".</span><span class="sxs-lookup"><span data-stu-id="5e244-110">Hexadecimal big integers are supported and written with a "0x" prefix.</span></span>
<span data-ttu-id="5e244-111">Portanto, veja a seguir todos os usos válidos de `BigInt` literais:</span><span class="sxs-lookup"><span data-stu-id="5e244-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="5e244-112">`Double` os literais no Q# são números de ponto flutuante gravados usando dígitos decimais.</span><span class="sxs-lookup"><span data-stu-id="5e244-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="5e244-113">Eles podem ser escritos com ou sem um ponto decimal, `.` ou uma parte exponencial indicada com ' e ' ou ' e ' (após o qual apenas um possível sinal negativo e dígitos decimais são válidos).</span><span class="sxs-lookup"><span data-stu-id="5e244-113">They can be written with or without a decimal point, `.`, or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="5e244-114">Os seguintes são `Double` literais válidos: `0.0` , `1.2e5` , `1e-5` .</span><span class="sxs-lookup"><span data-stu-id="5e244-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="5e244-115">Dada uma expressão de matriz de qualquer tipo de elemento, você pode formar uma `Int` expressão usando a [`Length`](xref:microsoft.quantum.core.length) função interna, com a expressão de matriz entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="5e244-115">Given an array expression of any element type, you can form an `Int` expression using the [`Length`](xref:microsoft.quantum.core.length) built-in function, with the array expression enclosed in parentheses.</span></span>
<span data-ttu-id="5e244-116">Por exemplo, se `a` estiver associado a uma matriz, `Length(a)` será uma expressão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="5e244-116">For example, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="5e244-117">Se `b` é uma matriz de matrizes de inteiros, `Int[][]` , `Length(b)` é o número de submatrizes em `b` e `Length(b[1])` é o número de inteiros na segunda submatriz no `b` .</span><span class="sxs-lookup"><span data-stu-id="5e244-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="5e244-118">Dadas duas expressões numéricas do mesmo tipo, os operadores binários,, `+` `-` `*` e `/` podem ser usados para formar uma nova expressão numérica.</span><span class="sxs-lookup"><span data-stu-id="5e244-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="5e244-119">O tipo da nova expressão é o mesmo que os tipos das expressões constituintes.</span><span class="sxs-lookup"><span data-stu-id="5e244-119">The type of the new expression is the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="5e244-120">Dadas duas expressões de inteiro, use o operador Binary `^` (Power) para formar uma nova expressão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="5e244-120">Given two integer expressions, use the binary operator `^` (power) to form a new integer expression.</span></span>
<span data-ttu-id="5e244-121">Da mesma forma, você também pode usar `^` com duas expressões duplas para formar uma nova expressão Double.</span><span class="sxs-lookup"><span data-stu-id="5e244-121">Similarly, you can also use `^` with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="5e244-122">Por fim, você pode usar `^` com um inteiro grande à esquerda e um inteiro à direita para formar uma nova expressão de inteiro grande.</span><span class="sxs-lookup"><span data-stu-id="5e244-122">Finally, you can use `^` with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="5e244-123">Nesse caso, o segundo parâmetro deve caber em 32 bits; caso contrário, ele gera um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5e244-123">In this case, the second parameter must fit into 32 bits; if not, it raises a runtime error.</span></span>

<span data-ttu-id="5e244-124">Dadas duas expressões de inteiro ou grandes inteiros, formate um novo inteiro ou uma expressão de inteiro grande usando os `%` operadores (módulo), `&&&` (bit e), (OR bit a bit `|||` ) ou `^^^` (XOR).</span><span class="sxs-lookup"><span data-stu-id="5e244-124">Given two integer or big integer expressions, form a new integer or big integer expression using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="5e244-125">Dado um inteiro ou uma expressão de inteiro grande à esquerda e uma expressão de inteiro à direita, use os `<<<` operadores (deslocamento aritmético à esquerda) ou `>>>` (deslocamento aritmético à direita) para criar uma nova expressão com o mesmo tipo que a expressão esquerda.</span><span class="sxs-lookup"><span data-stu-id="5e244-125">Given either an integer or big integer expression on the left, and an integer expression on the right, use the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="5e244-126">O segundo parâmetro (o valor de deslocamento) para a operação de deslocamento deve ser maior ou igual a zero; o comportamento para valores de deslocamento negativos é indefinido.</span><span class="sxs-lookup"><span data-stu-id="5e244-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="5e244-127">O valor de deslocamento para uma das operações de deslocamento também deve se ajustar a 32 bits; caso contrário, ele gera um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5e244-127">The shift amount for either shift operation must also fit into 32 bits; if not, it raises a runtime error.</span></span>
<span data-ttu-id="5e244-128">Se o número deslocado for um inteiro, o valor de deslocamento será interpretado `mod 64` ; ou seja, um deslocamento de 1 e um deslocamento de 65 terão o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="5e244-128">If the number shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="5e244-129">Para os valores inteiros e inteiros grandes, as turnos são aritméticas.</span><span class="sxs-lookup"><span data-stu-id="5e244-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="5e244-130">A mudança de um valor negativo para a esquerda ou para a direita resulta em um número negativo.</span><span class="sxs-lookup"><span data-stu-id="5e244-130">Shifting a negative value either left or right results in a negative number.</span></span>
<span data-ttu-id="5e244-131">Ou seja, mudar uma etapa para a esquerda ou para a direita é o mesmo que multiplicar ou dividir por 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5e244-131">That is, shifting one step to the left or right is the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="5e244-132">Divisão de inteiros e módulo de inteiro seguem o mesmo comportamento para números negativos em C#.</span><span class="sxs-lookup"><span data-stu-id="5e244-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span> <span data-ttu-id="5e244-133">Ou seja, `a % b` sempre tem o mesmo sinal como `a` e `b * (a / b) + a % b` sempre é igual a `a` .</span><span class="sxs-lookup"><span data-stu-id="5e244-133">That is, `a % b` always has the same sign as `a`, and `b * (a / b) + a % b` always equals `a`.</span></span> <span data-ttu-id="5e244-134">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5e244-134">For example:</span></span>

|`A` | `B` | `A / B` | `A % B`|
|:---------:|:----------:|:---------:|:---------:|
| <span data-ttu-id="5e244-135">5</span><span class="sxs-lookup"><span data-stu-id="5e244-135">5</span></span> | <span data-ttu-id="5e244-136">2</span><span class="sxs-lookup"><span data-stu-id="5e244-136">2</span></span> | <span data-ttu-id="5e244-137">2</span><span class="sxs-lookup"><span data-stu-id="5e244-137">2</span></span> | <span data-ttu-id="5e244-138">1</span><span class="sxs-lookup"><span data-stu-id="5e244-138">1</span></span> |
| <span data-ttu-id="5e244-139">5</span><span class="sxs-lookup"><span data-stu-id="5e244-139">5</span></span> | <span data-ttu-id="5e244-140">-2</span><span class="sxs-lookup"><span data-stu-id="5e244-140">-2</span></span> | <span data-ttu-id="5e244-141">-2</span><span class="sxs-lookup"><span data-stu-id="5e244-141">-2</span></span> | <span data-ttu-id="5e244-142">1</span><span class="sxs-lookup"><span data-stu-id="5e244-142">1</span></span> |
| <span data-ttu-id="5e244-143">-5</span><span class="sxs-lookup"><span data-stu-id="5e244-143">-5</span></span> | <span data-ttu-id="5e244-144">2</span><span class="sxs-lookup"><span data-stu-id="5e244-144">2</span></span> | <span data-ttu-id="5e244-145">-2</span><span class="sxs-lookup"><span data-stu-id="5e244-145">-2</span></span> | <span data-ttu-id="5e244-146">-1</span><span class="sxs-lookup"><span data-stu-id="5e244-146">-1</span></span> |
| <span data-ttu-id="5e244-147">-5</span><span class="sxs-lookup"><span data-stu-id="5e244-147">-5</span></span> | <span data-ttu-id="5e244-148">-2</span><span class="sxs-lookup"><span data-stu-id="5e244-148">-2</span></span> | <span data-ttu-id="5e244-149">2</span><span class="sxs-lookup"><span data-stu-id="5e244-149">2</span></span> | <span data-ttu-id="5e244-150">-1</span><span class="sxs-lookup"><span data-stu-id="5e244-150">-1</span></span> |

<span data-ttu-id="5e244-151">A divisão de inteiro grande e as operações de módulo funcionam da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="5e244-151">Big integer division and modulus operations work the same way.</span></span>

<span data-ttu-id="5e244-152">Dada qualquer expressão numérica, você pode formar uma nova expressão usando o `-` operador unário.</span><span class="sxs-lookup"><span data-stu-id="5e244-152">Given any numeric expression, you can form a new expression using the `-` unary operator.</span></span>
<span data-ttu-id="5e244-153">A nova expressão é do mesmo tipo que a expressão constituir.</span><span class="sxs-lookup"><span data-stu-id="5e244-153">The new expression is the same type as the constituent expression.</span></span>

<span data-ttu-id="5e244-154">Dada qualquer inteiro ou expressão de inteiro grande, você pode formar uma nova expressão do mesmo tipo usando o `~~~` operador unário (complemento bit a bit).</span><span class="sxs-lookup"><span data-stu-id="5e244-154">Given any integer or big integer expression, you can form a new expression of the same type using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="5e244-155">Expressões boolianas</span><span class="sxs-lookup"><span data-stu-id="5e244-155">Boolean Expressions</span></span>

<span data-ttu-id="5e244-156">Os dois `Bool` valores literais são `true` e `false` .</span><span class="sxs-lookup"><span data-stu-id="5e244-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="5e244-157">Dadas as duas expressões do mesmo tipo primitivo, os `==` `!=` operadores binários e podem ser usados para construir uma `Bool` expressão.</span><span class="sxs-lookup"><span data-stu-id="5e244-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="5e244-158">A expressão será true se as duas expressões forem iguais e false se não.</span><span class="sxs-lookup"><span data-stu-id="5e244-158">The expression is true if the two expressions are equal and false if not.</span></span>

<span data-ttu-id="5e244-159">Os valores de tipos definidos pelo usuário não podem ser comparados, apenas seus valores não encapsulados podem ser comparados.</span><span class="sxs-lookup"><span data-stu-id="5e244-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="5e244-160">Por exemplo, usando o operador "sem encapsulamento" `!` (explicado em detalhes em [tipos Q# em ](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span><span class="sxs-lookup"><span data-stu-id="5e244-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="5e244-161">A comparação de igualdade para `Qubit` valores é igualdade de identidade; ou seja, se as duas expressões identificam o mesmo qubit.</span><span class="sxs-lookup"><span data-stu-id="5e244-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="5e244-162">Os Estados dos dois qubits não são comparados, acessados, medidos ou modificados por essa comparação.</span><span class="sxs-lookup"><span data-stu-id="5e244-162">The states of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="5e244-163">A comparação de igualdade para `Double` valores pode ser enganosa devido a efeitos de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="5e244-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="5e244-164">Por exemplo, `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="5e244-164">For example, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="5e244-165">Dadas quaisquer duas expressões numéricas, os operadores binários,, `>` `<` `>=` e `<=` podem ser usados para construir uma nova expressão booliana que seja verdadeira se a primeira expressão for maior que, menor que, maior ou igual ou menor ou igual à segunda expressão.</span><span class="sxs-lookup"><span data-stu-id="5e244-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="5e244-166">Dadas quaisquer duas expressões booleanas, use o `and` operador binário para construir uma nova expressão booliana que seja verdadeira se ambas as duas expressões forem verdadeiras.</span><span class="sxs-lookup"><span data-stu-id="5e244-166">Given any two Boolean expressions, use the `and` binary operator to construct a new Boolean expression that is true if both of the two expressions are true.</span></span> <span data-ttu-id="5e244-167">Da mesma forma, usar o `or` operador criará uma expressão que será verdadeira se uma das duas expressões for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="5e244-167">Likewise, using the `or` operator creates an expression that is true if either of the two expressions is true.</span></span>

<span data-ttu-id="5e244-168">Dada qualquer expressão booliana, o `not` operador unário pode ser usado para construir uma nova expressão booliana que seja verdadeira se a expressão constituinte for falsa.</span><span class="sxs-lookup"><span data-stu-id="5e244-168">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="5e244-169">Expressões de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="5e244-169">String expressions</span></span>

<span data-ttu-id="5e244-170">Q# permite que as cadeias de caracteres sejam usadas na `fail` instrução (explicada no [fluxo de controle](xref:microsoft.quantum.guide.controlflow#fail-statement)) e na [`Message`](xref:microsoft.quantum.intrinsic.message) função padrão.</span><span class="sxs-lookup"><span data-stu-id="5e244-170">Q# allows strings to be used in the `fail` statement (explained in [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:microsoft.quantum.intrinsic.message) standard function.</span></span> <span data-ttu-id="5e244-171">O comportamento específico do segundo depende do simulador usado, mas normalmente grava uma mensagem no console do host quando chamado durante um Q# programa.</span><span class="sxs-lookup"><span data-stu-id="5e244-171">The specific behavior of the latter depends on the simulator used but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="5e244-172">Cadeias de caracteres no Q# são literais ou cadeias de caracteres interpoladas.</span><span class="sxs-lookup"><span data-stu-id="5e244-172">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="5e244-173">Literais de cadeia de caracteres são semelhantes a literais de cadeia de caracteres simples na maioria dos idiomas: uma sequência de caracteres Unicode entre aspas duplas `" "` .</span><span class="sxs-lookup"><span data-stu-id="5e244-173">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double-quotes `" "`.</span></span>
<span data-ttu-id="5e244-174">Dentro de uma cadeia de caracteres, use o caractere de barra invertida `\` para escapar de um caractere de aspas duplas ( `\"` ) ou para inserir uma linha ( `\n` ), um retorno de carro ( `\r` ) ou uma tabulação ( `\t` ).</span><span class="sxs-lookup"><span data-stu-id="5e244-174">Inside of a string, use the backslash character `\` to escape a double-quote character (`\"`), or to insert a new-line ( `\n` ), a carriage return (`\r`), or a tab (`\t`).</span></span>
<span data-ttu-id="5e244-175">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5e244-175">For example:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="5e244-176">Cadeias de caracteres interpoladas</span><span class="sxs-lookup"><span data-stu-id="5e244-176">Interpolated strings</span></span>

<span data-ttu-id="5e244-177">A Q# sintaxe para interpolações de cadeia de caracteres é um subconjunto da sintaxe C#.</span><span class="sxs-lookup"><span data-stu-id="5e244-177">The Q# syntax for string interpolations is a subset of the C# syntax.</span></span> <span data-ttu-id="5e244-178">A seguir estão os principais pontos que pertencem a Q# :</span><span class="sxs-lookup"><span data-stu-id="5e244-178">Following are the key points as they pertain to Q#:</span></span>

* <span data-ttu-id="5e244-179">Para identificar uma literal de cadeia de caracteres como uma cadeia de caracteres interpolada, preceda-o com o símbolo `$`.</span><span class="sxs-lookup"><span data-stu-id="5e244-179">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span> <span data-ttu-id="5e244-180">Não pode haver nenhum espaço em branco entre o `$` e o `"` que inicia uma cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="5e244-180">There can be no white space between the `$` and the `"` that starts a string literal.</span></span>

* <span data-ttu-id="5e244-181">Veja a seguir um exemplo básico usando a [`Message`](xref:microsoft.quantum.intrinsic.message) função para gravar o resultado de uma medida no console, juntamente com outras Q# expressões.</span><span class="sxs-lookup"><span data-stu-id="5e244-181">The following is a basic example using the [`Message`](xref:microsoft.quantum.intrinsic.message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```

* <span data-ttu-id="5e244-182">Qualquer Q# expressão válida pode aparecer em uma cadeia de caracteres interpolada.</span><span class="sxs-lookup"><span data-stu-id="5e244-182">Any valid Q# expression may appear in an interpolated string.</span></span>

* <span data-ttu-id="5e244-183">As expressões dentro de uma cadeia de caracteres interpolada seguem a Q# sintaxe, e não a sintaxe C#.</span><span class="sxs-lookup"><span data-stu-id="5e244-183">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span> <span data-ttu-id="5e244-184">A distinção mais notável é que o não Q# oferece suporte a cadeias de caracteres interpoladas (várias linhas) textuais.</span><span class="sxs-lookup"><span data-stu-id="5e244-184">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>

<span data-ttu-id="5e244-185">Para obter mais detalhes sobre a sintaxe C#, consulte [*cadeias de caracteres interpoladas*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span><span class="sxs-lookup"><span data-stu-id="5e244-185">For more details about the C# syntax, see [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>

## <a name="range-expressions"></a><span data-ttu-id="5e244-186">Expressões de intervalo</span><span class="sxs-lookup"><span data-stu-id="5e244-186">Range Expressions</span></span>

<span data-ttu-id="5e244-187">Dadas todas as três `Int` expressões `start` , `step` e `stop` , a expressão `start .. step .. stop` é uma expressão de intervalo cujo primeiro elemento é `start` , o segundo elemento é, o `start+step` terceiro elemento é `start+step+step` , e assim por diante, até que você passe `stop` .</span><span class="sxs-lookup"><span data-stu-id="5e244-187">Given any three `Int` expressions `start`, `step`, and `stop`, the expression `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, and so on, until you pass `stop`.</span></span>
<span data-ttu-id="5e244-188">Um intervalo pode estar vazio se, por exemplo, `step` for positivo e `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="5e244-188">A range may be empty if, for example, `step` is positive and `stop < start`.</span></span>

<span data-ttu-id="5e244-189">O intervalo é inclusivo em ambas as extremidades.</span><span class="sxs-lookup"><span data-stu-id="5e244-189">The range is inclusive at both ends.</span></span> <span data-ttu-id="5e244-190">Ou seja, se a diferença entre `start` e `stop` for um inteiro múltiplo de `step` , o último elemento do intervalo será `stop` .</span><span class="sxs-lookup"><span data-stu-id="5e244-190">That is, if the difference between `start` and `stop` is an integer multiple of `step`, the last element of the range will be `stop`.</span></span>

<span data-ttu-id="5e244-191">Dadas as duas `Int` expressões `start` e `stop` , a expressão `start .. stop` é uma expressão de intervalo igual a `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="5e244-191">Given any two `Int` expressions `start` and `stop`, the expression `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="5e244-192">Observe que o implícito `step` é + 1, mesmo se `stop` for menor que `start` ; nesse caso, o intervalo estará vazio.</span><span class="sxs-lookup"><span data-stu-id="5e244-192">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="5e244-193">Alguns intervalos de exemplo são:</span><span class="sxs-lookup"><span data-stu-id="5e244-193">Some example ranges are:</span></span>

- <span data-ttu-id="5e244-194">`1..3` é o intervalo 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="5e244-194">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="5e244-195">`2..2..5` é o intervalo de 2, 4.</span><span class="sxs-lookup"><span data-stu-id="5e244-195">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="5e244-196">`2..2..6` é o intervalo de 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="5e244-196">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="5e244-197">`6..-2..2` é o intervalo de 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="5e244-197">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="5e244-198">`2..1` é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="5e244-198">`2..1` is the empty range.</span></span>
- <span data-ttu-id="5e244-199">`2..6..7` é o intervalo 2.</span><span class="sxs-lookup"><span data-stu-id="5e244-199">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="5e244-200">`2..2..1` é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="5e244-200">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="5e244-201">`1..-1..2` é o intervalo vazio.</span><span class="sxs-lookup"><span data-stu-id="5e244-201">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="5e244-202">Expressões qubit</span><span class="sxs-lookup"><span data-stu-id="5e244-202">Qubit Expressions</span></span>

<span data-ttu-id="5e244-203">As únicas `Qubit` expressões são símbolos que são associados a `Qubit` valores ou elementos de matriz de `Qubit` matrizes.</span><span class="sxs-lookup"><span data-stu-id="5e244-203">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="5e244-204">Não há `Qubit` literais.</span><span class="sxs-lookup"><span data-stu-id="5e244-204">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="5e244-205">Expressões Pauli</span><span class="sxs-lookup"><span data-stu-id="5e244-205">Pauli Expressions</span></span>

<span data-ttu-id="5e244-206">Os quatro `Pauli` valores, `PauliI` , `PauliX` , `PauliY` e `PauliZ` , são expressões válidas `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="5e244-206">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="5e244-207">Além disso, as únicas `Pauli` expressões são símbolos associados a `Pauli` valores ou elementos de matriz de `Pauli` matrizes.</span><span class="sxs-lookup"><span data-stu-id="5e244-207">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="5e244-208">Expressões de resultado</span><span class="sxs-lookup"><span data-stu-id="5e244-208">Result Expressions</span></span>

<span data-ttu-id="5e244-209">Os dois `Result` valores, `One` e `Zero` , são expressões válidas `Result` .</span><span class="sxs-lookup"><span data-stu-id="5e244-209">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="5e244-210">Além disso, as únicas `Result` expressões são símbolos associados a `Result` valores ou elementos de matriz de `Result` matrizes.</span><span class="sxs-lookup"><span data-stu-id="5e244-210">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="5e244-211">Em particular, observe que `One` não é o mesmo que o inteiro `1` , e não há nenhuma conversão direta entre eles.</span><span class="sxs-lookup"><span data-stu-id="5e244-211">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="5e244-212">O mesmo é verdadeiro para `Zero` e `0` .</span><span class="sxs-lookup"><span data-stu-id="5e244-212">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="5e244-213">Expressões de tupla</span><span class="sxs-lookup"><span data-stu-id="5e244-213">Tuple Expressions</span></span>

<span data-ttu-id="5e244-214">Um literal de tupla é uma sequência de expressões de elemento do tipo apropriado, separadas por vírgulas, delimitadas por parênteses.</span><span class="sxs-lookup"><span data-stu-id="5e244-214">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in parentheses.</span></span>
<span data-ttu-id="5e244-215">Por exemplo, `(1, One)` é uma `(Int, Result)` expressão.</span><span class="sxs-lookup"><span data-stu-id="5e244-215">For example, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="5e244-216">Além de literais, as únicas expressões de tupla são símbolos associados a valores de tupla, elementos de matriz de matrizes de tupla e invocações que retornam tuplas.</span><span class="sxs-lookup"><span data-stu-id="5e244-216">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="5e244-217">Expressões de tipo definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5e244-217">User-Defined Type Expressions</span></span>

<span data-ttu-id="5e244-218">Um literal de um tipo definido pelo usuário consiste no nome do tipo seguido por um literal de tupla do tipo de tupla base do tipo.</span><span class="sxs-lookup"><span data-stu-id="5e244-218">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="5e244-219">Por exemplo, se `IntPair` for um tipo definido pelo usuário baseado em `(Int, Int)` , `IntPair(2, 3)` será um literal válido desse tipo.</span><span class="sxs-lookup"><span data-stu-id="5e244-219">For example, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` is a valid literal of that type.</span></span>

<span data-ttu-id="5e244-220">Além de literais, as únicas expressões de um tipo definido pelo usuário são símbolos que são associados a valores desse tipo, elementos da matriz de matrizes desse tipo e invocações que retornam esse tipo.</span><span class="sxs-lookup"><span data-stu-id="5e244-220">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="5e244-221">Desencapsular expressões</span><span class="sxs-lookup"><span data-stu-id="5e244-221">Unwrap Expressions</span></span>

<span data-ttu-id="5e244-222">No Q# , o operador de desencapsulamento é um ponto de exclamação à direita `!` .</span><span class="sxs-lookup"><span data-stu-id="5e244-222">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="5e244-223">Por exemplo, se `IntPair` for um tipo definido pelo usuário com o tipo subjacente `(Int, Int)` e `s` for uma variável com valor `IntPair(2, 3)` , `s!` será `(2, 3)` .</span><span class="sxs-lookup"><span data-stu-id="5e244-223">For example, if `IntPair` is a user-defined type with the underlying type `(Int, Int)` and `s` is a variable with value `IntPair(2, 3)`, then `s!` is `(2, 3)`.</span></span>

<span data-ttu-id="5e244-224">Para tipos definidos pelo usuário definidos em termos de outros tipos definidos pelo usuário, você pode repetir o operador de desencapsulamento.</span><span class="sxs-lookup"><span data-stu-id="5e244-224">For user-defined types defined in terms of other user-defined types, you can repeat the unwrap operator.</span></span> <span data-ttu-id="5e244-225">Por exemplo, `s!!` indica o valor duplo não encapsulado de `s` .</span><span class="sxs-lookup"><span data-stu-id="5e244-225">For example, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="5e244-226">Portanto, se `WrappedPair` for um tipo definido pelo usuário com o tipo subjacente `IntPair` , e `t` for uma variável com valor `WrappedPair(IntPair(1,2))` , `t!!` será `(1,2)` .</span><span class="sxs-lookup"><span data-stu-id="5e244-226">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` is `(1,2)`.</span></span>

<span data-ttu-id="5e244-227">O `!` operador tem precedência maior do que todos os outros operadores diferentes de `[]` para indexação e divisão de matriz.</span><span class="sxs-lookup"><span data-stu-id="5e244-227">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="5e244-228">`!` e `[]` Associate posicionalmente, ou seja, `a[i]![3]` é lido como `((a[i])!)[3]` : Pegue o `i` elemento th `a` , desenvolva-o e, em seguida, obtenha o terceiro elemento do valor não encapsulado (que deve ser uma matriz).</span><span class="sxs-lookup"><span data-stu-id="5e244-228">`!` and `[]` bind positionally; that is, `a[i]![3]` is read as `((a[i])!)[3]`: take the `i`th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="5e244-229">A precedência do `!` operador tem um impacto que pode não ser óbvio.</span><span class="sxs-lookup"><span data-stu-id="5e244-229">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="5e244-230">Se uma função ou operação retorna um valor que, em seguida, é desencapsulada, a função ou a chamada de operação deve ser colocada entre parênteses para que a tupla de argumento seja associada à chamada em vez de ser desencapsulada.</span><span class="sxs-lookup"><span data-stu-id="5e244-230">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="5e244-231">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5e244-231">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="5e244-232">Expressões de matriz</span><span class="sxs-lookup"><span data-stu-id="5e244-232">Array Expressions</span></span>

<span data-ttu-id="5e244-233">Um literal de matriz é uma sequência de uma ou mais expressões de elemento, separadas por vírgulas, delimitadas entre colchetes `[]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-233">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in square brackets `[]`.</span></span>
<span data-ttu-id="5e244-234">Todos os elementos devem ser compatíveis com o mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="5e244-234">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="5e244-235">Dadas duas matrizes do mesmo tipo, use o `+` operador Binary para formar uma nova matriz que é a concatenação das duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="5e244-235">Given two arrays of the same type, use the binary `+` operator to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="5e244-236">Por exemplo, `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span><span class="sxs-lookup"><span data-stu-id="5e244-236">For example, `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="5e244-237">Criação de matriz</span><span class="sxs-lookup"><span data-stu-id="5e244-237">Array Creation</span></span>

<span data-ttu-id="5e244-238">Dado um tipo e uma `Int` expressão, use o `new` operador para alocar uma nova matriz do tamanho determinado.</span><span class="sxs-lookup"><span data-stu-id="5e244-238">Given a type and an `Int` expression, use the `new` operator to allocate a new array of the given size.</span></span>
<span data-ttu-id="5e244-239">Por exemplo, `new Int[i + 1]` aloca uma nova `Int` matriz com `i + 1` elementos.</span><span class="sxs-lookup"><span data-stu-id="5e244-239">For example, `new Int[i + 1]` allocates a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="5e244-240">Literais de matriz vazios, como `[]` , não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="5e244-240">Empty array literals, such as `[]`, are not allowed.</span></span>
<span data-ttu-id="5e244-241">Em vez disso, você pode criar uma matriz de comprimento zero usando `new T[0]` , em que `T` é um espaço reservado para um tipo adequado.</span><span class="sxs-lookup"><span data-stu-id="5e244-241">Instead, you can create an array of length zero by using `new T[0]`, where `T` is a placeholder for a suitable type.</span></span>

<span data-ttu-id="5e244-242">Os elementos de uma nova matriz são inicializados para um valor padrão dependente de tipo.</span><span class="sxs-lookup"><span data-stu-id="5e244-242">The elements of a new array initialize to a type-dependent default value.</span></span>
<span data-ttu-id="5e244-243">Na maioria dos casos, essa é uma variação de zero.</span><span class="sxs-lookup"><span data-stu-id="5e244-243">In most cases, this is some variation of zero.</span></span>

<span data-ttu-id="5e244-244">Para qubits e callableies, que são referências a entidades, não há nenhum valor padrão razoável.</span><span class="sxs-lookup"><span data-stu-id="5e244-244">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="5e244-245">Portanto, para esses tipos, o padrão é uma referência inválida que você não pode usar sem causar um erro de tempo de execução, semelhante a uma referência nula em linguagens como C# ou Java.</span><span class="sxs-lookup"><span data-stu-id="5e244-245">Thus, for these types, the default is an invalid reference that you cannot use without causing a runtime error, similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="5e244-246">As matrizes que contêm qubits ou callables devem ser inicializadas com valores não padrão antes de você poder usar seus elementos com segurança.</span><span class="sxs-lookup"><span data-stu-id="5e244-246">Arrays containing qubits or callables must be initialized with non-default values before you can use their elements safely.</span></span> <span data-ttu-id="5e244-247">Para rotinas de inicialização adequadas, consulte <xref:microsoft.quantum.arrays> .</span><span class="sxs-lookup"><span data-stu-id="5e244-247">For suitable initialization routines, see <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="5e244-248">Os valores padrão para cada tipo são:</span><span class="sxs-lookup"><span data-stu-id="5e244-248">The default values for each type are:</span></span>

<span data-ttu-id="5e244-249">Type</span><span class="sxs-lookup"><span data-stu-id="5e244-249">Type</span></span> | <span data-ttu-id="5e244-250">Padrão</span><span class="sxs-lookup"><span data-stu-id="5e244-250">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="5e244-251">_qubit inválido_</span><span class="sxs-lookup"><span data-stu-id="5e244-251">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="5e244-252">O intervalo vazio, `1..1..0`</span><span class="sxs-lookup"><span data-stu-id="5e244-252">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="5e244-253">_callable inválido_</span><span class="sxs-lookup"><span data-stu-id="5e244-253">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="5e244-254">Os tipos de tupla inicializam elemento por elemento.</span><span class="sxs-lookup"><span data-stu-id="5e244-254">Tuple types initialize element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="5e244-255">Elementos da matriz</span><span class="sxs-lookup"><span data-stu-id="5e244-255">Array Elements</span></span>

<span data-ttu-id="5e244-256">Dada uma expressão de matriz e uma `Int` expressão, formam uma nova expressão usando o operador de elemento de matriz `[]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-256">Given an array expression and an `Int` expression, form a new expression using the array element operator `[]`.</span></span>
<span data-ttu-id="5e244-257">A nova expressão é do mesmo tipo que o tipo de elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="5e244-257">The new expression is the same type as the element type of the array.</span></span>
<span data-ttu-id="5e244-258">Por exemplo, se `a` estiver associado a uma matriz do tipo `Double` , `a[4]` será uma `Double` expressão.</span><span class="sxs-lookup"><span data-stu-id="5e244-258">For example, if `a` is bound to an array of type `Double`, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="5e244-259">Se a expressão de matriz não for um identificador simples, você deverá colocá-la entre parênteses para selecionar um elemento.</span><span class="sxs-lookup"><span data-stu-id="5e244-259">If the array expression is not a simple identifier, you must enclose it in parentheses to select an element.</span></span>
<span data-ttu-id="5e244-260">Por exemplo, se `a` e `b` forem ambas matrizes do tipo `Int` , um elemento da concatenação será expresso como:</span><span class="sxs-lookup"><span data-stu-id="5e244-260">For example, if `a` and `b` are both arrays of type `Int`, an element from the concatenation is expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="5e244-261">Todas as matrizes no Q# são baseadas em zero.</span><span class="sxs-lookup"><span data-stu-id="5e244-261">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="5e244-262">Ou seja, o primeiro elemento de uma matriz `a` é sempre `a[0]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-262">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="5e244-263">Fatias de matriz</span><span class="sxs-lookup"><span data-stu-id="5e244-263">Array Slices</span></span>

<span data-ttu-id="5e244-264">Dada uma expressão de matriz e uma `Range` expressão, formam uma nova expressão usando o operador matriz de fatia `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-264">Given an array expression and a `Range` expression, form a new expression using the array slice operator `[ ]`.</span></span>
<span data-ttu-id="5e244-265">A nova expressão é do mesmo tipo que a matriz e contém os itens de matriz indexados pelos elementos de `Range` , na ordem definida pelo `Range` .</span><span class="sxs-lookup"><span data-stu-id="5e244-265">The new expression is the same type as the array and contains the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="5e244-266">Por exemplo, se `a` estiver associado a uma matriz do tipo `Double` , `a[3..-1..0]` é uma `Double[]` expressão que contém os quatro primeiros elementos de `a` , mas na ordem inversa, conforme eles aparecem `a` .</span><span class="sxs-lookup"><span data-stu-id="5e244-266">For example, if `a` is bound to an array of type `Double`, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="5e244-267">Se o `Range` estiver vazio, a fatia da matriz resultante terá comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="5e244-267">If the `Range` is empty, then the resulting array slice is zero length.</span></span>

<span data-ttu-id="5e244-268">Assim como ocorre com a referência de elementos de matriz, se a expressão de matriz não for um identificador simples, você deverá colocá-la entre parênteses para dividir a tabela.</span><span class="sxs-lookup"><span data-stu-id="5e244-268">Just as with referencing array elements, if the array expression is not a simple identifier, you must enclose it in parentheses to slice it.</span></span>
<span data-ttu-id="5e244-269">Por exemplo, se `a` e `b` forem ambas matrizes do tipo `Int` , uma fatia da concatenação será expressa como:</span><span class="sxs-lookup"><span data-stu-id="5e244-269">For example, if `a` and `b` are both arrays of type `Int`, a slice from the concatenation is expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="5e244-270">Valores de início/término inferidos</span><span class="sxs-lookup"><span data-stu-id="5e244-270">Inferred start/end values</span></span>

<span data-ttu-id="5e244-271">A partir da nossa [versão 0,8](xref:microsoft.quantum.relnotes), damos suporte a expressões contextuais para divisão de intervalo.</span><span class="sxs-lookup"><span data-stu-id="5e244-271">Starting with our [0.8 release](xref:microsoft.quantum.relnotes), we support contextual expressions for range slicing.</span></span> <span data-ttu-id="5e244-272">Em particular, você pode omitir os valores de início e término do intervalo no contexto de uma expressão de divisão de intervalo.</span><span class="sxs-lookup"><span data-stu-id="5e244-272">In particular, you may omit range start and end values in the context of a range slicing expression.</span></span> <span data-ttu-id="5e244-273">Nesse caso, o compilador aplica as seguintes regras para inferir os delimitadores pretendidos para o intervalo:</span><span class="sxs-lookup"><span data-stu-id="5e244-273">In that case, the compiler applies the following rules to infer the intended delimiters for the range:</span></span>

* <span data-ttu-id="5e244-274">Se o valor de *início* do intervalo for omitido, o valor inicial inferido</span><span class="sxs-lookup"><span data-stu-id="5e244-274">If the range *start* value is omitted, then the inferred start value</span></span>
  * <span data-ttu-id="5e244-275">será zero se nenhuma etapa for especificada ou se a etapa especificada for positiva.</span><span class="sxs-lookup"><span data-stu-id="5e244-275">is zero if no step is specified or the specified step is positive.</span></span>  
  * <span data-ttu-id="5e244-276">é o comprimento da matriz segmentada menos uma se a etapa especificada é negativa.</span><span class="sxs-lookup"><span data-stu-id="5e244-276">is the length of the sliced array minus one if the specified step is negative.</span></span>

* <span data-ttu-id="5e244-277">Se o valor *final* do intervalo for omitido, o valor final inferido</span><span class="sxs-lookup"><span data-stu-id="5e244-277">If the range *end* value is omitted, then the inferred end value</span></span>
  * <span data-ttu-id="5e244-278">é o comprimento da matriz segmentada menos uma se nenhuma etapa for especificada ou a etapa especificada for positiva.</span><span class="sxs-lookup"><span data-stu-id="5e244-278">is the length of the sliced array minus one if no step is specified or the specified step is positive.</span></span>
  * <span data-ttu-id="5e244-279">será zero se a etapa especificada for negativa.</span><span class="sxs-lookup"><span data-stu-id="5e244-279">is zero if the specified step is negative.</span></span>

<span data-ttu-id="5e244-280">Alguns exemplos são:</span><span class="sxs-lookup"><span data-stu-id="5e244-280">Some examples are:</span></span>

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

### <a name="copy-and-update-expressions"></a><span data-ttu-id="5e244-281">Expressões Copy-and-Update</span><span class="sxs-lookup"><span data-stu-id="5e244-281">Copy-and-Update Expressions</span></span>

<span data-ttu-id="5e244-282">Como todos os Q# tipos são tipos de valor (com o qubits que assume uma função especial), formalmente uma "cópia" é criada quando um valor é associado a um símbolo ou quando um símbolo é reassociado.</span><span class="sxs-lookup"><span data-stu-id="5e244-282">Since all Q# types are value types (with the qubits taking a somewhat special role), formally a "copy" is created when a value is bound to a symbol or when a symbol is rebound.</span></span> <span data-ttu-id="5e244-283">Isso significa que o comportamento do Q# é o mesmo que se uma cópia fosse criada usando um operador de atribuição.</span><span class="sxs-lookup"><span data-stu-id="5e244-283">That is to say, the behavior of Q# is the same as if a copy were created using an assignment operator.</span></span> 

<span data-ttu-id="5e244-284">É claro que, na prática, apenas as partes relevantes são recriadas conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="5e244-284">Of course, in practice, only the relevant pieces are recreated as needed.</span></span> <span data-ttu-id="5e244-285">Isso afeta a maneira como você copia matrizes porque não é possível atualizar itens de matriz.</span><span class="sxs-lookup"><span data-stu-id="5e244-285">This affects how you copy arrays because it is not possible to update array items.</span></span> <span data-ttu-id="5e244-286">Para modificar uma matriz existente, é necessário aproveitar um mecanismo de *copiar e atualizar* .</span><span class="sxs-lookup"><span data-stu-id="5e244-286">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="5e244-287">Você pode criar uma nova matriz de uma matriz existente por meio de expressões de *copiar e atualizar* , que usam os `w/` operadores `<-` e.</span><span class="sxs-lookup"><span data-stu-id="5e244-287">You can create a new array from an existing array via *copy-and-update* expressions, which use the operators `w/` and `<-`.</span></span>
<span data-ttu-id="5e244-288">Uma expressão de copiar e atualizar é uma expressão do formulário `expression1 w/ expression2 <- expression3` , em que</span><span class="sxs-lookup"><span data-stu-id="5e244-288">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where</span></span>

* <span data-ttu-id="5e244-289">`expression1` deve ser tipo `T[]` para algum tipo `T` .</span><span class="sxs-lookup"><span data-stu-id="5e244-289">`expression1` must be type `T[]` for some type `T`.</span></span>
* <span data-ttu-id="5e244-290">`expression2` define quais índices na matriz especificados em `expression1` para modificar.</span><span class="sxs-lookup"><span data-stu-id="5e244-290">`expression2` defines which indices in the array specified in `expression1` to modify.</span></span> <span data-ttu-id="5e244-291">`expression2` deve ser tipo `Int` ou tipo `Range` .</span><span class="sxs-lookup"><span data-stu-id="5e244-291">`expression2` must be either type `Int` or type `Range`.</span></span>
* <span data-ttu-id="5e244-292">`expression3` são os valores usados para atualizar elementos no `expression1` , com base nos índices especificados em `expression2` .</span><span class="sxs-lookup"><span data-stu-id="5e244-292">`expression3` is the value(s) used to update elements in `expression1`, based on the indices specified in `expression2`.</span></span> <span data-ttu-id="5e244-293">Se `expression2` for Type `Int` , `expression3` deverá ser Type `T` .</span><span class="sxs-lookup"><span data-stu-id="5e244-293">If `expression2` is type `Int`, `expression3` must be type `T`.</span></span> <span data-ttu-id="5e244-294">Se `expression2` for Type `Range` , `expression3` deverá ser Type `T[]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-294">If `expression2` is type `Range`, `expression3` must be type `T[]`.</span></span>

<span data-ttu-id="5e244-295">Por exemplo, a expressão Copy-and-update `arr w/ idx <- value` constrói uma nova matriz com todos os elementos definidos para os elementos correspondentes no `arr` , exceto para o elemento especificado por `idx` , que é definido como o (s) valor (es) em `value` .</span><span class="sxs-lookup"><span data-stu-id="5e244-295">For example, the copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding elements in `arr`, except for the element(s) specified by `idx`, which is set to the value(s) in `value`.</span></span> 

<span data-ttu-id="5e244-296">Fornecido `arr` contém a matriz `[0,1,2,3]` , então</span><span class="sxs-lookup"><span data-stu-id="5e244-296">Given `arr` contains the array `[0,1,2,3]`, then</span></span> 

- <span data-ttu-id="5e244-297">`arr w/ 0 <- 10` é a matriz `[10,1,2,3]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-297">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="5e244-298">`arr w/ 2 <- 10` é a matriz `[0,1,10,3]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-298">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="5e244-299">`arr w/ 0..2..3 <- [10,12]` é a matriz `[10,1,12,3]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-299">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="5e244-300">Copiar e atualizar expressões para itens nomeados</span><span class="sxs-lookup"><span data-stu-id="5e244-300">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="5e244-301">Existem expressões semelhantes para itens nomeados em tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5e244-301">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="5e244-302">Por exemplo, considere o tipo</span><span class="sxs-lookup"><span data-stu-id="5e244-302">For example, consider the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="5e244-303">Se `c` contiver o valor do tipo `Complex(1., -1.)` , `c w/ Re <- 0.` será uma expressão do tipo `Complex` que é avaliada como `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="5e244-303">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="5e244-304">Matrizes denteadas</span><span class="sxs-lookup"><span data-stu-id="5e244-304">Jagged Arrays</span></span>

<span data-ttu-id="5e244-305">Uma matriz denteada, às vezes chamada de "matriz de matrizes", é uma matriz cujos elementos são matrizes.</span><span class="sxs-lookup"><span data-stu-id="5e244-305">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="5e244-306">Os elementos de uma matriz denteada podem ser de tamanhos diferentes.</span><span class="sxs-lookup"><span data-stu-id="5e244-306">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="5e244-307">O exemplo a seguir mostra como declarar e inicializar uma matriz denteada que representa uma tabela de multiplicação.</span><span class="sxs-lookup"><span data-stu-id="5e244-307">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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

### <a name="arrays-of-callables"></a><span data-ttu-id="5e244-308">Matrizes de callablefiles</span><span class="sxs-lookup"><span data-stu-id="5e244-308">Arrays of callables</span></span> 

<span data-ttu-id="5e244-309">Você também pode criar uma matriz de chamadores.</span><span class="sxs-lookup"><span data-stu-id="5e244-309">You can also create an array of callables.</span></span>

* <span data-ttu-id="5e244-310">Se o tipo de elemento comum for uma operação ou tipo de função, todos os elementos deverão ter os mesmos tipos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="5e244-310">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
* <span data-ttu-id="5e244-311">O tipo de elemento da matriz dá suporte a qualquer [transmissão functors](xref:microsoft.quantum.guide.operationsfunctions) que tenha suporte de todos os elementos.</span><span class="sxs-lookup"><span data-stu-id="5e244-311">The element type of the array supports any [functors](xref:microsoft.quantum.guide.operationsfunctions) that are supported by all of the elements.</span></span>
<span data-ttu-id="5e244-312">Por exemplo, If `Op1` , `Op2` e `Op3` All são `Qubit[] => Unit` operações, mas `Op1` dá suporte a, dá suporte a `Adjoint` `Op2` `Controlled` e `Op3` dá suporte a ambos:</span><span class="sxs-lookup"><span data-stu-id="5e244-312">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit` operations, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>
  * <span data-ttu-id="5e244-313">`[Op1, Op2]` é uma matriz de `(Qubit[] => Unit)` operações.</span><span class="sxs-lookup"><span data-stu-id="5e244-313">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
  * <span data-ttu-id="5e244-314">`[Op1, Op3]` é uma matriz de `(Qubit[] => Unit is Adj)` operações.</span><span class="sxs-lookup"><span data-stu-id="5e244-314">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
  * <span data-ttu-id="5e244-315">`[Op2, Op3]` é uma matriz de `(Qubit[] => Unit is Ctl)` operações.</span><span class="sxs-lookup"><span data-stu-id="5e244-315">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="5e244-316">No entanto, enquanto as operações `(Qubit[] => Unit is Adj)` e  `(Qubit[] => Unit is Ctl)` têm o tipo base comum de `(Qubit[] => Unit)` , as *matrizes* dessas operações não compartilham um tipo base comum.</span><span class="sxs-lookup"><span data-stu-id="5e244-316">However, while the operations `(Qubit[] => Unit is Adj)` and  `(Qubit[] => Unit is Ctl)` have the common base type of `(Qubit[] => Unit)`, *arrays* of these operations do not share a common base type.</span></span>

<span data-ttu-id="5e244-317">Por exemplo, `[[Op1], [Op2]]` no momento, o geraria um erro porque ele tenta criar uma matriz dos dois tipos de matriz incompatíveis `(Qubit[] => Unit is Adj)[]` e `(Qubit[] => Unit is Ctl)[]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-317">For example, `[[Op1], [Op2]]` would currently raise an error because it attempts to create an array of the two incompatible array types `(Qubit[] => Unit is Adj)[]` and `(Qubit[] => Unit is Ctl)[]`.</span></span>

<span data-ttu-id="5e244-318">Para obter mais informações sobre o callables, consulte [expressões chamáveis](#callable-expressions) nesta página ou [operações e Q# funções no ](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="5e244-318">For more information on callables, see [Callable expressions](#callable-expressions)  on this page or [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="5e244-319">Expressões condicionais</span><span class="sxs-lookup"><span data-stu-id="5e244-319">Conditional Expressions</span></span>

<span data-ttu-id="5e244-320">Dadas duas expressões do mesmo tipo e uma expressão booleana, formate uma expressão condicional usando o ponto de interrogação, `?` e a barra vertical `|` .</span><span class="sxs-lookup"><span data-stu-id="5e244-320">Given two expressions of the same type and a Boolean expression, form a conditional expression using the question mark, `?`, and the vertical bar `|`.</span></span> <span data-ttu-id="5e244-321">Dado `a==b ? c | d` , o valor da expressão condicional é `c` se `a==b` for true e `d` se for false.</span><span class="sxs-lookup"><span data-stu-id="5e244-321">Given `a==b ? c | d`, the value of the conditional expression is `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="5e244-322">Expressões condicionais com callablefiles</span><span class="sxs-lookup"><span data-stu-id="5e244-322">Conditional expressions with callables</span></span>

<span data-ttu-id="5e244-323">Expressões condicionais podem ser avaliadas como operações que têm as mesmas entradas e saídas, mas dão suporte a diferentes transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="5e244-323">Conditional expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span> <span data-ttu-id="5e244-324">Nesse caso, o tipo da expressão condicional é uma operação com entradas e saídas que dão suporte a qualquer transmissão functors com suporte em ambas as expressões.</span><span class="sxs-lookup"><span data-stu-id="5e244-324">In this case, the type of the conditional expression is an operation with inputs and outputs that support any functors supported by both expressions.</span></span>
<span data-ttu-id="5e244-325">Por exemplo, se `Op1` , `Op2` , e `Op3` todos forem `Qubit[]=>Unit` , mas o oferecer suporte a, o oferece suporte a `Op1` `Adjoint` `Op2` `Controlled` , e `Op3` dá suporte a ambos:</span><span class="sxs-lookup"><span data-stu-id="5e244-325">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="5e244-326">`flag ? Op1 | Op2` é uma `(Qubit[] => Unit)` operação.</span><span class="sxs-lookup"><span data-stu-id="5e244-326">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="5e244-327">`flag ? Op1 | Op3` é uma `(Qubit[] => Unit is Adj)` operação.</span><span class="sxs-lookup"><span data-stu-id="5e244-327">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="5e244-328">`flag ? Op2 | Op3` é uma `(Qubit[] => Unit is Ctl)` operação.</span><span class="sxs-lookup"><span data-stu-id="5e244-328">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="5e244-329">Se qualquer uma das duas expressões de resultado possíveis incluir uma função ou uma chamada de operação, essa chamada só ocorrerá se o resultado for aquele que é o valor da chamada.</span><span class="sxs-lookup"><span data-stu-id="5e244-329">If either of the two possible result expressions include a function or operation call, that call only takes place if that result is the one that is the value of the call.</span></span> <span data-ttu-id="5e244-330">Por exemplo, no caso `a==b ? C(qs) | D(qs)` , se `a==b` for true, a `C` operação será invocada e, se for false, somente a `D` operação será invocada.</span><span class="sxs-lookup"><span data-stu-id="5e244-330">For example, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true, then the `C` operation is invoked, and if it is false then only the `D` operation is invoked.</span></span> <span data-ttu-id="5e244-331">Essa abordagem é semelhante ao *curto circuito* em outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="5e244-331">This approach is similar to *short-circuiting* in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="5e244-332">Expressões que podem ser chamadas</span><span class="sxs-lookup"><span data-stu-id="5e244-332">Callable Expressions</span></span>

<span data-ttu-id="5e244-333">Um literal que pôde ser chamado é o nome de uma operação ou função definida no escopo de compilação.</span><span class="sxs-lookup"><span data-stu-id="5e244-333">A callable literal is the name of an operation or function defined in the compilation scope.</span></span> <span data-ttu-id="5e244-334">Por exemplo, `X` é um literal de operação que se refere à operação de biblioteca padrão `X` e `Message` é um literal de função que se refere à função de biblioteca padrão `Message` .</span><span class="sxs-lookup"><span data-stu-id="5e244-334">For example, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="5e244-335">Se uma operação oferecer suporte a `Adjoint` functor, `Adjoint op` será uma expressão de operação.</span><span class="sxs-lookup"><span data-stu-id="5e244-335">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="5e244-336">Da mesma forma, se a operação oferecer suporte a `Controlled` functor, `Controlled op` será uma expressão de operação.</span><span class="sxs-lookup"><span data-stu-id="5e244-336">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="5e244-337">Para obter mais informações sobre os tipos dessas expressões, consulte [chamando especializações de operação](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span><span class="sxs-lookup"><span data-stu-id="5e244-337">For more information about the types of these expressions, see [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="5e244-338">Transmissão functors ( `Adjoint` e `Controlled` ) associam-se mais de todos os outros operadores, exceto para o operador de desencapsulamento `!` e a indexação de matriz com `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="5e244-338">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[ ]`.</span></span>
<span data-ttu-id="5e244-339">Portanto, as seguintes são todas válidas, supondo que as operações suportam o transmissão functors usado:</span><span class="sxs-lookup"><span data-stu-id="5e244-339">Thus, the following are all valid, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="5e244-340">Expressões callable parametrizadas de tipo</span><span class="sxs-lookup"><span data-stu-id="5e244-340">Type-parameterized callable expressions</span></span>

<span data-ttu-id="5e244-341">Você pode usar um literal chamável como um valor, por exemplo, para atribuí-lo a uma variável ou passá-lo para outro callable.</span><span class="sxs-lookup"><span data-stu-id="5e244-341">You can use a callable literal as a value, for example, to assign it to a variable or pass it to another callable.</span></span> <span data-ttu-id="5e244-342">Nesse caso, se o callable tiver [parâmetros de tipo](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), você deverá fornecer os parâmetros como parte do valor que pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="5e244-342">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), you must provide the parameters as part of the callable value.</span></span>

<span data-ttu-id="5e244-343">Um valor callable não pode ter nenhum parâmetro de tipo não especificado.</span><span class="sxs-lookup"><span data-stu-id="5e244-343">A callable value cannot have any unspecified type parameters.</span></span> <span data-ttu-id="5e244-344">Por exemplo, se `Fun` for uma função com a assinatura `'T1->Unit` :</span><span class="sxs-lookup"><span data-stu-id="5e244-344">For example, if `Fun` is a function with the signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomeOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="5e244-345">Expressões de invocação que podem ser chamadas</span><span class="sxs-lookup"><span data-stu-id="5e244-345">Callable Invocation Expressions</span></span>

<span data-ttu-id="5e244-346">Dada uma expressão resgatável (operação ou função) e uma expressão de tupla do tipo de entrada da assinatura do callable, você pode formar uma *expressão de invocação* acrescentando a expressão de tupla à expressão que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5e244-346">Given a callable expression (operation or function) and a tuple expression of the input type of the callable's signature, you can form an *invocation expression* by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="5e244-347">O tipo da expressão de invocação é o tipo de saída da assinatura do callable.</span><span class="sxs-lookup"><span data-stu-id="5e244-347">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="5e244-348">Por exemplo, se `Op` for uma operação com a assinatura `((Int, Qubit) => Double)` , `Op(3, qubit1)` será uma expressão do tipo `Double` .</span><span class="sxs-lookup"><span data-stu-id="5e244-348">For example, if `Op` is an operation with the signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="5e244-349">Da mesma forma, se `Sin` for uma função com a assinatura `(Double -> Double)` , `Sin(0.1)` será uma expressão do tipo `Double` .</span><span class="sxs-lookup"><span data-stu-id="5e244-349">Similarly, if `Sin` is a function with the signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="5e244-350">Por fim, se `Builder` for uma função com a assinatura `(Int -> (Int -> Int))` , `Builder(3)` será uma função de `Int` para `Int` .</span><span class="sxs-lookup"><span data-stu-id="5e244-350">Finally, if `Builder` is a function with the signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from `Int` to `Int`.</span></span>

<span data-ttu-id="5e244-351">Invocar o resultado de uma expressão com valor callable requer um par extra de parênteses em volta da expressão callable.</span><span class="sxs-lookup"><span data-stu-id="5e244-351">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="5e244-352">Portanto, para invocar o resultado da chamada `Builder` do parágrafo anterior, a sintaxe correta é:</span><span class="sxs-lookup"><span data-stu-id="5e244-352">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="5e244-353">Ao invocar um callable [-parametrizado de tipo](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) , você pode especificar os parâmetros de tipo reais dentro de colchetes angulares `< >` após a expressão que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5e244-353">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, you can specify the actual type parameters within angle brackets `< >` after the callable expression.</span></span>
<span data-ttu-id="5e244-354">Normalmente, essa ação é desnecessária, pois o Q# compilador infere os tipos reais.</span><span class="sxs-lookup"><span data-stu-id="5e244-354">This action is usually unnecessary as the Q# compiler infers the actual types.</span></span>
<span data-ttu-id="5e244-355">No entanto, ele *será* necessário para o [aplicativo parcial](xref:microsoft.quantum.guide.operationsfunctions#partial-application) se um argumento de tipo parametrizado for deixado não especificado.</span><span class="sxs-lookup"><span data-stu-id="5e244-355">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="5e244-356">Ele também é útil ao passar operações com suporte diferente para o functor para um callable.</span><span class="sxs-lookup"><span data-stu-id="5e244-356">It is also useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="5e244-357">Por exemplo, se `Func` tem assinatura e tem assinatura e `('T1, 'T2, 'T1) -> 'T2` `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` tem assinatura `(Qubit[] => Unit)` , para invocar `Func` com `Op1` como o primeiro argumento, `Op2` como o segundo, e `Op3` como o terceiro:</span><span class="sxs-lookup"><span data-stu-id="5e244-357">For example, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="5e244-358">A especificação de tipo é necessária porque `Op3` e `Op1` tem tipos diferentes, portanto, o compilador tratará isso como ambíguo sem a especificação.</span><span class="sxs-lookup"><span data-stu-id="5e244-358">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="5e244-359">Precedência de operador</span><span class="sxs-lookup"><span data-stu-id="5e244-359">Operator Precedence</span></span>

* <span data-ttu-id="5e244-360">Todos os operadores binários são associativos à direita, exceto para `^` .</span><span class="sxs-lookup"><span data-stu-id="5e244-360">All binary operators are right-associative, except for `^`.</span></span>

* <span data-ttu-id="5e244-361">Colchetes, `[ ]` , para a divisão e a indexação de matriz, associe antes de qualquer operador.</span><span class="sxs-lookup"><span data-stu-id="5e244-361">Brackets, `[ ]`, for array slicing and indexing, bind before any operator.</span></span>

* <span data-ttu-id="5e244-362">A transmissão functors `Adjoint` e a `Controlled` Associação após a indexação da matriz, mas antes de todos os outros operadores.</span><span class="sxs-lookup"><span data-stu-id="5e244-362">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

* <span data-ttu-id="5e244-363">Parênteses para operação e invocação de função também são associados antes de qualquer operador, mas após a indexação de matriz e transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="5e244-363">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="5e244-364">Q# operadores em ordem de precedência, do mais alto ao mais baixo:</span><span class="sxs-lookup"><span data-stu-id="5e244-364">Q# operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="5e244-365">Operador</span><span class="sxs-lookup"><span data-stu-id="5e244-365">Operator</span></span> | <span data-ttu-id="5e244-366">Arity</span><span class="sxs-lookup"><span data-stu-id="5e244-366">Arity</span></span> | <span data-ttu-id="5e244-367">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e244-367">Description</span></span> | <span data-ttu-id="5e244-368">Tipos de operando</span><span class="sxs-lookup"><span data-stu-id="5e244-368">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="5e244-369">à direita `!`</span><span class="sxs-lookup"><span data-stu-id="5e244-369">trailing `!`</span></span> | <span data-ttu-id="5e244-370">Unário</span><span class="sxs-lookup"><span data-stu-id="5e244-370">Unary</span></span> | <span data-ttu-id="5e244-371">Desencapsular</span><span class="sxs-lookup"><span data-stu-id="5e244-371">Unwrap</span></span> | <span data-ttu-id="5e244-372">Qualquer tipo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5e244-372">Any user-defined type</span></span>
 <span data-ttu-id="5e244-373">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="5e244-373">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="5e244-374">Unário</span><span class="sxs-lookup"><span data-stu-id="5e244-374">Unary</span></span> | <span data-ttu-id="5e244-375">Numérico negativo, complemento de bit-nte, negação lógica</span><span class="sxs-lookup"><span data-stu-id="5e244-375">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="5e244-376">`Int`, `BigInt` ou `Double` para `-` , `Int` ou `BigInt` para `~~~` , `Bool` para `not`</span><span class="sxs-lookup"><span data-stu-id="5e244-376">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="5e244-377">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-377">Binary</span></span> | <span data-ttu-id="5e244-378">Potência de inteiro</span><span class="sxs-lookup"><span data-stu-id="5e244-378">Integer power</span></span> | <span data-ttu-id="5e244-379">`Int` ou `BigInt` para a base, `Int` para o expoente</span><span class="sxs-lookup"><span data-stu-id="5e244-379">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="5e244-380">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="5e244-380">`/`, `*`, `%`</span></span> | <span data-ttu-id="5e244-381">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-381">Binary</span></span> | <span data-ttu-id="5e244-382">Divisão, multiplicação, módulo de inteiro</span><span class="sxs-lookup"><span data-stu-id="5e244-382">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="5e244-383">`Int`, `BigInt` ou `Double` para `/` e `*` , `Int` ou `BigInt` para `%`</span><span class="sxs-lookup"><span data-stu-id="5e244-383">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="5e244-384">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="5e244-384">`+`, `-`</span></span> | <span data-ttu-id="5e244-385">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-385">Binary</span></span> | <span data-ttu-id="5e244-386">Adição ou concatenação de cadeia de caracteres e matriz, subtração</span><span class="sxs-lookup"><span data-stu-id="5e244-386">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="5e244-387">`Int`, `BigInt` ou `Double` , além disso, `String` ou qualquer tipo de matriz para `+`</span><span class="sxs-lookup"><span data-stu-id="5e244-387">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="5e244-388">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="5e244-388">`<<<`, `>>>`</span></span> | <span data-ttu-id="5e244-389">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-389">Binary</span></span> | <span data-ttu-id="5e244-390">Deslocamento à esquerda, deslocamento à direita</span><span class="sxs-lookup"><span data-stu-id="5e244-390">Left shift, right shift</span></span> | <span data-ttu-id="5e244-391">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5e244-391">`Int` or `BigInt`</span></span>
 <span data-ttu-id="5e244-392">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="5e244-392">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="5e244-393">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-393">Binary</span></span> | <span data-ttu-id="5e244-394">Comparações de menor que, menor que ou igual a, maior que, maior que ou igual a</span><span class="sxs-lookup"><span data-stu-id="5e244-394">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="5e244-395">`Int`, `BigInt` ou `Double`</span><span class="sxs-lookup"><span data-stu-id="5e244-395">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="5e244-396">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="5e244-396">`==`, `!=`</span></span> | <span data-ttu-id="5e244-397">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-397">Binary</span></span> | <span data-ttu-id="5e244-398">comparações iguais, não iguais</span><span class="sxs-lookup"><span data-stu-id="5e244-398">equal, not-equal comparisons</span></span> | <span data-ttu-id="5e244-399">qualquer tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="5e244-399">any primitive type</span></span>
 `&&&` | <span data-ttu-id="5e244-400">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-400">Binary</span></span> | <span data-ttu-id="5e244-401">AND bit a bit</span><span class="sxs-lookup"><span data-stu-id="5e244-401">Bitwise AND</span></span> | <span data-ttu-id="5e244-402">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5e244-402">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="5e244-403">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-403">Binary</span></span> | <span data-ttu-id="5e244-404">XOR bit a bit</span><span class="sxs-lookup"><span data-stu-id="5e244-404">Bitwise XOR</span></span> | <span data-ttu-id="5e244-405">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5e244-405">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="5e244-406">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-406">Binary</span></span> | <span data-ttu-id="5e244-407">OR bit a bit</span><span class="sxs-lookup"><span data-stu-id="5e244-407">Bitwise OR</span></span> | <span data-ttu-id="5e244-408">`Int` ou `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5e244-408">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="5e244-409">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-409">Binary</span></span> | <span data-ttu-id="5e244-410">AND lógico</span><span class="sxs-lookup"><span data-stu-id="5e244-410">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="5e244-411">Binário</span><span class="sxs-lookup"><span data-stu-id="5e244-411">Binary</span></span> | <span data-ttu-id="5e244-412">OR lógico</span><span class="sxs-lookup"><span data-stu-id="5e244-412">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="5e244-413">Binary/ternário</span><span class="sxs-lookup"><span data-stu-id="5e244-413">Binary/Ternary</span></span> | <span data-ttu-id="5e244-414">Operador de intervalo</span><span class="sxs-lookup"><span data-stu-id="5e244-414">Range operator</span></span> | `Int`
 <span data-ttu-id="5e244-415">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="5e244-415">`?` `|`</span></span> | <span data-ttu-id="5e244-416">Ternário</span><span class="sxs-lookup"><span data-stu-id="5e244-416">Ternary</span></span> | <span data-ttu-id="5e244-417">Condicional</span><span class="sxs-lookup"><span data-stu-id="5e244-417">Conditional</span></span> | <span data-ttu-id="5e244-418">`Bool` para o lado esquerdo</span><span class="sxs-lookup"><span data-stu-id="5e244-418">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="5e244-419">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="5e244-419">`w/` `<-`</span></span> | <span data-ttu-id="5e244-420">Ternário</span><span class="sxs-lookup"><span data-stu-id="5e244-420">Ternary</span></span> | <span data-ttu-id="5e244-421">Copiar e atualizar</span><span class="sxs-lookup"><span data-stu-id="5e244-421">Copy-and-update</span></span> | <span data-ttu-id="5e244-422">Consulte [expressões de copiar e atualizar](#copy-and-update-expressions)</span><span class="sxs-lookup"><span data-stu-id="5e244-422">See [Copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="next-steps"></a><span data-ttu-id="5e244-423">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="5e244-423">Next steps</span></span>

<span data-ttu-id="5e244-424">Agora que você pode trabalhar com expressões no Q# , vá para [operações e funções Q# no](xref:microsoft.quantum.guide.operationsfunctions) para saber como definir e chamar operações e funções.</span><span class="sxs-lookup"><span data-stu-id="5e244-424">Now that you can work with expressions in Q#, move on to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
