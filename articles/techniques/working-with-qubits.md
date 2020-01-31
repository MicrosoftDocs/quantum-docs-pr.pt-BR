---
title: Trabalhando com qubits
description: 'Trabalhando com técnicas qubits-Q #'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: dc6db93dadc37534aece9624fe516125d919f8cd
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819987"
---
# <a name="working-with-qubits"></a><span data-ttu-id="8fd52-103">Trabalhando com qubits</span><span class="sxs-lookup"><span data-stu-id="8fd52-103">Working with Qubits</span></span>

<span data-ttu-id="8fd52-104">Agora que já vi uma variedade de diferentes partes da linguagem Q #, vamos nos aprofundar em tudo e ver como usar o qubits em si.</span><span class="sxs-lookup"><span data-stu-id="8fd52-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="8fd52-105">Alocando qubits</span><span class="sxs-lookup"><span data-stu-id="8fd52-105">Allocating Qubits</span></span>

<span data-ttu-id="8fd52-106">Primeiro, para obter um qubit que possamos usar em Q #, *alocamos* qubits em um bloco de `using`:</span><span class="sxs-lookup"><span data-stu-id="8fd52-106">First, to obtain a qubit that we can use in Q#, we *allocate* qubits within a `using` block:</span></span>

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

<span data-ttu-id="8fd52-107">Qualquer qubits alocado dessa maneira começa no $ \ket{0}$ State; no exemplo acima, `register` é, portanto, no estado $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="8fd52-107">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="8fd52-108">No final do bloco de `using`, qualquer qubits alocada por esse bloco será imediatamente desalocada e não poderá mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="8fd52-108">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="8fd52-109">Os computadores de destino esperam que qubits estejam no $ \ket{0}$ State imediatamente antes da desalocação, para que possam ser reutilizados e oferecidos a outros blocos de `using` para alocação.</span><span class="sxs-lookup"><span data-stu-id="8fd52-109">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="8fd52-110">Sempre que possível, use operações de unitário para retornar qualquer qubits alocado para $ \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="8fd52-110">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="8fd52-111">Se necessário, a operação de @"microsoft.quantum.intrinsic.reset" pode ser usada para medir um qubit em vez disso e usar esse resultado de medida para garantir que o qubit medido seja retornado para $ \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="8fd52-111">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="8fd52-112">Essa medida destruirá qualquer Entanglement com a qubits restante e, portanto, poderá afetar a computação.</span><span class="sxs-lookup"><span data-stu-id="8fd52-112">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="8fd52-113">Operações intrínsecas</span><span class="sxs-lookup"><span data-stu-id="8fd52-113">Intrinsic Operations</span></span>

<span data-ttu-id="8fd52-114">Uma vez alocada, um qubit pode ser passado para funções e operações.</span><span class="sxs-lookup"><span data-stu-id="8fd52-114">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="8fd52-115">De certa forma, isso é tudo o que um programa Q # pode fazer com um qubit, pois as ações que podem ser executadas são todas definidas como operações.</span><span class="sxs-lookup"><span data-stu-id="8fd52-115">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="8fd52-116">Veremos essas operações com mais detalhes em [operações intrínsecas e funções](xref:microsoft.quantum.libraries.standard.prelude), mas, por enquanto, mencionamos algumas operações úteis que podem ser usadas para interagir com o qubits.</span><span class="sxs-lookup"><span data-stu-id="8fd52-116">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="8fd52-117">Primeiro, os operadores de Pauli qubit $X $, $Y $ e $Z $ são representados em Q # pelas operações intrínsecas `X`, `Y`e `Z`, cada uma delas com o tipo `(Qubit => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="8fd52-117">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="8fd52-118">Conforme descrito em [operações e funções intrínsecas](xref:microsoft.quantum.libraries.standard.prelude), podemos considerar $X $ e, portanto, `X` como uma operação de inversão de bits ou não de porta.</span><span class="sxs-lookup"><span data-stu-id="8fd52-118">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="8fd52-119">A operação `X` nos permite preparar Estados do formulário $ \ket{s_0 s_1 \dots s_n} $ para uma cadeia de caracteres de bits clássica $s $:</span><span class="sxs-lookup"><span data-stu-id="8fd52-119">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
> <span data-ttu-id="8fd52-120">Mais tarde, veremos mais formas compactadas de gravar essa operação que não exigem controle de fluxo manual.</span><span class="sxs-lookup"><span data-stu-id="8fd52-120">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="8fd52-121">Também podemos preparar Estados como $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ e $ \ket{-} = \left (\ket{0}-\ket{1}\right)/\sqrt{2}$ usando a transformação Hadamard $H $, que é representada em Q # pela operação intrínseca `H : (Qubit => Unit is Adj + Ctl)`:</span><span class="sxs-lookup"><span data-stu-id="8fd52-121">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="8fd52-122">Medidas</span><span class="sxs-lookup"><span data-stu-id="8fd52-122">Measurements</span></span>

