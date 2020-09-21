---
title: Fluxo de controle em Q#
description: Loops, condicionais, etc.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
no-loc:
- Q#
- $$v
ms.openlocfilehash: 547c57cab67443e8b487bf817eb79fc922b43cdc
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833515"
---
# <a name="control-flow-in-no-locq"></a>Fluxo de controle em Q#

Em uma operação ou função, cada instrução é executada em ordem, semelhante a outros idiomas clássicos imperativos comuns.
No entanto, você pode modificar o fluxo de controle de três maneiras distintas:

* `if` instruções
* `for` loops
* `repeat-until-success` loops
* conjugações ( `apply-within` instruções)

As `if` `for` construções de fluxo de controle e passam em um sentido familiar para a maioria das linguagens de programação clássicas. [`Repeat-until-success`](#repeat-until-success-loop) os loops e os [conjugados](#conjugations) são discutidos posteriormente neste artigo.

Importante, `for` loops e `if` instruções podem ser usados em operações para as quais as [especializações](xref:microsoft.quantum.guide.operationsfunctions) são geradas automaticamente. Nesse cenário, o adjoin de um `for` loop inverte a direção e usa o adjacente de cada iteração.
Esta ação segue o princípio de "calçados e-Socks": se você deseja desfazer a colocação em SOCKS e, em seguida, os sapatos, você deve desfazer a colocação de sapatos e, em seguida, desfazer a colocação em Socks. 

## <a name="if-else-if-else"></a>If, else-if, Else

A `if` instrução dá suporte ao processamento condicional.
Ele consiste na palavra-chave `if` , uma expressão booliana entre parênteses e um bloco de instrução (o bloco _then_ ).
Opcionalmente, qualquer número de cláusulas else-if pode seguir, cada uma delas consiste na palavra-chave `elif` , uma expressão booliana entre parênteses e um bloco de instrução (o bloco _else-if_ ).
Por fim, a instrução pode, opcionalmente, ser concluída com uma cláusula else, que consiste na palavra-chave `else` seguida por outro bloco de instrução (o bloco _else_ ).

A `if` condição é avaliada e, se for *verdadeira*, o bloco *then* será executado.
Se a condição for *falsa*, a primeira condição IF-IF será avaliada; Se isso for verdadeiro, o bloco *else-if* será executado.
Caso contrário, o segundo bloco else é avaliado e, em seguida, o terceiro, e assim por diante, até que seja encontrada uma cláusula com uma condição true ou que não haja mais cláusulas If-If.
Se a condição *If* original e todas as cláusulas else-if forem avaliadas como *false*, o bloco *else* será executado, se fornecido.

Observe que qualquer bloco é executado, ele é executado dentro de seu próprio escopo.
Associações feitas dentro de um `if` bloco, `elif` ou `else` não são visíveis depois que o bloco termina.

Por exemplo,

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
ou
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

## <a name="for-loop"></a>Loop for

A `for` instrução dá suporte à iteração em um intervalo de inteiros ou em uma matriz.
A instrução consiste na palavra-chave `for` , seguida por uma tupla de símbolo ou símbolo, a palavra-chave `in` e uma expressão de tipo `Range` ou matriz, todas entre parênteses e um bloco de instruções.

O bloco de instrução (o corpo do loop) é executado repetidamente, com o símbolo definido (a variável de loop) associado a cada valor no intervalo ou na matriz.
Observe que, se a expressão de intervalo for avaliada como um intervalo ou uma matriz vazia, o corpo não será executado.
A expressão é totalmente avaliada antes de entrar no loop e não é alterada enquanto o loop está em execução.

A variável de loop é associada a cada entrada no corpo do loop e é desassociada no final do corpo.
A variável de loop não está associada após a conclusão do loop for.
A associação da variável de loop é imutável e segue as mesmas regras que outras associações de variáveis. 

Nestes exemplos, `qubits` é um registro de qubits (ou seja, do tipo `Qubit[]` ), 

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

Observe que, no final, utilizamos o operador binário aritmético-Shift-Left, `<<<` . Para obter mais informações, consulte [expressões numéricas](xref:microsoft.quantum.guide.expressions#numeric-expressions).

## <a name="repeat-until-success-loop"></a>Repetir-loop Until-êxito

A Q# linguagem permite que o fluxo de controle clássico dependa dos resultados da medição de qubits.
Essa funcionalidade, por sua vez, permite a implementação de gadgets probabilística eficientes que podem reduzir o custo computacional para a implementação de unidades.
Exemplos disso são os padrões de " *repetir-até-êxito* " (RUS) no Q# .
Esses padrões de RUS são programas probabilística que têm um baixo custo *esperado* em termos de Gates elementares; o custo incorrido depende da execução real e da intercalação das várias ramificações possíveis.

Para facilitar os padrões do RUS (repetição até o êxito), Q# o dá suporte às construções

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

em que `expression` é qualquer expressão válida que seja avaliada como um valor do tipo `Bool` .
O corpo do loop é executado e, em seguida, a condição é avaliada.
Se a condição for verdadeira, a instrução será concluída; caso contrário, a correção é executada e a instrução é executada novamente, começando com o corpo do loop.

Todas as três partes de um loop RUS (o corpo, o teste e a correção) são tratadas como um único escopo *para cada repetição*, de modo que os símbolos associados ao corpo estejam disponíveis no teste e na correção.
No entanto, concluir a execução da correção encerra o escopo da instrução, para que as associações de símbolo feitas durante o corpo ou correção não estejam disponíveis em repetições subsequentes.

Além disso, a `fixup` instrução geralmente é útil, mas nem sempre é necessária.
Em casos em que não é necessário, a construção

```qsharp
repeat {
    // do stuff
}
until (expression);
```

também é um padrão RUS válido.

Para obter mais exemplos e detalhes, consulte os [exemplos de repetir-até-êxito](#repeat-until-success-examples) neste artigo.

> [!TIP]   
> Evite usar loops repetir-até-sucesso dentro de funções. Use loops *while* para fornecer a funcionalidade correspondente dentro das funções. 

## <a name="while-loop"></a>Loop while

Os padrões de repetição-até-sucesso têm uma connotação de muito Quantum específica. Eles são amplamente usados em classes específicas de algoritmos Quantum, portanto, a construção de linguagem dedicada no Q# . No entanto, os loops que quebram com base em uma condição e cujo comprimento de execução é, portanto, desconhecido em tempo de compilação, são tratados com cuidado específico em um tempo de execução do Quantum. No entanto, seu uso dentro de funções não é problemático, pois esses loops contêm apenas um código que é executado em hardware convencional (sem Quantum). 

Q#o, portanto, dá suporte ao uso de loops while apenas dentro de funções.
Uma `while` instrução consiste na palavra-chave `while` , uma expressão booliana entre parênteses e um bloco de instruções.
O bloco de instrução (o corpo do loop) é executado contanto que a condição seja avaliada como `true` .

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="conjugations"></a>Conjugações

Em contraste com os bits clássicos, liberar memória Quantum é um pouco mais envolvida, uma vez que a redefinição oculta de qubits pode ter efeitos indesejados na computação restante se o qubits ainda for confusas. Esses efeitos podem ser evitados de forma adequada "desfazer" as computações realizadas antes de liberar a memória. Um padrão comum na computação Quantum é, portanto, o seguinte: 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

Q# dá suporte a uma instrução de conjugação que implementa a transformação anterior. Usando essa instrução, a operação `ApplyWith` pode ser implementada da seguinte maneira:

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
Essa instrução de conjugação se torna útil se as transformações externas e internas não estão prontamente disponíveis como operações, mas são mais convenientes de descrever por um bloco consistindo em várias instruções. 

A transformação inversa para as instruções definidas no bloco Within é gerada automaticamente pelo compilador e executada após a conclusão do bloco de aplicação.
Como as variáveis mutáveis usadas como parte do bloco Within não podem ser reassociadas no bloco Apply, a transformação gerada é garantida como sendo a adjoin do cálculo no bloco Within. 

## <a name="return-statement"></a>Instrução Return

A instrução return encerra a execução de uma operação ou função e retorna um valor para o chamador.
Ele consiste na palavra-chave `return` , seguida por uma expressão do tipo apropriado e um ponto e vírgula de terminação.

Por exemplo,
```qsharp
return 1;
```
ou
```qsharp
return (results, qubits);
```

* Um callable que retorna uma tupla vazia, `()` , não requer uma instrução de retorno.
* Para especificar uma saída antecipada da operação ou da função, use `return ();` .
Os chamadores que retornam qualquer outro tipo exigem uma instrução de retorno final.
* Não há um número máximo de instruções de retorno em uma operação.
O compilador pode emitir um aviso se as instruções seguirem uma instrução return dentro de um bloco.

   
## <a name="fail-statement"></a>Instrução Fail

A instrução Fail encerra a execução de uma operação e retorna um valor de erro para o chamador.
Ele consiste na palavra-chave `fail` , seguida por uma cadeia de caracteres e um ponto e vírgula de terminação.
A instrução retorna a cadeia de caracteres para o driver clássico como a mensagem de erro.

Não há nenhuma restrição quanto ao número de instruções de falha em uma operação.
O compilador pode emitir um aviso se as instruções seguirem uma instrução Fail dentro de um bloco.

Por exemplo,

```qsharp
fail $"Impossible state reached";
```
ou, usando [cadeias de caracteres interpoladas](xref:microsoft.quantum.guide.expressions#interpolated-strings),
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a>Exemplos de repetição-até-êxito

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a>Padrão RUS para rotação de qubit único sobre um eixo irracional 

Em um caso de uso típico, a Q# operação a seguir implementa uma rotação em um eixo irracional de $ (I + 2i Z)/\sqrt {5} $ na esfera de Bloch. A implementação usa um padrão RUS conhecido:

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

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a>Loop RUS com uma variável mutável no escopo

Este exemplo mostra o uso de uma variável mutável, `finished` , que está dentro do escopo de todo o loop Repeat-Until-recorretion e que é inicializado antes do loop e atualizado na etapa de correção.

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

### <a name="rus-without-fixup"></a>RUS sem `fixup`

Este exemplo mostra um loop RUS sem a etapa de correção. O código é um circuito probabilística que implementa um portão de rotação importante $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ usando `H` as `T` Gates e.
O loop termina em média de $ \frac {8} {5} $ repetições.
Consulte [*repetir-até-êxito: decomposição não determinística de unidades de qubit único*](https://arxiv.org/abs/1311.1074) (Paetznick e Svore, 2014) para obter mais detalhes.

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

### <a name="rus-to-prepare-a-quantum-state"></a>RUS para preparar um estado Quantum

Finalmente, aqui está um exemplo de um padrão RUS para preparar um Quantum State $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, começando pelo Estado $ \ket{+} $.

Os recursos programáticos notáveis mostrados nesta operação são:

* Uma parte mais complexa `fixup` do loop, que envolve operações de Quantum. 
* O uso de `AssertMeasurementProbability` instruções para avaliar a probabilidade de medir o estado do Quantum em determinados pontos especificados no programa.

Para obter mais informações sobre [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) as [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) operações e, consulte [testando e Depurando](xref:microsoft.quantum.guide.testingdebugging).

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

Para obter mais informações, consulte [exemplo de teste de unidade fornecido com a biblioteca padrão](https://github.com/microsoft/Quantum/blob/main/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):

## <a name="next-steps"></a>Próximas etapas

Saiba mais sobre [teste e depuração](xref:microsoft.quantum.guide.testingdebugging) no Q# .
