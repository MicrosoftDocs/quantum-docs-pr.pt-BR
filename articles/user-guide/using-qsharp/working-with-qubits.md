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
# <a name="working-with-qubits"></a><span data-ttu-id="58ac2-103">Trabalhar com qubits</span><span class="sxs-lookup"><span data-stu-id="58ac2-103">Working with qubits</span></span>

<span data-ttu-id="58ac2-104">Agora que já vi uma variedade de diferentes partes da linguagem Q #, vamos nos aprofundar em tudo e ver como usar o qubits em si.</span><span class="sxs-lookup"><span data-stu-id="58ac2-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

<span data-ttu-id="58ac2-105">Observe que nenhuma dessas instruções é permitida dentro do corpo de uma função.</span><span class="sxs-lookup"><span data-stu-id="58ac2-105">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="58ac2-106">Eles só são válidos dentro de operações.</span><span class="sxs-lookup"><span data-stu-id="58ac2-106">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="58ac2-107">Alocando qubits</span><span class="sxs-lookup"><span data-stu-id="58ac2-107">Allocating Qubits</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="58ac2-108">Limpar qubits</span><span class="sxs-lookup"><span data-stu-id="58ac2-108">Clean qubits</span></span>

<span data-ttu-id="58ac2-109">A `using` instrução é usada para *alocar* novo qubits para uso durante um bloco de instruções.</span><span class="sxs-lookup"><span data-stu-id="58ac2-109">The `using` statement is used to *allocate* new qubits for use during a statement block.</span></span>

<span data-ttu-id="58ac2-110">A instrução consiste na palavra-chave `using` , seguida por um parêntese de abertura `(` , uma associação, um parêntese de fechamento `)` e o bloco de instrução dentro do qual o qubits estará disponível.</span><span class="sxs-lookup"><span data-stu-id="58ac2-110">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="58ac2-111">A associação segue o mesmo padrão que as `let` instruções: um único símbolo ou uma tupla de símbolos, seguido por um sinal de igual `=` , e um único valor ou uma tupla correspondente de *inicializadores*.</span><span class="sxs-lookup"><span data-stu-id="58ac2-111">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers*.</span></span>

<span data-ttu-id="58ac2-112">Inicializadores estão disponíveis para um único qubit, indicado como `Qubit()` , ou uma matriz de qubits, `Qubit[n]` , em que `n` é uma `Int` expressão.</span><span class="sxs-lookup"><span data-stu-id="58ac2-112">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="58ac2-113">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="58ac2-113">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="58ac2-114">Qualquer qubits alocada dessa maneira começa no estado $ \ket {0} $; no exemplo acima, `register` é, portanto, no estado $ \ket {00000} = \ket {0} \otimes \ket \otimes \cdots {0} \otimes \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="58ac2-114">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="58ac2-115">No final do `using` bloco, qualquer qubits alocada por esse bloco será imediatamente desalocada e não poderá mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="58ac2-115">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="58ac2-116">As máquinas de destino esperam que qubits estejam no estado $ \ket {0} $ imediatamente antes da desalocação, para que possam ser reutilizadas e oferecidas a outros `using` blocos para alocação.</span><span class="sxs-lookup"><span data-stu-id="58ac2-116">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="58ac2-117">Sempre que possível, use operações de unitário para retornar qualquer qubits alocado para $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="58ac2-117">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="58ac2-118">Se necessário, a @"microsoft.quantum.intrinsic.reset" operação pode ser usada para medir um qubit em vez disso e usar esse resultado de medida para garantir que o qubit medido seja retornado para $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="58ac2-118">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="58ac2-119">Essa medida destruirá qualquer Entanglement com a qubits restante e, portanto, poderá afetar a computação.</span><span class="sxs-lookup"><span data-stu-id="58ac2-119">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="58ac2-120">Qubits emprestado</span><span class="sxs-lookup"><span data-stu-id="58ac2-120">Borrowed Qubits</span></span>

<span data-ttu-id="58ac2-121">A `borrowing` instrução é usada para tornar o qubits disponível para uso temporário, que não precisa estar em um estado específico.</span><span class="sxs-lookup"><span data-stu-id="58ac2-121">The `borrowing` statement is used to make qubits available for temporary use, which do not need be in a specific state.</span></span>