<span data-ttu-id="8fd52-123">Usando a operação `Measure`, que é uma operação não-unitário intrínseca interna, podemos extrair informações clássicas de um objeto do tipo `Qubit` e atribuir um valor clássico como resultado, que tem um tipo reservado `Result`, indicando que o resultado não é mais um estado Quantum.</span><span class="sxs-lookup"><span data-stu-id="8fd52-123">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="8fd52-124">A entrada para `Measure` é um eixo Pauli na esfera Bloch, representado por um valor do tipo `Pauli` (por instância `PauliX`) e um valor do tipo `Qubit`.</span><span class="sxs-lookup"><span data-stu-id="8fd52-124">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="8fd52-125">Um exemplo simples é a operação a seguir, que aloca um qubit no estado $ \ket{0}$ e, em seguida, aplica uma operação Hadamard `H` a ele e mede o resultado na base `PauliZ`.</span><span class="sxs-lookup"><span data-stu-id="8fd52-125">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

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

<span data-ttu-id="8fd52-126">Um exemplo um pouco mais complicado é fornecido pela seguinte operação, que retorna o valor booliano `true` se todos os qubits em um registro do tipo `Qubit[]` estiverem no estado zero quando medido em uma base de Pauli especificada e que retorna `false` caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8fd52-126">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

<span data-ttu-id="8fd52-127">A linguagem Q # permite que o fluxo de controle clássico dependa dos resultados da medição de qubits.</span><span class="sxs-lookup"><span data-stu-id="8fd52-127">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="8fd52-128">Esse recurso, por sua vez, habilita a implementação de gadgets probabilística poderosos que podem reduzir o custo computacional para a implementação de unidades.</span><span class="sxs-lookup"><span data-stu-id="8fd52-128">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="8fd52-129">Por exemplo, é fácil implementar os chamados padrões de " *repetir até o êxito* " (RUS) em Q #.</span><span class="sxs-lookup"><span data-stu-id="8fd52-129">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="8fd52-130">Esses padrões de RUS são programas probabilística que têm um baixo custo *esperado* em termos de Gates elementares, mas para os quais o custo real depende de uma execução e de uma intercalação real de várias ramificações possíveis.</span><span class="sxs-lookup"><span data-stu-id="8fd52-130">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="8fd52-131">Para facilitar os padrões do RUS (repetição até o êxito), o Q # dá suporte à construção</span><span class="sxs-lookup"><span data-stu-id="8fd52-131">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the construct</span></span>

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

<span data-ttu-id="8fd52-132">onde `statementBlock1` e `statementBlock2` são zero ou mais instruções Q # e `expression` qualquer expressão válida que seja avaliada como um valor do tipo `Bool`.</span><span class="sxs-lookup"><span data-stu-id="8fd52-132">where `statementBlock1` and `statementBlock2` are zero or more Q# statements, and `expression` any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="8fd52-133">Em um caso de uso típico, a seguinte operação Q # implementa uma rotação em um eixo irracional de $ (I + 2i Z)/\sqrt{5}$ na esfera de Bloch.</span><span class="sxs-lookup"><span data-stu-id="8fd52-133">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="8fd52-134">Isso é feito usando um padrão de RUS conhecido:</span><span class="sxs-lookup"><span data-stu-id="8fd52-134">This is accomplished by using a known RUS pattern:</span></span>

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

<span data-ttu-id="8fd52-135">Este exemplo mostra o uso de uma variável mutável `finished` que está no escopo de todo o loop Repeat-Until-recorretion e que é inicializado antes do loop e atualizado na etapa de correção.</span><span class="sxs-lookup"><span data-stu-id="8fd52-135">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

<span data-ttu-id="8fd52-136">Por fim, mostramos um exemplo de um padrão RUS para preparar um estado Quantum $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $, começando com o estado $ \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="8fd52-136">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="8fd52-137">Consulte também o [exemplo de teste de unidade fornecido com a biblioteca padrão](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="8fd52-137">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

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

<span data-ttu-id="8fd52-138">Os recursos programáticos notáveis mostrados nesta operação são uma parte `fixup` mais complexa do loop, que envolve operações de Quantum e o uso de instruções `AssertProb` para avaliar a probabilidade de medir o estado Quantum em determinados pontos especificados no programa.</span><span class="sxs-lookup"><span data-stu-id="8fd52-138">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="8fd52-139">Consulte também [testando e Depurando](xref:microsoft.quantum.techniques.testing-and-debugging) para obter mais informações sobre as operações de [`Assert`](xref:microsoft.quantum.intrinsic.assert) e [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) .</span><span class="sxs-lookup"><span data-stu-id="8fd52-139">See also [Testing and debugging](xref:microsoft.quantum.techniques.testing-and-debugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>
