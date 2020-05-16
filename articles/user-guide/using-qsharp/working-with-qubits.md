---
title: Trabalhar com qubits
description: Descrição do preenchimento
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: e89b9ccfe2a0796e01eedfc99f7ce71038d85f38
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430927"
---
# <a name="working-with-qubits"></a>Trabalhar com qubits

Agora que já vi uma variedade de diferentes partes da linguagem Q #, vamos nos aprofundar em tudo e ver como usar o qubits em si.

Observe que nenhuma dessas instruções é permitida dentro do corpo de uma função.
Eles só são válidos dentro de operações.

## <a name="allocating-qubits"></a>Alocando qubits

### <a name="clean-qubits"></a>Limpar qubits

A `using` instrução é usada para *alocar* novo qubits para uso durante um bloco de instruções.

A instrução consiste na palavra-chave `using` , seguida por um parêntese de abertura `(` , uma associação, um parêntese de fechamento `)` e o bloco de instrução dentro do qual o qubits estará disponível.
A associação segue o mesmo padrão que as `let` instruções: um único símbolo ou uma tupla de símbolos, seguido por um sinal de igual `=` , e um único valor ou uma tupla correspondente de *inicializadores*.

Inicializadores estão disponíveis para um único qubit, indicado como `Qubit()` , ou uma matriz de qubits, `Qubit[n]` , em que `n` é uma `Int` expressão.
Por exemplo,

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

Qualquer qubits alocada dessa maneira começa no estado $ \ket {0} $; no exemplo acima, `register` é, portanto, no estado $ \ket {00000} = \ket {0} \otimes \ket \otimes \cdots {0} \otimes \ket {0} $.
No final do `using` bloco, qualquer qubits alocada por esse bloco será imediatamente desalocada e não poderá mais ser usada.

> [!WARNING]
> As máquinas de destino esperam que qubits estejam no estado $ \ket {0} $ imediatamente antes da desalocação, para que possam ser reutilizadas e oferecidas a outros `using` blocos para alocação.
> Sempre que possível, use operações de unitário para retornar qualquer qubits alocado para $ \ket {0} $.
> Se necessário, a @"microsoft.quantum.intrinsic.reset" operação pode ser usada para medir um qubit em vez disso e usar esse resultado de medida para garantir que o qubit medido seja retornado para $ \ket {0} $. Essa medida destruirá qualquer Entanglement com a qubits restante e, portanto, poderá afetar a computação.


### <a name="borrowed-qubits"></a>Qubits emprestado

A `borrowing` instrução é usada para tornar o qubits disponível para uso temporário, que não precisa estar em um estado específico.

O mecanismo de empréstimo permite a alocação de qubits que pode ser usada como espaço transitório durante uma computação.
Esses qubits geralmente não estão em um estado limpo, ou seja, eles não são necessariamente inicializados em um estado conhecido, como $ \ket {0} $.
Essas são muitas vezes chamadas de qubits "sujas" porque seu estado é desconhecido e pode até mesmo ser confusas com outras partes da memória do computador Quantum.

A associação segue o mesmo padrão e regras que uma em uma `using` instrução.
Por exemplo,
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
O qubits emprestado está em um estado desconhecido e sai do escopo no final do bloco de instrução.
O tomador de confirmações para deixar o qubits no mesmo estado em que estavam emprestados, ou seja, seu estado no início e no final do bloco de instrução deve ser o mesmo.
Esse estado em particular não é necessariamente um estado clássico, de modo que, na maioria dos casos, os escopos emprestados não devem conter medidas. 

Ao emprestar qubits, o sistema primeiro tentará preencher a solicitação de qubits que estão em uso, mas que não são acessadas durante o corpo da `borrowing` instrução.
Se não houver tal qubits suficiente, ele alocará o novo qubits para concluir a solicitação.


