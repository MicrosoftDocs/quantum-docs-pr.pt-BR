---
title: Fluxo de controle emQ#
description: Loops, condicionais, etc.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
no-loc:
- Q#
- $$v
ms.openlocfilehash: fc619d64bfebfc27d7feac6dafb2dd4cf22825d6
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867940"
---
# <a name="control-flow-in-no-locq"></a><span data-ttu-id="ebe98-103">Fluxo de controle emQ#</span><span class="sxs-lookup"><span data-stu-id="ebe98-103">Control flow in Q#</span></span>

<span data-ttu-id="ebe98-104">Em uma operação ou função, cada instrução é executada em ordem, semelhante a outros idiomas clássicos imperativos comuns.</span><span class="sxs-lookup"><span data-stu-id="ebe98-104">Within an operation or function, each statement runs in order, similar to other common imperative classical languages.</span></span>
<span data-ttu-id="ebe98-105">No entanto, você pode modificar o fluxo de controle de três maneiras distintas:</span><span class="sxs-lookup"><span data-stu-id="ebe98-105">However, you can modify the flow of control in three distinct ways:</span></span>

* <span data-ttu-id="ebe98-106">`if`instruções</span><span class="sxs-lookup"><span data-stu-id="ebe98-106">`if` statements</span></span>
* <span data-ttu-id="ebe98-107">`for`loops</span><span class="sxs-lookup"><span data-stu-id="ebe98-107">`for` loops</span></span>
* <span data-ttu-id="ebe98-108">`repeat-until-success`loops</span><span class="sxs-lookup"><span data-stu-id="ebe98-108">`repeat-until-success` loops</span></span>