<span data-ttu-id="58ac2-122">O mecanismo de empréstimo permite a alocação de qubits que pode ser usada como espaço transitório durante uma computação.</span><span class="sxs-lookup"><span data-stu-id="58ac2-122">The borrowing mechanism allows the allocation of qubits that can be used as scratch space during a computation.</span></span>
<span data-ttu-id="58ac2-123">Esses qubits geralmente não estão em um estado limpo, ou seja, eles não são necessariamente inicializados em um estado conhecido, como $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="58ac2-123">These qubits are generally not in a clean state, i.e., they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="58ac2-124">Essas são muitas vezes chamadas de qubits "sujas" porque seu estado é desconhecido e pode até mesmo ser confusas com outras partes da memória do computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="58ac2-124">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="58ac2-125">A associação segue o mesmo padrão e regras que uma em uma `using` instrução.</span><span class="sxs-lookup"><span data-stu-id="58ac2-125">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>
<span data-ttu-id="58ac2-126">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="58ac2-126">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="58ac2-127">O qubits emprestado está em um estado desconhecido e sai do escopo no final do bloco de instrução.</span><span class="sxs-lookup"><span data-stu-id="58ac2-127">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="58ac2-128">O tomador de confirmações para deixar o qubits no mesmo estado em que estavam emprestados, ou seja, seu estado no início e no final do bloco de instrução deve ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="58ac2-128">The borrower commits to leaving the qubits in the same state they were in when they were borrowed,  i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="58ac2-129">Esse estado em particular não é necessariamente um estado clássico, de modo que, na maioria dos casos, os escopos emprestados não devem conter medidas.</span><span class="sxs-lookup"><span data-stu-id="58ac2-129">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="58ac2-130">Ao emprestar qubits, o sistema primeiro tentará preencher a solicitação de qubits que estão em uso, mas que não são acessadas durante o corpo da `borrowing` instrução.</span><span class="sxs-lookup"><span data-stu-id="58ac2-130">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="58ac2-131">Se não houver tal qubits suficiente, ele alocará o novo qubits para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="58ac2-131">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>


