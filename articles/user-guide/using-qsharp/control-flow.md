---
title: 'Fluxo de controle em p #'
description: Loops, condicionais, etc.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: c534e016fcb8b50e66c11ca29c253ba0512acc6e
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430944"
---
# <a name="control-flow-in-q"></a><span data-ttu-id="5f7e4-103">Fluxo de controle em p #</span><span class="sxs-lookup"><span data-stu-id="5f7e4-103">Control Flow in Q#</span></span>

<span data-ttu-id="5f7e4-104">Em uma operação ou função, cada instrução é executada em ordem, semelhante às linguagens clássicas mais comuns.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-104">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="5f7e4-105">No entanto, esse fluxo de controle pode ser modificado de três maneiras distintas:</span><span class="sxs-lookup"><span data-stu-id="5f7e4-105">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="5f7e4-106">`if`instruções</span><span class="sxs-lookup"><span data-stu-id="5f7e4-106">`if` statements</span></span>
- <span data-ttu-id="5f7e4-107">`for`loops</span><span class="sxs-lookup"><span data-stu-id="5f7e4-107">`for` loops</span></span>
- <span data-ttu-id="5f7e4-108">`repeat`-`until`loops</span><span class="sxs-lookup"><span data-stu-id="5f7e4-108">`repeat`-`until` loops</span></span>