<span data-ttu-id="ebe98-109">As `if` `for` construções de fluxo de controle e passam em um sentido familiar para a maioria das linguagens de programação clássicas.</span><span class="sxs-lookup"><span data-stu-id="ebe98-109">The `if` and `for` control flow constructs proceed in a familiar sense to most classical programming languages.</span></span> <span data-ttu-id="ebe98-110">[`Repeat-until-success`](#repeat-until-success-loop)os loops são discutidos posteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="ebe98-110">[`Repeat-until-success`](#repeat-until-success-loop) loops are discussed later in this article.</span></span>

<span data-ttu-id="ebe98-111">Importante, `for` loops e `if` instruções podem ser usados em operações para as quais as [especializações](xref:microsoft.quantum.guide.operationsfunctions) são geradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ebe98-111">Importantly, `for` loops and `if` statements can be used in operations for which [specializations](xref:microsoft.quantum.guide.operationsfunctions) are auto-generated.</span></span> <span data-ttu-id="ebe98-112">Nesse cenário, o adjoin de um `for` loop inverte a direção e usa o adjacente de cada iteração.</span><span class="sxs-lookup"><span data-stu-id="ebe98-112">In that scenario, the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="ebe98-113">Esta ação segue o princípio de "calçados e-Socks": se você deseja desfazer a colocação em SOCKS e, em seguida, os sapatos, você deve desfazer a colocação de sapatos e, em seguida, desfazer a colocação em Socks.</span><span class="sxs-lookup"><span data-stu-id="ebe98-113">This action follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span> 

## <a name="if-else-if-else"></a><span data-ttu-id="ebe98-114">If, else-if, Else</span><span class="sxs-lookup"><span data-stu-id="ebe98-114">If, Else-if, Else</span></span>

<span data-ttu-id="ebe98-115">A `if` instrução dá suporte à execução condicional.</span><span class="sxs-lookup"><span data-stu-id="ebe98-115">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="ebe98-116">Ele consiste na palavra-chave `if` , uma expressão booliana entre parênteses e um bloco de instrução (o bloco _then_ ).</span><span class="sxs-lookup"><span data-stu-id="ebe98-116">It consists of the keyword `if`, a Boolean expression in parentheses, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="ebe98-117">Opcionalmente, qualquer número de cláusulas else-if pode seguir, cada uma delas consiste na palavra-chave `elif` , uma expressão booliana entre parênteses e um bloco de instrução (o bloco _else-if_ ).</span><span class="sxs-lookup"><span data-stu-id="ebe98-117">Optionally, any number of else-if clauses can follow, each of which consists of the keyword `elif`, a Boolean expression in parentheses, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="ebe98-118">Por fim, a instrução pode, opcionalmente, ser concluída com uma cláusula else, que consiste na palavra-chave `else` seguida por outro bloco de instrução (o bloco _else_ ).</span><span class="sxs-lookup"><span data-stu-id="ebe98-118">Finally, the statement can optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="ebe98-119">A `if` condição é avaliada e, se for *verdadeira*, o bloco *then* será executado.</span><span class="sxs-lookup"><span data-stu-id="ebe98-119">The `if` condition is evaluated, and if it is *true*, the *then* block is run.</span></span>
<span data-ttu-id="ebe98-120">Se a condição for *falsa*, a primeira condição IF-IF será avaliada; Se isso for verdadeiro, o bloco *else-if* será executado.</span><span class="sxs-lookup"><span data-stu-id="ebe98-120">If the condition is *false*, then the first else-if condition is evaluated; if that is true, then the *else-if* block is run.</span></span>
<span data-ttu-id="ebe98-121">Caso contrário, o segundo bloco else é avaliado e, em seguida, o terceiro, e assim por diante, até que seja encontrada uma cláusula com uma condição true ou que não haja mais cláusulas If-If.</span><span class="sxs-lookup"><span data-stu-id="ebe98-121">Otherwise, the second else-if block evaluates, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="ebe98-122">Se a condição *If* original e todas as cláusulas else-if forem avaliadas como *false*, o bloco *else* será executado, se fornecido.</span><span class="sxs-lookup"><span data-stu-id="ebe98-122">If the original *if* condition and all the else-if clauses evaluate to *false*, the *else* block is run, if provided.</span></span>

<span data-ttu-id="ebe98-123">Observe que qualquer bloco é executado, ele é executado dentro de seu próprio escopo.</span><span class="sxs-lookup"><span data-stu-id="ebe98-123">Note that whichever block runs, it runs within its own scope.</span></span>
<span data-ttu-id="ebe98-124">Associações feitas dentro de um `if` bloco, `elif` ou `else` não são visíveis depois que o bloco termina.</span><span class="sxs-lookup"><span data-stu-id="ebe98-124">Bindings made inside of an `if`, `elif`, or `else` block are not visible after the block ends.</span></span>

<span data-ttu-id="ebe98-125">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ebe98-125">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="ebe98-126">ou o</span><span class="sxs-lookup"><span data-stu-id="ebe98-126">or</span></span>
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a><span data-ttu-id="ebe98-127">Loop for</span><span class="sxs-lookup"><span data-stu-id="ebe98-127">For loop</span></span>

<span data-ttu-id="ebe98-128">A `for` instrução dá suporte à iteração em um intervalo de inteiros ou em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="ebe98-128">The `for` statement supports iteration over an integer range or an array.</span></span>
<span data-ttu-id="ebe98-129">A instrução consiste na palavra-chave `for` , seguida por uma tupla de símbolo ou símbolo, a palavra-chave `in` e uma expressão de tipo `Range` ou matriz, todas entre parênteses e um bloco de instruções.</span><span class="sxs-lookup"><span data-stu-id="ebe98-129">The statement consists of the keyword `for`, followed by a symbol or symbol tuple, the keyword `in`, and an expression of type `Range` or array, all in parentheses, and a statement block.</span></span>

<span data-ttu-id="ebe98-130">O bloco de instrução (o corpo do loop) é executado repetidamente, com o símbolo definido (a variável de loop) associado a cada valor no intervalo ou na matriz.</span><span class="sxs-lookup"><span data-stu-id="ebe98-130">The statement block (the body of the loop) runs repeatedly, with the defined symbol (the loop variable) bound to each value in the range or array.</span></span>
<span data-ttu-id="ebe98-131">Observe que, se a expressão de intervalo for avaliada como um intervalo ou uma matriz vazia, o corpo não será executado.</span><span class="sxs-lookup"><span data-stu-id="ebe98-131">Note that if the range expression evaluates to an empty range or array, the body does not run at all.</span></span>
<span data-ttu-id="ebe98-132">A expressão é totalmente avaliada antes de entrar no loop e não é alterada enquanto o loop está em execução.</span><span class="sxs-lookup"><span data-stu-id="ebe98-132">The expression is fully evaluated before entering the loop, and does not change while the loop is executing.</span></span>

<span data-ttu-id="ebe98-133">A variável de loop é associada a cada entrada no corpo do loop e é desassociada no final do corpo.</span><span class="sxs-lookup"><span data-stu-id="ebe98-133">The loop variable is bound at each entrance to the loop body, and is unbound at the end of the body.</span></span>
<span data-ttu-id="ebe98-134">A variável de loop não está associada após a conclusão do loop for.</span><span class="sxs-lookup"><span data-stu-id="ebe98-134">The loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="ebe98-135">A associação da variável de loop é imutável e segue as mesmas regras que outras associações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="ebe98-135">The binding of the loop variable is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="ebe98-136">Nestes exemplos, `qubits` é um registro de qubits (ou seja, do tipo `Qubit[]` ),</span><span class="sxs-lookup"><span data-stu-id="ebe98-136">In these examples, `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

<span data-ttu-id="ebe98-137">Observe que, no final, utilizamos o operador binário aritmético-Shift-Left, `<<<` .</span><span class="sxs-lookup"><span data-stu-id="ebe98-137">Note that at the end, we utilized the arithmetic-shift-left binary operator, `<<<`.</span></span> <span data-ttu-id="ebe98-138">Para obter mais informações, consulte [expressões numéricas](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span><span class="sxs-lookup"><span data-stu-id="ebe98-138">For more information, see [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span></span>

## <a name="repeat-until-success-loop"></a><span data-ttu-id="ebe98-139">Repetir-loop Until-êxito</span><span class="sxs-lookup"><span data-stu-id="ebe98-139">Repeat-until-success loop</span></span>

<span data-ttu-id="ebe98-140">A Q# linguagem permite que o fluxo de controle clássico dependa dos resultados da medição de qubits.</span><span class="sxs-lookup"><span data-stu-id="ebe98-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="ebe98-141">Essa funcionalidade, por sua vez, permite a implementação de gadgets probabilística eficientes que podem reduzir o custo computacional para a implementação de unidades.</span><span class="sxs-lookup"><span data-stu-id="ebe98-141">This capability, in turn, enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="ebe98-142">Exemplos disso são os padrões de " *repetir-até-êxito* " (RUS) no Q# .</span><span class="sxs-lookup"><span data-stu-id="ebe98-142">Examples of this are the *repeat-until-success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="ebe98-143">Esses padrões de RUS são programas probabilística que têm um baixo custo *esperado* em termos de Gates elementares; o custo incorrido depende da execução real e da intercalação das várias ramificações possíveis.</span><span class="sxs-lookup"><span data-stu-id="ebe98-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates; the incurred cost depends on the actual run and the interleaving of the multiple possible branchings.</span></span>

<span data-ttu-id="ebe98-144">Para facilitar os padrões do RUS (repetição até o êxito), Q# o dá suporte às construções</span><span class="sxs-lookup"><span data-stu-id="ebe98-144">To facilitate repeat-until-success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="ebe98-145">em que `expression` é qualquer expressão válida que seja avaliada como um valor do tipo `Bool` .</span><span class="sxs-lookup"><span data-stu-id="ebe98-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="ebe98-146">O corpo do loop é executado e, em seguida, a condição é avaliada.</span><span class="sxs-lookup"><span data-stu-id="ebe98-146">The loop body runs, and then the condition is evaluated.</span></span>
<span data-ttu-id="ebe98-147">Se a condição for verdadeira, a instrução será concluída; caso contrário, a correção é executada e a instrução é executada novamente, começando com o corpo do loop.</span><span class="sxs-lookup"><span data-stu-id="ebe98-147">If the condition is true, then the statement is completed; otherwise, the fixup runs, and the statement runs again, starting with the loop body.</span></span>

<span data-ttu-id="ebe98-148">Todas as três partes de um loop RUS (o corpo, o teste e a correção) são tratadas como um único escopo *para cada repetição*, de modo que os símbolos associados ao corpo estejam disponíveis no teste e na correção.</span><span class="sxs-lookup"><span data-stu-id="ebe98-148">All three portions of an RUS loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in both the test and the fixup.</span></span>
<span data-ttu-id="ebe98-149">No entanto, concluir a execução da correção encerra o escopo da instrução, para que as associações de símbolo feitas durante o corpo ou correção não estejam disponíveis em repetições subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ebe98-149">However, completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="ebe98-150">Além disso, a `fixup` instrução geralmente é útil, mas nem sempre é necessária.</span><span class="sxs-lookup"><span data-stu-id="ebe98-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="ebe98-151">Em casos em que não é necessário, a construção</span><span class="sxs-lookup"><span data-stu-id="ebe98-151">In cases that it is not needed, the construct</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression);
```

<span data-ttu-id="ebe98-152">também é um padrão RUS válido.</span><span class="sxs-lookup"><span data-stu-id="ebe98-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="ebe98-153">Para obter mais exemplos e detalhes, consulte os [exemplos de repetir-até-êxito](#repeat-until-success-examples) neste artigo.</span><span class="sxs-lookup"><span data-stu-id="ebe98-153">For more examples and details, see [Repeat-until-success examples](#repeat-until-success-examples) in this article.</span></span>

> [!TIP]   
> <span data-ttu-id="ebe98-154">Evite usar loops repetir-até-sucesso dentro de funções.</span><span class="sxs-lookup"><span data-stu-id="ebe98-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="ebe98-155">Use loops *while* para fornecer a funcionalidade correspondente dentro das funções.</span><span class="sxs-lookup"><span data-stu-id="ebe98-155">Use *while* loops to provide the corresponding functionality inside functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="ebe98-156">Loop while</span><span class="sxs-lookup"><span data-stu-id="ebe98-156">While loop</span></span>

<span data-ttu-id="ebe98-157">Os padrões de repetição-até-sucesso têm uma connotação de muito Quantum específica.</span><span class="sxs-lookup"><span data-stu-id="ebe98-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="ebe98-158">Eles são amplamente usados em classes específicas de algoritmos Quantum, portanto, a construção de linguagem dedicada no Q# .</span><span class="sxs-lookup"><span data-stu-id="ebe98-158">They are widely used in particular classes of quantum algorithms - hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="ebe98-159">No entanto, os loops que quebram com base em uma condição e cujo comprimento de execução é, portanto, desconhecido em tempo de compilação, são tratados com cuidado específico em um tempo de execução do Quantum.</span><span class="sxs-lookup"><span data-stu-id="ebe98-159">However, loops that break based on a condition and whose execution length is thus unknown at compile-time, are handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="ebe98-160">No entanto, seu uso dentro de funções não é problemático, pois esses loops contêm apenas um código que é executado em hardware convencional (sem Quantum).</span><span class="sxs-lookup"><span data-stu-id="ebe98-160">However, their use within functions is unproblematic since these loops only contain code that runs on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="ebe98-161">Q#o, portanto, dá suporte ao uso de loops while apenas dentro de funções.</span><span class="sxs-lookup"><span data-stu-id="ebe98-161">Q#, therefore, supports to use of while loops within functions only.</span></span> <span data-ttu-id="ebe98-162">Uma `while` instrução consiste na palavra-chave `while` , uma expressão booliana entre parênteses e um bloco de instruções.</span><span class="sxs-lookup"><span data-stu-id="ebe98-162">A `while` statement consists of the keyword `while`, a Boolean expression in parentheses, and a statement block.</span></span>
<span data-ttu-id="ebe98-163">O bloco de instrução (o corpo do loop) é executado contanto que a condição seja avaliada como `true` .</span><span class="sxs-lookup"><span data-stu-id="ebe98-163">The statement block (the body of the loop) runs as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="return-statement"></a><span data-ttu-id="ebe98-164">Instrução Return</span><span class="sxs-lookup"><span data-stu-id="ebe98-164">Return Statement</span></span>

<span data-ttu-id="ebe98-165">A instrução return encerra a execução de uma operação ou função e retorna um valor para o chamador.</span><span class="sxs-lookup"><span data-stu-id="ebe98-165">The return statement ends the run of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="ebe98-166">Ele consiste na palavra-chave `return` , seguida por uma expressão do tipo apropriado e um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="ebe98-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="ebe98-167">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ebe98-167">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="ebe98-168">ou o</span><span class="sxs-lookup"><span data-stu-id="ebe98-168">or</span></span>
```qsharp
return (results, qubits);
```

* <span data-ttu-id="ebe98-169">Um callable que retorna uma tupla vazia, `()` , não requer uma instrução de retorno.</span><span class="sxs-lookup"><span data-stu-id="ebe98-169">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
* <span data-ttu-id="ebe98-170">Para especificar uma saída antecipada da operação ou da função, use `return ();` .</span><span class="sxs-lookup"><span data-stu-id="ebe98-170">To specify an early exit from the operation or function, use `return ();`.</span></span>
<span data-ttu-id="ebe98-171">Os chamadores que retornam qualquer outro tipo exigem uma instrução de retorno final.</span><span class="sxs-lookup"><span data-stu-id="ebe98-171">Callables that return any other type require a final return statement.</span></span>
* <span data-ttu-id="ebe98-172">Não há um número máximo de instruções de retorno em uma operação.</span><span class="sxs-lookup"><span data-stu-id="ebe98-172">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="ebe98-173">O compilador pode emitir um aviso se as instruções seguirem uma instrução return dentro de um bloco.</span><span class="sxs-lookup"><span data-stu-id="ebe98-173">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

   
## <a name="fail-statement"></a><span data-ttu-id="ebe98-174">Instrução Fail</span><span class="sxs-lookup"><span data-stu-id="ebe98-174">Fail statement</span></span>

<span data-ttu-id="ebe98-175">A instrução Fail encerra a execução de uma operação e retorna um valor de erro para o chamador.</span><span class="sxs-lookup"><span data-stu-id="ebe98-175">The fail statement ends the run of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="ebe98-176">Ele consiste na palavra-chave `fail` , seguida por uma cadeia de caracteres e um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="ebe98-176">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="ebe98-177">A instrução retorna a cadeia de caracteres para o driver clássico como a mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="ebe98-177">The statement returns the string to the classical driver as the error message.</span></span>

<span data-ttu-id="ebe98-178">Não há nenhuma restrição quanto ao número de instruções de falha em uma operação.</span><span class="sxs-lookup"><span data-stu-id="ebe98-178">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="ebe98-179">O compilador pode emitir um aviso se as instruções seguirem uma instrução Fail dentro de um bloco.</span><span class="sxs-lookup"><span data-stu-id="ebe98-179">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="ebe98-180">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ebe98-180">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="ebe98-181">ou, usando [cadeias de caracteres interpoladas](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span><span class="sxs-lookup"><span data-stu-id="ebe98-181">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="ebe98-182">Exemplos de repetição-até-êxito</span><span class="sxs-lookup"><span data-stu-id="ebe98-182">Repeat-until-success examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="ebe98-183">Padrão RUS para rotação de qubit único sobre um eixo irracional</span><span class="sxs-lookup"><span data-stu-id="ebe98-183">RUS pattern for single-qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="ebe98-184">Em um caso de uso típico, a Q# operação a seguir implementa uma rotação em um eixo irracional de $ (I + 2i Z)/\sqrt {5} $ na esfera de Bloch.</span><span class="sxs-lookup"><span data-stu-id="ebe98-184">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="ebe98-185">A implementação usa um padrão RUS conhecido:</span><span class="sxs-lookup"><span data-stu-id="ebe98-185">The implementation uses a known RUS pattern:</span></span>

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a><span data-ttu-id="ebe98-186">Loop RUS com uma variável mutável no escopo</span><span class="sxs-lookup"><span data-stu-id="ebe98-186">RUS loop with a mutable variable in scope</span></span>

<span data-ttu-id="ebe98-187">Este exemplo mostra o uso de uma variável mutável, `finished` , que está dentro do escopo de todo o loop Repeat-Until-recorretion e que é inicializado antes do loop e atualizado na etapa de correção.</span><span class="sxs-lookup"><span data-stu-id="ebe98-187">This example shows the use of a mutable variable, `finished`, which is within the scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a><span data-ttu-id="ebe98-188">RUS sem`fixup`</span><span class="sxs-lookup"><span data-stu-id="ebe98-188">RUS without `fixup`</span></span>

<span data-ttu-id="ebe98-189">Este exemplo mostra um loop RUS sem a etapa de correção.</span><span class="sxs-lookup"><span data-stu-id="ebe98-189">This example shows an RUS loop without the fixup step.</span></span> <span data-ttu-id="ebe98-190">O código é um circuito probabilística que implementa um portão de rotação importante $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ usando `H` as `T` Gates e.</span><span class="sxs-lookup"><span data-stu-id="ebe98-190">The code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="ebe98-191">O loop termina em média de $ \frac {8} {5} $ repetições.</span><span class="sxs-lookup"><span data-stu-id="ebe98-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="ebe98-192">Consulte [*repetir-até-êxito: decomposição não determinística de unidades de qubit único*](https://arxiv.org/abs/1311.1074) (Paetznick e Svore, 2014) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="ebe98-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="ebe98-193">RUS para preparar um estado Quantum</span><span class="sxs-lookup"><span data-stu-id="ebe98-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="ebe98-194">Finalmente, aqui está um exemplo de um padrão RUS para preparar um Quantum State $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, começando pelo Estado $ \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="ebe98-194">Finally, here is an example of an RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>

<span data-ttu-id="ebe98-195">Os recursos programáticos notáveis mostrados nesta operação são:</span><span class="sxs-lookup"><span data-stu-id="ebe98-195">Notable programmatic features shown in this operation are:</span></span>

* <span data-ttu-id="ebe98-196">Uma parte mais complexa `fixup` do loop, que envolve operações de Quantum.</span><span class="sxs-lookup"><span data-stu-id="ebe98-196">A more complex `fixup` part of the loop, which involves quantum operations.</span></span> 
* <span data-ttu-id="ebe98-197">O uso de `AssertMeasurementProbability` instruções para avaliar a probabilidade de medir o estado do Quantum em determinados pontos especificados no programa.</span><span class="sxs-lookup"><span data-stu-id="ebe98-197">The use of `AssertMeasurementProbability` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>

<span data-ttu-id="ebe98-198">Para obter mais informações sobre [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) as [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) operações e, consulte [testando e Depurando](xref:microsoft.quantum.guide.testingdebugging).</span><span class="sxs-lookup"><span data-stu-id="ebe98-198">For more information about the [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) and [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) operations, see [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging).</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertMeasurementProbability(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertMeasurementProbability(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertMeasurementProbability(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

<span data-ttu-id="ebe98-199">Para obter mais informações, consulte [exemplo de teste de unidade fornecido com a biblioteca padrão](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="ebe98-199">For more information, see [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

## <a name="next-steps"></a><span data-ttu-id="ebe98-200">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="ebe98-200">Next steps</span></span>

<span data-ttu-id="ebe98-201">Saiba mais sobre [teste e depuração](xref:microsoft.quantum.guide.testingdebugging) no Q# .</span><span class="sxs-lookup"><span data-stu-id="ebe98-201">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>