<span data-ttu-id="58ac2-132">Entre os casos de uso conhecidos de qubits sujos estão implementações de Gates de CNOT de vários controle que exigem apenas poucos qubits e implementação de incrementais.</span><span class="sxs-lookup"><span data-stu-id="58ac2-132">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="58ac2-133">Consulte o [exemplo de empréstimo de qubits](#borrowing-qubits-example) abaixo para ver um exemplo de seu uso em Q # ou a [*fatoração de papel usando 2n + 2 qubits com multiplicação modular baseada em Toffoli*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler e Svore 2017) para um algoritmo que utiliza qubits emprestados.</span><span class="sxs-lookup"><span data-stu-id="58ac2-133">See the [Borrowing Qubits Example](#borrowing-qubits-example) below to see an example of their use in Q#, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>


## <a name="intrinsic-operations"></a><span data-ttu-id="58ac2-134">Operações intrínsecas</span><span class="sxs-lookup"><span data-stu-id="58ac2-134">Intrinsic Operations</span></span>

<span data-ttu-id="58ac2-135">Uma vez alocada, um qubit pode ser passado para funções e operações.</span><span class="sxs-lookup"><span data-stu-id="58ac2-135">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="58ac2-136">De certa forma, isso é tudo o que um programa Q # pode fazer com um qubit, pois as ações que podem ser executadas são todas definidas como operações.</span><span class="sxs-lookup"><span data-stu-id="58ac2-136">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="58ac2-137">Veremos essas operações com mais detalhes em [operações intrínsecas e funções](xref:microsoft.quantum.libraries.standard.prelude), mas, por enquanto, mencionamos algumas operações úteis que podem ser usadas para interagir com o qubits.</span><span class="sxs-lookup"><span data-stu-id="58ac2-137">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="58ac2-138">Primeiro, os operadores de Pauli de qubit único $X $, $Y $ e $Z $ são representados em Q # pelas operações intrínsecas `X` , `Y` e `Z` cada um deles tem um tipo `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="58ac2-138">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="58ac2-139">Conforme descrito em [operações intrínsecas e funções](xref:microsoft.quantum.libraries.standard.prelude), podemos imaginar $X $ e, portanto, `X` como uma operação de inversão de bits ou não de portão.</span><span class="sxs-lookup"><span data-stu-id="58ac2-139">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="58ac2-140">A `X` operação nos permite preparar Estados do formulário $ \ket{s_0 s_1 \dots s_n} $ para uma cadeia de caracteres de bits clássica $s $:</span><span class="sxs-lookup"><span data-stu-id="58ac2-140">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
> <span data-ttu-id="58ac2-141">Mais tarde, veremos mais formas compactadas de gravar essa operação que não exigem controle de fluxo manual.</span><span class="sxs-lookup"><span data-stu-id="58ac2-141">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="58ac2-142">Também podemos preparar Estados como $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ e $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ usando o Hadamard Transform $H $, que é representado em Q # pela operação intrínseca `H : (Qubit => Unit is Adj + Ctl)` :</span><span class="sxs-lookup"><span data-stu-id="58ac2-142">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="58ac2-143">Medidas</span><span class="sxs-lookup"><span data-stu-id="58ac2-143">Measurements</span></span>

<span data-ttu-id="58ac2-144">Usando a `Measure` operação, que é uma operação não-unitário intrínseca interna, podemos extrair informações clássicas de um objeto do tipo `Qubit` e atribuir um valor clássico como resultado, que tem um tipo reservado `Result` , indicando que o resultado não é mais um estado Quantum.</span><span class="sxs-lookup"><span data-stu-id="58ac2-144">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="58ac2-145">A entrada para `Measure` é um eixo Pauli na esfera Bloch, representado por um valor do tipo `Pauli` (por exemplo `PauliX` ) e um valor do tipo `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="58ac2-145">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="58ac2-146">Um exemplo simples é a operação a seguir, que aloca um qubit no estado $ \ket {0} $ e, em seguida, aplica uma operação Hadamard `H` a ele e mede o resultado na `PauliZ` base.</span><span class="sxs-lookup"><span data-stu-id="58ac2-146">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

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

<span data-ttu-id="58ac2-147">Um exemplo um pouco mais complicado é dado pela seguinte operação, que retorna o valor booliano `true` se todos os qubits em um registro do tipo `Qubit[]` estiverem no estado zero quando medido em uma base de Pauli especificada e que retorna de `false` outra forma.</span><span class="sxs-lookup"><span data-stu-id="58ac2-147">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

## <a name="borrowing-qubits-example"></a><span data-ttu-id="58ac2-148">Exemplo de qubits de empréstimo</span><span class="sxs-lookup"><span data-stu-id="58ac2-148">Borrowing Qubits Example</span></span>

<span data-ttu-id="58ac2-149">Na Canon, há exemplos que usam a `borrowing` palavra-chave, por exemplo, a função `MultiControlledXBorrow` definida abaixo.</span><span class="sxs-lookup"><span data-stu-id="58ac2-149">In the canon there are examples that use the `borrowing` keyword, for instance the function `MultiControlledXBorrow` defined below.</span></span>
<span data-ttu-id="58ac2-150">Se `controls` a denotar o qubits de controle que deve ser adicionado a uma `X` operação, um geral de `Length(controls)-2` muitos ancillas sujos será adicionado por essa implementação.</span><span class="sxs-lookup"><span data-stu-id="58ac2-150">If `controls` denotes the control qubits that should be added to an `X` operation, then an overall of `Length(controls)-2` many dirty ancillas will be added by this implementation.</span></span>

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

<span data-ttu-id="58ac2-151">Observe que o uso extensivo do `With` combinador---em seu formato aplicável a operações que dão suporte a adjoint, ou seja, `WithA` ---foram feitas neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="58ac2-151">Note that extensive use of the `With` combinator---in its form that is applicable for operations that support adjoint, i.e., `WithA`---was made in this example.</span></span>
<span data-ttu-id="58ac2-152">Esse é um bom estilo de programação, pois adicionar controle a estruturas que envolve `With` propaga controle somente para a operação interna.</span><span class="sxs-lookup"><span data-stu-id="58ac2-152">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="58ac2-153">Além disso, observe que, além do `body` da operação, uma implementação do `controlled` corpo da operação foi fornecida explicitamente, em vez de recorrer a uma `controlled auto` instrução.</span><span class="sxs-lookup"><span data-stu-id="58ac2-153">Further, note that here in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="58ac2-154">O motivo disso é que sabemos da estrutura do circuito como adicionar com facilidade mais controles, o que é benéfico em comparação com a adição de controle a cada portão e a cada porta individual no `body` .</span><span class="sxs-lookup"><span data-stu-id="58ac2-154">The reason for this is that we know from the structure of the circuit how to easily add further controls which is beneficial compared to adding control to each and every individual gate in the `body`.</span></span> 

<span data-ttu-id="58ac2-155">É instrutivo comparar esse código com outra função Canon `MultiControlledXClean` que atinge o mesmo objetivo de implementar uma operação controlada por multiplicação `X` , no entanto, que usa várias qubits limpas usando o `using` mecanismo.</span><span class="sxs-lookup"><span data-stu-id="58ac2-155">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="whats-next"></a><span data-ttu-id="58ac2-156">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="58ac2-156">What's Next?</span></span>
<span data-ttu-id="58ac2-157">Saiba mais sobre o [fluxo de controle](xref:microsoft.quantum.guide.controlflow) em Q #.</span><span class="sxs-lookup"><span data-stu-id="58ac2-157">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>