<span data-ttu-id="5f7e4-109">Adiamos a discussão do último [para mais adiante](#repeat-until-success-loop).</span><span class="sxs-lookup"><span data-stu-id="5f7e4-109">We defer discussion of the latter to further [below](#repeat-until-success-loop).</span></span>
<span data-ttu-id="5f7e4-110">As `if` `for` construções de fluxo de controle e, no entanto, prosseguem de forma familiar para a maioria das linguagens de programação clássicas.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-110">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>

<span data-ttu-id="5f7e4-111">Importante, `for` loops e `if` instruções podem até mesmo ser usados em operações para as quais as especializações são geradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-111">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="5f7e4-112">Nesse caso, o adjoin de um `for` loop inverte a direção e usa o modo adjacente de cada iteração.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-112">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="5f7e4-113">Isso segue o princípio "sapatos-and-Socks": se você deseja desfazer a colocação em SOCKS e, em seguida, os sapatos, você deve desfazer a colocação de sapatos e, em seguida, desfazer a colocação em Socks.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-113">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="5f7e4-114">Ele funciona decididamente menos bem para tentar e retomar seus Socks enquanto você ainda estiver aproveitando seus sapatos!</span><span class="sxs-lookup"><span data-stu-id="5f7e4-114">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="if-else-if-else"></a><span data-ttu-id="5f7e4-115">If, else-if, Else</span><span class="sxs-lookup"><span data-stu-id="5f7e4-115">If, Else-if, Else</span></span>

<span data-ttu-id="5f7e4-116">A `if` instrução dá suporte à execução condicional.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-116">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="5f7e4-117">Ele consiste na palavra-chave `if` , um parêntese de abertura `(` , uma expressão booleana, um parêntese de fechamento `)` e um bloco de instrução (o bloco _then_ ).</span><span class="sxs-lookup"><span data-stu-id="5f7e4-117">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="5f7e4-118">Isso pode ser seguido por qualquer número de cláusulas else-if, cada uma das quais consiste na palavra-chave `elif` , um parêntese de abertura `(` , uma expressão booleana, um parêntese de fechamento `)` e um bloco de instrução (o bloco _else-if_ ).</span><span class="sxs-lookup"><span data-stu-id="5f7e4-118">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="5f7e4-119">Por fim, a instrução pode, opcionalmente, ser concluída com uma cláusula else, que consiste na palavra-chave `else` seguida por outro bloco de instrução (o bloco _else_ ).</span><span class="sxs-lookup"><span data-stu-id="5f7e4-119">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="5f7e4-120">A `if` condição é avaliada e, se for verdadeira, o bloco then será executado.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-120">The `if` condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="5f7e4-121">Se a condição for falsa, a primeira condição IF-IF será avaliada; Se for true, o bloco else if será executado.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-121">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="5f7e4-122">Caso contrário, o segundo bloco else é testado e, em seguida, o terceiro, e assim por diante, até que seja encontrada uma cláusula com uma condição true ou que não haja mais cláusulas If-If.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-122">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="5f7e4-123">Se a condição if original e todas as cláusulas If forem avaliadas como false, o bloco else será executado se um for fornecido.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-123">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="5f7e4-124">Observe que qualquer bloco executado é executado em seu próprio escopo.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-124">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="5f7e4-125">Associações feitas dentro de um `if` bloco, `elif` ou `else` não são visíveis após seu fim.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-125">Bindings made inside of an `if`, `elif`, or `else` block are not visible after its end.</span></span>

<span data-ttu-id="5f7e4-126">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="5f7e4-126">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="5f7e4-127">ou</span><span class="sxs-lookup"><span data-stu-id="5f7e4-127">or</span></span>
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

## <a name="for-loop"></a><span data-ttu-id="5f7e4-128">Loop For</span><span class="sxs-lookup"><span data-stu-id="5f7e4-128">For Loop</span></span>

<span data-ttu-id="5f7e4-129">A `for` instrução dá suporte à iteração em um intervalo de inteiros ou em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-129">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="5f7e4-130">A instrução consiste na palavra-chave `for` , um parênteses aberto `(` , seguida por uma tupla de símbolo ou símbolo, a palavra-chave `in` , uma expressão de tipo `Range` ou matriz, um parêntese de fechamento `)` e um bloco de instrução.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-130">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="5f7e4-131">O bloco de instrução (o corpo do loop) é executado repetidamente, com os símbolos definidos (as variáveis de loop) associadas a cada valor no intervalo ou na matriz.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-131">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="5f7e4-132">Observe que, se a expressão de intervalo for avaliada como um intervalo ou uma matriz vazia, o corpo não será executado.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-132">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="5f7e4-133">A expressão é totalmente avaliada antes de entrar no loop e não será alterada enquanto o loop estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-133">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="5f7e4-134">A variável de loop é associada a cada entrada no corpo do loop e desassociada no final do corpo.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-134">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="5f7e4-135">Em particular, a variável de loop não é associada depois que o loop for é concluído.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-135">In particular, the loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="5f7e4-136">A Associação dos símbolos declarados é imutável e segue as mesmas regras que outras associações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-136">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="5f7e4-137">Para alguns exemplos, suponhamos `qubits` é um registro de qubits (ou seja, do tipo `Qubit[]` ),</span><span class="sxs-lookup"><span data-stu-id="5f7e4-137">For some examples, supposing `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

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
<span data-ttu-id="5f7e4-138">Observe que, no final, utilizamos o operador binário aritmético-Shift-Left, `<<<` , os detalhes que podem ser encontrados em [expressões numéricas](xref:microsoft.quantum.guide.expressions#numeric-expressions)</span><span class="sxs-lookup"><span data-stu-id="5f7e4-138">Note that at the end we utilized the arithmetic-shift-left binary operator, `<<<`, details of which can be found at [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions)</span></span>


## <a name="repeat-until-success-loop"></a><span data-ttu-id="5f7e4-139">Repetir-loop Until-êxito</span><span class="sxs-lookup"><span data-stu-id="5f7e4-139">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="5f7e4-140">A linguagem Q # permite que o fluxo de controle clássico dependa dos resultados da medição de qubits.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="5f7e4-141">Esse recurso, por sua vez, habilita a implementação de gadgets probabilística poderosos que podem reduzir o custo computacional para a implementação de unidades.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-141">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="5f7e4-142">Por exemplo, é fácil implementar os chamados padrões de " *repetir até o êxito* " (RUS) em Q #.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-142">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="5f7e4-143">Esses padrões de RUS são programas probabilística que têm um baixo custo *esperado* em termos de Gates elementares, mas para os quais o custo real depende de uma execução e de uma intercalação real de várias ramificações possíveis.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="5f7e4-144">Para facilitar os padrões do RUS (repetição até o sucesso), o Q # dá suporte às construções</span><span class="sxs-lookup"><span data-stu-id="5f7e4-144">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="5f7e4-145">em que `expression` é qualquer expressão válida que seja avaliada como um valor do tipo `Bool` .</span><span class="sxs-lookup"><span data-stu-id="5f7e4-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="5f7e4-146">O corpo do loop é executado e a condição é avaliada.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-146">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="5f7e4-147">Se a condição for verdadeira, a instrução será concluída; caso contrário, a correção será executada e a instrução será executada novamente começando com o corpo do loop.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-147">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>

<span data-ttu-id="5f7e4-148">Todas as três partes de um loop repetir/até (o corpo, o teste e a correção) são tratadas como um único escopo *para cada repetição*, de modo que os símbolos associados ao corpo estão disponíveis no teste e no conserto.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-148">All three portions of a repeat/until loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in the test and in the fixup.</span></span>
<span data-ttu-id="5f7e4-149">No entanto, concluir a execução da correção encerra o escopo da instrução, para que as associações de símbolo feitas durante o corpo ou correção não estejam disponíveis em repetições subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-149">However completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="5f7e4-150">Além disso, a `fixup` instrução geralmente é útil, mas nem sempre é necessária.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="5f7e4-151">Em casos em que não é necessário, a construção</span><span class="sxs-lookup"><span data-stu-id="5f7e4-151">In cases that it is not needed, the construct</span></span>
```qsharp
repeat {
    // do stuff
}
until (expression);
```
<span data-ttu-id="5f7e4-152">também é um padrão RUS válido.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="5f7e4-153">Na parte inferior desta página, apresentamos alguns [exemplos de loops de Rus](#repeat-until-success-examples).</span><span class="sxs-lookup"><span data-stu-id="5f7e4-153">At the bottom of this page we present some [examples of RUS loops](#repeat-until-success-examples).</span></span>

> [!TIP]   
> <span data-ttu-id="5f7e4-154">Evite usar loops repetir-até-sucesso dentro de funções.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="5f7e4-155">A funcionalidade correspondente é fornecida por loops em funções do.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-155">The corresponding functionality is provided by while loops in functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="5f7e4-156">Loop while</span><span class="sxs-lookup"><span data-stu-id="5f7e4-156">While Loop</span></span>

<span data-ttu-id="5f7e4-157">Os padrões de repetição-até-sucesso têm uma connotação de muito Quantum específica.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="5f7e4-158">Eles são amplamente usados em classes específicas de algoritmos Quantum, portanto, a construção de linguagem dedicada em Q #.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-158">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="5f7e4-159">No entanto, os loops que quebram com base em uma condição e cujo comprimento de execução é, portanto, desconhecido em tempo de compilação precisam ser manipulados com cuidado específico em um tempo de execução do Quantum.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-159">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="5f7e4-160">Seu uso dentro de funções por outro lado é inproblemático, pois elas contêm apenas o código que será executado em hardware convencional (sem Quantum).</span><span class="sxs-lookup"><span data-stu-id="5f7e4-160">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="5f7e4-161">O Q #, portanto, dá suporte ao uso de loops while apenas dentro de funções.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-161">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="5f7e4-162">Uma `while` instrução consiste na palavra-chave `while` , um parêntese de abertura `(` , uma condição (ou seja, uma expressão booliana), um parêntese de fechamento `)` e um bloco de instruções.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-162">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="5f7e4-163">O bloco de instrução (o corpo do loop) é executado contanto que a condição seja avaliada como `true` .</span><span class="sxs-lookup"><span data-stu-id="5f7e4-163">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```


## <a name="return-statement"></a><span data-ttu-id="5f7e4-164">Instrução Return</span><span class="sxs-lookup"><span data-stu-id="5f7e4-164">Return Statement</span></span>

<span data-ttu-id="5f7e4-165">A instrução return encerra a execução de uma operação ou função e retorna um valor para o chamador.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-165">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="5f7e4-166">Ele consiste na palavra-chave `return` , seguida por uma expressão do tipo apropriado e um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="5f7e4-167">Um callable que retorna uma tupla vazia, `()` , não requer uma instrução de retorno.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-167">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="5f7e4-168">Se uma saída antecipada for desejada, `return ()` ela poderá ser usada nesse caso.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-168">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="5f7e4-169">Os chamadores que retornam qualquer outro tipo exigem uma instrução de retorno final.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-169">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="5f7e4-170">Não há um número máximo de instruções de retorno em uma operação.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-170">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="5f7e4-171">O compilador pode emitir um aviso se as instruções seguirem uma instrução return dentro de um bloco.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-171">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="5f7e4-172">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="5f7e4-172">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="5f7e4-173">ou</span><span class="sxs-lookup"><span data-stu-id="5f7e4-173">or</span></span>
```qsharp
return ();
```
<span data-ttu-id="5f7e4-174">ou</span><span class="sxs-lookup"><span data-stu-id="5f7e4-174">or</span></span>
```qsharp
return (results, qubits);
```

## <a name="fail-statement"></a><span data-ttu-id="5f7e4-175">Instrução Fail</span><span class="sxs-lookup"><span data-stu-id="5f7e4-175">Fail Statement</span></span>

<span data-ttu-id="5f7e4-176">A instrução Fail encerra a execução de uma operação e retorna um valor de erro para o chamador.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-176">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="5f7e4-177">Ele consiste na palavra-chave `fail` , seguida por uma cadeia de caracteres e um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-177">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="5f7e4-178">A cadeia de caracteres é retornada ao driver clássico como a mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-178">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="5f7e4-179">Não há nenhuma restrição quanto ao número de instruções de falha em uma operação.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-179">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="5f7e4-180">O compilador pode emitir um aviso se as instruções seguirem uma instrução Fail dentro de um bloco.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-180">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="5f7e4-181">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="5f7e4-181">For example,</span></span>
```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="5f7e4-182">ou, usando [cadeias de caracteres interpoladas](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span><span class="sxs-lookup"><span data-stu-id="5f7e4-182">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="5f7e4-183">Exemplos de repetição-até-êxito</span><span class="sxs-lookup"><span data-stu-id="5f7e4-183">Repeat-Until-Success Examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="5f7e4-184">Padrão RUS para rotação de qubit única sobre um eixo irracional</span><span class="sxs-lookup"><span data-stu-id="5f7e4-184">RUS pattern for single qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="5f7e4-185">Em um caso de uso típico, a seguinte operação Q # implementa uma rotação em um eixo irracional de $ (I + 2i Z)/\sqrt {5} $ na esfera de Bloch.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-185">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="5f7e4-186">Isso é feito usando um padrão de RUS conhecido:</span><span class="sxs-lookup"><span data-stu-id="5f7e4-186">This is accomplished by using a known RUS pattern:</span></span>

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

### <a name="rus-loop-with-mutable-variable-in-scope"></a><span data-ttu-id="5f7e4-187">Loop RUS com variável mutável no escopo</span><span class="sxs-lookup"><span data-stu-id="5f7e4-187">RUS loop with mutable variable in scope</span></span>

<span data-ttu-id="5f7e4-188">Este exemplo mostra o uso de uma variável mutável `finished` que está no escopo de todo o loop Repeat-Until-recorretion e que é inicializado antes do loop e atualizado na etapa de correção.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-188">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

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

### <a name="rus-without-fixup"></a><span data-ttu-id="5f7e4-189">RUS sem`fixup`</span><span class="sxs-lookup"><span data-stu-id="5f7e4-189">RUS without `fixup`</span></span>

<span data-ttu-id="5f7e4-190">Por exemplo, o código a seguir é um circuito probabilística que implementa um portão de rotação importante $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ usando as `H` `T` Gates e.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-190">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="5f7e4-191">O loop termina em média de $ \frac {8} {5} $ repetições.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="5f7e4-192">Consulte [*repetir-até-êxito: decomposição não determinística de unidades de qubit único*](https://arxiv.org/abs/1311.1074) (Paetznick e Svore, 2014) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

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

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="5f7e4-193">RUS para preparar um estado Quantum</span><span class="sxs-lookup"><span data-stu-id="5f7e4-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="5f7e4-194">Por fim, mostramos um exemplo de um padrão RUS para preparar um Quantum State $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, a partir do estado $ \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-194">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="5f7e4-195">Consulte também o [exemplo de teste de unidade fornecido com a biblioteca padrão](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="5f7e4-195">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
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

<span data-ttu-id="5f7e4-196">Os recursos programáticos notáveis mostrados nesta operação são uma parte mais complexa `fixup` do loop, que envolve operações de Quantum e o uso de `AssertProb` instruções para avaliar a probabilidade de medir o estado Quantum em determinados pontos especificados no programa.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-196">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="5f7e4-197">Consulte também [testando e Depurando](xref:microsoft.quantum.guide.testingdebugging) para obter mais informações sobre as [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operações e.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-197">See also [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>


## <a name="whats-next"></a><span data-ttu-id="5f7e4-198">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="5f7e4-198">What's Next?</span></span>
<span data-ttu-id="5f7e4-199">Saiba mais sobre [teste e depuração](xref:microsoft.quantum.guide.testingdebugging) em Q #.</span><span class="sxs-lookup"><span data-stu-id="5f7e4-199">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>