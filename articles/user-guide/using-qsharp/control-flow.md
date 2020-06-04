---
title: 'Fluxo de controle em p #'
description: Loops, condicionais, etc.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: 1f1b641563fe35879abeee32b4f0aeeb7001b1a0
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84326533"
---
# <a name="control-flow-in-q"></a>Fluxo de controle em p #

Em uma operação ou função, cada instrução é executada em ordem, semelhante às linguagens clássicas mais comuns.
No entanto, esse fluxo de controle pode ser modificado de três maneiras distintas:

- `if`instruções
- `for`loops
- `repeat`-`until`loops

Adiamos a discussão do último [para mais adiante](#repeat-until-success-loop).
As `if` `for` construções de fluxo de controle e, no entanto, prosseguem de forma familiar para a maioria das linguagens de programação clássicas.

Importante, `for` loops e `if` instruções podem até mesmo ser usados em operações para as quais as especializações são geradas automaticamente. Nesse caso, o adjoin de um `for` loop inverte a direção e usa o modo adjacente de cada iteração.
Isso segue o princípio "sapatos-and-Socks": se você deseja desfazer a colocação em SOCKS e, em seguida, os sapatos, você deve desfazer a colocação de sapatos e, em seguida, desfazer a colocação em Socks.
Ele funciona decididamente menos bem para tentar e retomar seus Socks enquanto você ainda estiver aproveitando seus sapatos!

## <a name="if-else-if-else"></a>If, else-if, Else

A `if` instrução dá suporte à execução condicional.
Ele consiste na palavra-chave `if` , um parêntese de abertura `(` , uma expressão booleana, um parêntese de fechamento `)` e um bloco de instrução (o bloco _then_ ).
Isso pode ser seguido por qualquer número de cláusulas else-if, cada uma das quais consiste na palavra-chave `elif` , um parêntese de abertura `(` , uma expressão booleana, um parêntese de fechamento `)` e um bloco de instrução (o bloco _else-if_ ).
Por fim, a instrução pode, opcionalmente, ser concluída com uma cláusula else, que consiste na palavra-chave `else` seguida por outro bloco de instrução (o bloco _else_ ).

A `if` condição é avaliada e, se for verdadeira, o bloco then será executado.
Se a condição for falsa, a primeira condição IF-IF será avaliada; Se for true, o bloco else if será executado.
Caso contrário, o segundo bloco else é testado e, em seguida, o terceiro, e assim por diante, até que seja encontrada uma cláusula com uma condição true ou que não haja mais cláusulas If-If.
Se a condição if original e todas as cláusulas If forem avaliadas como false, o bloco else será executado se um for fornecido.

Observe que qualquer bloco executado é executado em seu próprio escopo.
Associações feitas dentro de um `if` bloco, `elif` ou `else` não são visíveis após seu fim.

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

## <a name="for-loop"></a>Loop For

A `for` instrução dá suporte à iteração em um intervalo de inteiros ou em uma matriz.
A instrução consiste na palavra-chave `for` , um parênteses aberto `(` , seguida por uma tupla de símbolo ou símbolo, a palavra-chave `in` , uma expressão de tipo `Range` ou matriz, um parêntese de fechamento `)` e um bloco de instrução.

O bloco de instrução (o corpo do loop) é executado repetidamente, com os símbolos definidos (as variáveis de loop) associadas a cada valor no intervalo ou na matriz.
Observe que, se a expressão de intervalo for avaliada como um intervalo ou uma matriz vazia, o corpo não será executado.
A expressão é totalmente avaliada antes de entrar no loop e não será alterada enquanto o loop estiver em execução.

A variável de loop é associada a cada entrada no corpo do loop e desassociada no final do corpo.
Em particular, a variável de loop não é associada depois que o loop for é concluído.
A Associação dos símbolos declarados é imutável e segue as mesmas regras que outras associações de variáveis. 

Para alguns exemplos, suponhamos `qubits` é um registro de qubits (ou seja, do tipo `Qubit[]` ), 

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
Observe que, no final, utilizamos o operador binário aritmético-Shift-Left, `<<<` , os detalhes que podem ser encontrados em [expressões numéricas](xref:microsoft.quantum.guide.expressions#numeric-expressions)


## <a name="repeat-until-success-loop"></a>Repetir-loop Until-êxito

A linguagem Q # permite que o fluxo de controle clássico dependa dos resultados da medição de qubits.
Esse recurso, por sua vez, habilita a implementação de gadgets probabilística poderosos que podem reduzir o custo computacional para a implementação de unidades.
Por exemplo, é fácil implementar os chamados padrões de " *repetir até o êxito* " (RUS) em Q #.
Esses padrões de RUS são programas probabilística que têm um baixo custo *esperado* em termos de Gates elementares, mas para os quais o custo real depende de uma execução e de uma intercalação real de várias ramificações possíveis.

Para facilitar os padrões do RUS (repetição até o sucesso), o Q # dá suporte às construções

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
O corpo do loop é executado e a condição é avaliada.
Se a condição for verdadeira, a instrução será concluída; caso contrário, a correção será executada e a instrução será executada novamente começando com o corpo do loop.

Todas as três partes de um loop repetir/até (o corpo, o teste e a correção) são tratadas como um único escopo *para cada repetição*, de modo que os símbolos associados ao corpo estão disponíveis no teste e no conserto.
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

Na parte inferior desta página, apresentamos alguns [exemplos de loops de Rus](#repeat-until-success-examples).

> [!TIP]   
> Evite usar loops repetir-até-sucesso dentro de funções. A funcionalidade correspondente é fornecida por loops em funções do. 

## <a name="while-loop"></a>Loop while

Os padrões de repetição-até-sucesso têm uma connotação de muito Quantum específica. Eles são amplamente usados em classes específicas de algoritmos Quantum, portanto, a construção de linguagem dedicada em Q #. No entanto, os loops que quebram com base em uma condição e cujo comprimento de execução é, portanto, desconhecido em tempo de compilação precisam ser manipulados com cuidado específico em um tempo de execução do Quantum. Seu uso dentro de funções por outro lado é inproblemático, pois elas contêm apenas o código que será executado em hardware convencional (sem Quantum). 

O Q #, portanto, dá suporte ao uso de loops while apenas dentro de funções. Uma `while` instrução consiste na palavra-chave `while` , um parêntese de abertura `(` , uma condição (ou seja, uma expressão booliana), um parêntese de fechamento `)` e um bloco de instruções.
O bloco de instrução (o corpo do loop) é executado contanto que a condição seja avaliada como `true` .

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```


## <a name="return-statement"></a>Instrução Return

A instrução return encerra a execução de uma operação ou função e retorna um valor para o chamador.
Ele consiste na palavra-chave `return` , seguida por uma expressão do tipo apropriado e um ponto e vírgula de terminação.

Um callable que retorna uma tupla vazia, `()` , não requer uma instrução de retorno.
Se uma saída antecipada for desejada, `return ()` ela poderá ser usada nesse caso.
Os chamadores que retornam qualquer outro tipo exigem uma instrução de retorno final.

Não há um número máximo de instruções de retorno em uma operação.
O compilador pode emitir um aviso se as instruções seguirem uma instrução return dentro de um bloco.

Por exemplo,
```qsharp
return 1;
```
ou
```qsharp
return ();
```
ou
```qsharp
return (results, qubits);
```

## <a name="fail-statement"></a>Instrução Fail

A instrução Fail encerra a execução de uma operação e retorna um valor de erro para o chamador.
Ele consiste na palavra-chave `fail` , seguida por uma cadeia de caracteres e um ponto e vírgula de terminação.
A cadeia de caracteres é retornada ao driver clássico como a mensagem de erro.

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

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a>Padrão RUS para rotação de qubit única sobre um eixo irracional 

Em um caso de uso típico, a seguinte operação Q # implementa uma rotação em um eixo irracional de $ (I + 2i Z)/\sqrt {5} $ na esfera de Bloch. Isso é feito usando um padrão de RUS conhecido:

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

### <a name="rus-loop-with-mutable-variable-in-scope"></a>Loop RUS com variável mutável no escopo

Este exemplo mostra o uso de uma variável mutável `finished` que está no escopo de todo o loop Repeat-Until-recorretion e que é inicializado antes do loop e atualizado na etapa de correção.

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

### <a name="rus-without-fixup"></a>RUS sem`fixup`

Por exemplo, o código a seguir é um circuito probabilística que implementa um portão de rotação importante $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ usando as `H` `T` Gates e.
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

Por fim, mostramos um exemplo de um padrão RUS para preparar um Quantum State $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, a partir do estado $ \ket{+} $.
Consulte também o [exemplo de teste de unidade fornecido com a biblioteca padrão](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):

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

Os recursos programáticos notáveis mostrados nesta operação são uma parte mais complexa `fixup` do loop, que envolve operações de Quantum e o uso de `AssertProb` instruções para avaliar a probabilidade de medir o estado Quantum em determinados pontos especificados no programa.
Consulte também [testando e Depurando](xref:microsoft.quantum.guide.testingdebugging) para obter mais informações sobre as [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operações e.


## <a name="next-steps"></a>Próximas etapas

Saiba mais sobre [teste e depuração](xref:microsoft.quantum.guide.testingdebugging) em Q #.