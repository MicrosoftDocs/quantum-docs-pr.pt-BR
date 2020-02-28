---
title: Trabalhando com qubits
description: Saiba como alocar qubits, usá-los em operações e funções e medir os resultados.
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: 1aa2432996dda61d099e3b5bb4db78379ce43d97
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907640"
---
# <a name="working-with-qubits"></a>Trabalhando com qubits

Agora que já vi uma variedade de diferentes partes da linguagem Q #, vamos nos aprofundar em tudo e ver como usar o qubits em si.

## <a name="allocating-qubits"></a>Alocando qubits

Primeiro, para obter um qubit que possamos usar em Q #, *alocamos* qubits em um bloco de `using`:

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

Qualquer qubits alocado dessa maneira começa no $ \ket{0}$ State; no exemplo acima, `register` é, portanto, no estado $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.
No final do bloco de `using`, qualquer qubits alocada por esse bloco será imediatamente desalocada e não poderá mais ser usada.

> [!WARNING]
> Os computadores de destino esperam que qubits estejam no $ \ket{0}$ State imediatamente antes da desalocação, para que possam ser reutilizados e oferecidos a outros blocos de `using` para alocação.
> Sempre que possível, use operações de unitário para retornar qualquer qubits alocado para $ \ket{0}$.
> Se necessário, a operação de @"microsoft.quantum.intrinsic.reset" pode ser usada para medir um qubit em vez disso e usar esse resultado de medida para garantir que o qubit medido seja retornado para $ \ket{0}$. Essa medida destruirá qualquer Entanglement com a qubits restante e, portanto, poderá afetar a computação.

## <a name="intrinsic-operations"></a>Operações intrínsecas

Uma vez alocada, um qubit pode ser passado para funções e operações.
De certa forma, isso é tudo o que um programa Q # pode fazer com um qubit, pois as ações que podem ser executadas são todas definidas como operações.
Veremos essas operações com mais detalhes em [operações intrínsecas e funções](xref:microsoft.quantum.libraries.standard.prelude), mas, por enquanto, mencionamos algumas operações úteis que podem ser usadas para interagir com o qubits.

Primeiro, os operadores de Pauli qubit $X $, $Y $ e $Z $ são representados em Q # pelas operações intrínsecas `X`, `Y`e `Z`, cada uma delas com o tipo `(Qubit => Unit is Adj + Ctl)`.
Conforme descrito em [operações e funções intrínsecas](xref:microsoft.quantum.libraries.standard.prelude), podemos considerar $X $ e, portanto, `X` como uma operação de inversão de bits ou não de porta.
A operação `X` nos permite preparar Estados do formulário $ \ket{s_0 s_1 \dots s_n} $ para uma cadeia de caracteres de bits clássica $s $:

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

Também podemos preparar Estados como $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ e $ \ket{-} = \left (\ket{0}-\ket{1}\right)/\sqrt{2}$ usando a transformação Hadamard $H $, que é representada em Q # pela operação intrínseca `H : (Qubit => Unit is Adj + Ctl)`:

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

Usando a operação `Measure`, que é uma operação não-unitário intrínseca interna, podemos extrair informações clássicas de um objeto do tipo `Qubit` e atribuir um valor clássico como resultado, que tem um tipo reservado `Result`, indicando que o resultado não é mais um estado Quantum.
A entrada para `Measure` é um eixo Pauli na esfera Bloch, representado por um valor do tipo `Pauli` (por instância `PauliX`) e um valor do tipo `Qubit`.

Um exemplo simples é a operação a seguir, que aloca um qubit no estado $ \ket{0}$ e, em seguida, aplica uma operação Hadamard `H` a ele e mede o resultado na base `PauliZ`.

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

Um exemplo um pouco mais complicado é fornecido pela seguinte operação, que retorna o valor booliano `true` se todos os qubits em um registro do tipo `Qubit[]` estiverem no estado zero quando medido em uma base de Pauli especificada e que retorna `false` caso contrário.

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

A linguagem Q # permite que o fluxo de controle clássico dependa dos resultados da medição de qubits.
Esse recurso, por sua vez, habilita a implementação de gadgets probabilística poderosos que podem reduzir o custo computacional para a implementação de unidades.
Por exemplo, é fácil implementar os chamados padrões de " *repetir até o êxito* " (RUS) em Q #.
Esses padrões de RUS são programas probabilística que têm um baixo custo *esperado* em termos de Gates elementares, mas para os quais o custo real depende de uma execução e de uma intercalação real de várias ramificações possíveis.

Para facilitar os padrões do RUS (repetição até o êxito), o Q # dá suporte à construção

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

onde `statementBlock1` e `statementBlock2` são zero ou mais instruções Q # e `expression` qualquer expressão válida que seja avaliada como um valor do tipo `Bool`.
Em um caso de uso típico, a seguinte operação Q # implementa uma rotação em um eixo irracional de $ (I + 2i Z)/\sqrt{5}$ na esfera de Bloch. Isso é feito usando um padrão de RUS conhecido:

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

Este exemplo mostra o uso de uma variável mutável `finished` que está no escopo de todo o loop Repeat-Until-recorretion e que é inicializado antes do loop e atualizado na etapa de correção.

Por fim, mostramos um exemplo de um padrão RUS para preparar um estado Quantum $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $, começando com o estado $ \ket{+} $.
Consulte também o [exemplo de teste de unidade fornecido com a biblioteca padrão](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+⟩ state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+⟩ state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+⟩ state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+⟩ in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+⟩ state.
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

Os recursos programáticos notáveis mostrados nesta operação são uma parte `fixup` mais complexa do loop, que envolve operações de Quantum e o uso de instruções `AssertProb` para avaliar a probabilidade de medir o estado Quantum em determinados pontos especificados no programa.
Consulte também [testando e Depurando](xref:microsoft.quantum.techniques.testing-and-debugging) para obter mais informações sobre as operações de [`Assert`](xref:microsoft.quantum.intrinsic.assert) e [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) .