Entre os casos de uso conhecidos de qubits sujos estão implementações de Gates de CNOT de vários controle que exigem apenas poucos qubits e implementação de incrementais.
Consulte o [exemplo de empréstimo de qubits](#borrowing-qubits-example) abaixo para ver um exemplo de seu uso em Q # ou a [*fatoração de papel usando 2n + 2 qubits com multiplicação modular baseada em Toffoli*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler e Svore 2017) para um algoritmo que utiliza qubits emprestados.


## <a name="intrinsic-operations"></a>Operações intrínsecas

Uma vez alocada, um qubit pode ser passado para funções e operações.
De certa forma, isso é tudo o que um programa Q # pode fazer com um qubit, pois as ações que podem ser executadas são todas definidas como operações.
Veremos essas operações com mais detalhes em [operações intrínsecas e funções](xref:microsoft.quantum.libraries.standard.prelude), mas, por enquanto, mencionamos algumas operações úteis que podem ser usadas para interagir com o qubits.

Primeiro, os operadores de Pauli de qubit único $X $, $Y $ e $Z $ são representados em Q # pelas operações intrínsecas `X` , `Y` e `Z` cada um deles tem um tipo `(Qubit => Unit is Adj + Ctl)` .
Conforme descrito em [operações intrínsecas e funções](xref:microsoft.quantum.libraries.standard.prelude), podemos imaginar $X $ e, portanto, `X` como uma operação de inversão de bits ou não de portão.
A `X` operação nos permite preparar Estados do formulário $ \ket{s_0 s_1 \dots s_n} $ para uma cadeia de caracteres de bits clássica $s $:

```qsharp
operation PrepareBitString(bitstring : Bool[], register : Qubit[]) : Unit
is Adj + Ctl {
    let nQubits = Length(register);
    for (idxQubit in 0..nQubits - 1) {
        if (bitstring[idxQubit]) {
            X(register[idxQubit]);
        }
    }
}

operation RunExample() : Unit {
    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
        // Resetting the qubits will allow us to deallocate them properly.
        ResetAll(register);
    }
}
```

> [!TIP]
> Mais tarde, veremos mais formas compactadas de gravar essa operação que não exigem controle de fluxo manual.

Também podemos preparar Estados como $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ e $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ usando o Hadamard Transform $H $, que é representado em Q # pela operação intrínseca `H : (Qubit => Unit is Adj + Ctl)` :

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString, above.
    PrepareBitString(bitstring, register);
    // Next, we use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the state we want.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a>Medidas

Usando a `Measure` operação, que é uma operação não-unitário intrínseca interna, podemos extrair informações clássicas de um objeto do tipo `Qubit` e atribuir um valor clássico como resultado, que tem um tipo reservado `Result` , indicando que o resultado não é mais um estado Quantum.
A entrada para `Measure` é um eixo Pauli na esfera Bloch, representado por um valor do tipo `Pauli` (por exemplo `PauliX` ) e um valor do tipo `Qubit` .

Um exemplo simples é a operação a seguir, que aloca um qubit no estado $ \ket {0} $ e, em seguida, aplica uma operação Hadamard `H` a ele e mede o resultado na `PauliZ` base.

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

Um exemplo um pouco mais complicado é dado pela seguinte operação, que retorna o valor booliano `true` se todos os qubits em um registro do tipo `Qubit[]` estiverem no estado zero quando medido em uma base de Pauli especificada e que retorna de `false` outra forma.

```qsharp
operation MeasureIfAllQubitsAreZero(qubits : Qubit[], pauli : Pauli) : Bool {
    mutable value = true;
    for (qubit in qubits) {
        if (Measure([pauli], [qubit]) == One) {
            set value = false;
        }
    }
    return value;
}
```

## <a name="borrowing-qubits-example"></a>Exemplo de qubits de empréstimo

Na Canon, há exemplos que usam a `borrowing` palavra-chave, por exemplo, a função `MultiControlledXBorrow` definida abaixo.
Se `controls` a denotar o qubits de controle que deve ser adicionado a uma `X` operação, um geral de `Length(controls)-2` muitos ancillas sujos será adicionado por essa implementação.

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

Observe que o uso extensivo do `With` combinador---em seu formato aplicável a operações que dão suporte a adjoint, ou seja, `WithA` ---foram feitas neste exemplo.
Esse é um bom estilo de programação, pois adicionar controle a estruturas que envolve `With` propaga controle somente para a operação interna.
Além disso, observe que, além do `body` da operação, uma implementação do `controlled` corpo da operação foi fornecida explicitamente, em vez de recorrer a uma `controlled auto` instrução.
O motivo disso é que sabemos da estrutura do circuito como adicionar com facilidade mais controles, o que é benéfico em comparação com a adição de controle a cada portão e a cada porta individual no `body` . 

É instrutivo comparar esse código com outra função Canon `MultiControlledXClean` que atinge o mesmo objetivo de implementar uma operação controlada por multiplicação `X` , no entanto, que usa várias qubits limpas usando o `using` mecanismo. 

## <a name="whats-next"></a>O que vem a seguir?
Saiba mais sobre o [fluxo de controle](xref:microsoft.quantum.guide.controlflow) em Q #.