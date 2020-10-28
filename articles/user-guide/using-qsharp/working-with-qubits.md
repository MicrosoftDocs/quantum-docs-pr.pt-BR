---
title: Trabalhar com qubits
description: Saiba mais sobre como trabalhar com o qubits em Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9a3d7e03016332a04ac9d1610428b6fcd546d1f6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691579"
---
# <a name="working-with-qubits"></a>Trabalhar com qubits

Qubits são o objeto fundamental das informações na computação Quantum. Para obter uma introdução geral ao qubits, consulte [noções básicas sobre computação Quantum](xref:microsoft.quantum.overview.understanding)e aprofundar-se em sua representação matemática, consulte [o qubit](xref:microsoft.quantum.concepts.qubit). 

Este artigo explora como usar e trabalhar com o qubits em um Q# programa. 

> [!IMPORTANT]
>Nenhuma das instruções discutidas neste artigo são válidas dentro do corpo de uma função. Eles só são válidos dentro de operações.

## <a name="allocating-qubits"></a>Alocando qubits

Como os qubits físicos são um recurso precioso em um computador Quantum, parte do trabalho do compilador é garantir que eles estejam sendo usados com a maior eficiência possível.
Como tal, você precisa dizer Q# para *alocar* qubits para uso em um bloco de instrução específico.
Você pode alocar qubits como um único qubit ou como uma matriz de qubits, conhecida como um *registro* . 

### <a name="clean-qubits"></a>Limpar qubits

Use a `using` instrução para alocar novo qubits para uso durante um bloco de instruções.

A instrução consiste na palavra-chave `using` , seguida por uma associação entre parênteses `( )` e o bloco de instrução dentro do qual os qubits estão disponíveis.
A associação segue o mesmo padrão que as `let` instruções: um único símbolo ou uma tupla de símbolos, seguido por um sinal de igual `=` , e um único valor ou uma tupla correspondente de *inicializadores* .

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

Qualquer qubits alocada dessa maneira começa no estado $ \ket {0} $. Portanto, no exemplo anterior, `auxiliary` é um único qubit no estado $ \ket {0} $ e `register` está no estado de cinco qubit $ \ket {00000} = \ket {0} \otimes \ket \otimes {0} \cdots \otimes \ket {0} $.
No final do `using` bloco, qualquer qubits alocada por esse bloco será imediatamente desalocada e não poderá mais ser usada.

> [!WARNING]
> Os computadores de destino podem reutilizar qubits desalocados e oferecê-los a outros `using` blocos para alocação. Como tal, a máquina de destino espera que qubits estejam no estado $ \ket {0} $ imediatamente antes da desalocação.
> Sempre que possível, use operações de unitário para retornar qualquer qubits alocado para $ \ket {0} $.
> Se necessário, você pode usar a @"microsoft.quantum.intrinsic.reset" operação, que retorna o qubit para $ \ket {0} $ medindo-o e executando condicionalmente uma operação com base no resultado. Essa medida destrói qualquer Entanglement com a qubits restante e, portanto, pode afetar a computação.


### <a name="borrowed-qubits"></a>Qubits emprestado

Use a `borrowing` instrução para alocar qubits para uso temporário, que não precisa estar em um estado específico.

Você pode usar qubits emprestados como espaço transitório durante uma computação.
Esses qubits geralmente não estão em um estado limpo, ou seja, eles não são necessariamente inicializados em um estado conhecido, como $ \ket {0} $.
Essas são muitas vezes chamadas de qubits "sujas" porque seu estado é desconhecido e pode até mesmo ser confusas com outras partes da memória do computador Quantum.

A associação segue o mesmo padrão e regras que a `using` instrução.
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
O tomador de confirmações para deixar o qubits no mesmo estado em que estavam emprestados; ou seja, seu estado no início e o final do bloco de instrução devem ser iguais.
Como esse estado não é necessariamente um estado clássico, na maioria dos casos, os escopos emprestados não devem conter medidas. 

Ao emprestar qubits, o sistema primeiro tenta preencher a solicitação de qubits que estão em uso, mas que não são acessadas durante o corpo da `borrowing` instrução.
Se não houver tal qubits suficiente, ele alocará novas qubits para concluir a solicitação.

Entre os casos de uso conhecidos de qubits sujos estão implementações de Gates de CNOT de vários controle que exigem apenas poucos qubits e implementação de incrementais.
Para obter um exemplo de uso no Q# , consulte [emprestando qubits exemplo](#borrowing-qubits-example) neste artigo ou a [*fatoração de papel usando 2n + 2 qubits com multiplicação modular baseada em Toffoli*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler e Svore 2017) para um algoritmo que utiliza qubits emprestados.

## <a name="intrinsic-operations"></a>Operações intrínsecas

Uma vez alocado, você pode passar um qubit para funções e operações.
De certa forma, isso é tudo o que um Q# programa pode fazer com um qubit, pois as ações que podem ser executadas são todas definidas como operações.

Este artigo discute algumas Q# operações úteis que você pode usar para interagir com o qubits.
Para obter mais detalhes sobre esses e outros, consulte [operações e funções intrínsecas](xref:microsoft.quantum.libraries.standard.prelude). 

Primeiro, os operadores de Pauli de qubit único $X $, $Y $ e $Z $ são representados Q# pelas operações intrínsecas [`X`](xref:Microsoft.Quantum.Intrinsic.X) , [`Y`](xref:Microsoft.Quantum.Intrinsic.Y) e [`Z`](xref:Microsoft.Quantum.Intrinsic.Z) , cada um deles tem um tipo `(Qubit => Unit is Adj + Ctl)` .

Conforme descrito em [operações e funções intrínsecas](xref:microsoft.quantum.libraries.standard.prelude), considere o $X $ e, portanto, `X` como uma operação de inversão de bits ou não de porta.
Você pode usar a `X` operação para preparar Estados do formulário $ \ket{s_0 s_1 \dots s_n} $ para uma cadeia de caracteres de bits clássica $s $:

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
        // Remember to reset the qubits before deallocation:
        ResetAll(register);
    }
}
```

> [!TIP]
> Posteriormente, você verá mais formas compactadas de gravar essa operação que não exigem o fluxo de controle manual.

Você também pode preparar Estados como $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ e $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ usando o Hadamard Transform $H $, que é representado Q# pela operação intrínseca [`H`](xref:Microsoft.Quantum.Intrinsic.H) (também do tipo (qubit = unidade de> é adj + CTL) '):

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString in the earlier example.
    PrepareBitString(bitstring, register);
    // Next, use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the desired state.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a>Medidas

As medidas de qubits individuais podem ser executadas em diferentes bases, cada uma representada por um eixo Pauli na [esfera Bloch](xref:microsoft.quantum.glossary#bloch-sphere).
A *base computacional* refere-se à `PauliZ` base e é a base mais comum usada para medição.

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a>Meça um único qubit na `PauliZ` base

Use a [`M`](xref:Microsoft.Quantum.Intrinsic.M) operação, que é uma operação não-unitário intrínseca interna, para medir um único qubit `PauliZ` com base e atribuir um valor clássico ao resultado.
`M` tem um tipo de retorno reservado, `Result` , que só pode ter valores `Zero` ou `One` correspondentes aos Estados medidos $ \ket {0} $ ou $ \ket {1} $-indicando que o resultado não é mais um estado Quantum.

Um exemplo simples é a operação a seguir, que aloca um qubit no estado $ \ket {0} $ e, em seguida, aplica uma operação Hadamard `H` a ele e mede o resultado na `PauliZ` base.

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // Apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, return the result of the measurement.
        return result;
    }
}
```

### <a name="measure-one-or-more-qubits-in-specific-bases"></a>Medir um ou mais qubits em bases específicas

Para medir uma matriz de um ou mais qubits em bases específicas, você pode usar a [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) operação.

As entradas para `Measure` são uma matriz de `Pauli` tipos (por exemplo, `[PauliX, PauliZ, PauliZ]` ) e uma matriz de qubits.

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

Observe que esse exemplo ainda só `Measure` é executado em qubits individuais, um de cada vez, mas a operação pode ser estendida para medidas conjuntas em vários qubits.

## <a name="borrowing-qubits-example"></a>Exemplo de qubits de empréstimo

Há exemplos na Canon que usam a `borrowing` palavra-chave, como a função a seguir `MultiControlledXBorrow` . Se `controls` o denotar o qubits de controle a ser adicionado a uma `X` operação, o número de [ancillas](xref:microsoft.quantum.glossary#ancilla) sujas adicionado por essa implementação será `Length(controls)-2` .

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

Observe que este exemplo usou o uso extensivo do `With` combinador, em seu formato aplicável para operações que dão suporte a adjoint, por exemplo, `WithA` .
Esse é um bom estilo de programação, pois adicionar controle a estruturas que envolve `With` propaga controle somente para a operação interna.
Observe também que, além do `body` da operação, uma implementação do `controlled` corpo da operação foi fornecida explicitamente, em vez de recorrer a uma `controlled auto` instrução.
O motivo disso é que, devido à estrutura do circuito, é fácil adicionar mais controles, o que é benéfico em comparação à adição de controle a cada portão no `body` . 

É instrutivo comparar esse código com outra função Canon `MultiControlledXClean` que atinge o mesmo objetivo de implementar uma operação controlada por multiplicação `X` , no entanto, que usa várias qubits limpas usando o `using` mecanismo. 

## <a name="next-steps"></a>Próximas etapas

Saiba mais sobre o [fluxo de controle](xref:microsoft.quantum.guide.controlflow) no Q# .