---
title: Trabalhar com qubits
description: Descrição do preenchimento
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: 1655d18ab9d8638ad356e6fb90994b5c1fd76a25
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885308"
---
# <a name="working-with-qubits"></a><span data-ttu-id="0436e-103">Trabalhar com qubits</span><span class="sxs-lookup"><span data-stu-id="0436e-103">Working with qubits</span></span>

<span data-ttu-id="0436e-104">Qubits são o objeto fundamental das informações na computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="0436e-104">Qubits are the fundamental object of information in quantum computing.</span></span> <span data-ttu-id="0436e-105">Para obter uma introdução geral ao qubits, consulte [noções básicas sobre computação Quantum](xref:microsoft.quantum.overview.understanding)e aprofundar-se em sua representação matemática, consulte [o qubit](xref:microsoft.quantum.concepts.qubit).</span><span class="sxs-lookup"><span data-stu-id="0436e-105">For a general introduction to qubits, see [Understanding quantum computing](xref:microsoft.quantum.overview.understanding), and to dive deeper into their mathematical representation, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span> 

<span data-ttu-id="0436e-106">Este artigo explora como usar e trabalhar com o qubits em um programa Q #.</span><span class="sxs-lookup"><span data-stu-id="0436e-106">This article explores how to use and work with qubits in a Q# program.</span></span> 

> [!IMPORTANT]
><span data-ttu-id="0436e-107">Nenhuma das instruções discutidas neste artigo são válidas dentro do corpo de uma função.</span><span class="sxs-lookup"><span data-stu-id="0436e-107">None of the statements discussed in this article are valid within the body of a function.</span></span> <span data-ttu-id="0436e-108">Eles só são válidos dentro de operações.</span><span class="sxs-lookup"><span data-stu-id="0436e-108">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="0436e-109">Alocando qubits</span><span class="sxs-lookup"><span data-stu-id="0436e-109">Allocating Qubits</span></span>

<span data-ttu-id="0436e-110">Como os qubits físicos são um recurso precioso em um computador Quantum, parte do trabalho do compilador é garantir que eles estejam sendo usados com a maior eficiência possível.</span><span class="sxs-lookup"><span data-stu-id="0436e-110">Because physical qubits are a precious resource in a quantum computer, part of the compiler's job is to make sure they are being used as efficiently as possible.</span></span>
<span data-ttu-id="0436e-111">Como tal, você precisa informar Q # para *alocar* qubits para uso em um bloco de instrução específico.</span><span class="sxs-lookup"><span data-stu-id="0436e-111">As such, you need to tell Q# to *allocate* qubits for use within a particular statement block.</span></span>
<span data-ttu-id="0436e-112">Você pode alocar qubits como um único qubit ou como uma matriz de qubits, conhecida como um *registro*.</span><span class="sxs-lookup"><span data-stu-id="0436e-112">You can allocate qubits as a single qubit, or as an array of qubits, known as a *register*.</span></span> 

### <a name="clean-qubits"></a><span data-ttu-id="0436e-113">Limpar qubits</span><span class="sxs-lookup"><span data-stu-id="0436e-113">Clean qubits</span></span>

<span data-ttu-id="0436e-114">Use a `using` instrução para alocar novo qubits para uso durante um bloco de instruções.</span><span class="sxs-lookup"><span data-stu-id="0436e-114">Use the `using` statement to allocate new qubits for use during a statement block.</span></span>

<span data-ttu-id="0436e-115">A instrução consiste na palavra-chave `using` , seguida por uma associação entre parênteses `( )` e o bloco de instrução dentro do qual os qubits estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0436e-115">The statement consists of the keyword `using`, followed by a binding enclosed in parentheses `( )` and the statement block within which the qubits are available.</span></span>
<span data-ttu-id="0436e-116">A associação segue o mesmo padrão que as `let` instruções: um único símbolo ou uma tupla de símbolos, seguido por um sinal de igual `=` , e um único valor ou uma tupla correspondente de *inicializadores*.</span><span class="sxs-lookup"><span data-stu-id="0436e-116">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers*.</span></span>

<span data-ttu-id="0436e-117">Inicializadores estão disponíveis para um único qubit, indicado como `Qubit()` , ou uma matriz de qubits, `Qubit[n]` , em que `n` é uma `Int` expressão.</span><span class="sxs-lookup"><span data-stu-id="0436e-117">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="0436e-118">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="0436e-118">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="0436e-119">Qualquer qubits alocada dessa maneira começa no estado $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="0436e-119">Any qubits allocated in this way start off in the $\ket{0}$ state.</span></span> <span data-ttu-id="0436e-120">Portanto, no exemplo anterior, `auxiliary` é um único qubit no estado $ \ket {0} $ e `register` está no estado de cinco qubit $ \ket {00000} = \ket {0} \otimes \ket \otimes {0} \cdots \otimes \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="0436e-120">Thus in the previous example, `auxiliary` is a single qubit in the state $\ket{0}$, and `register` is in the five-qubit state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="0436e-121">No final do `using` bloco, qualquer qubits alocada por esse bloco será imediatamente desalocada e não poderá mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="0436e-121">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="0436e-122">Os computadores de destino podem reutilizar qubits desalocados e oferecê-los a outros `using` blocos para alocação.</span><span class="sxs-lookup"><span data-stu-id="0436e-122">Target machines can reuse deallocated qubits and offer them to other `using` blocks for allocation.</span></span> <span data-ttu-id="0436e-123">Como tal, a máquina de destino espera que qubits estejam no estado $ \ket {0} $ imediatamente antes da desalocação.</span><span class="sxs-lookup"><span data-stu-id="0436e-123">As such, the target machine expects that qubits are in the $\ket{0}$ state immediately before deallocation.</span></span>
> <span data-ttu-id="0436e-124">Sempre que possível, use operações de unitário para retornar qualquer qubits alocado para $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="0436e-124">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="0436e-125">Se necessário, você pode usar a @"microsoft.quantum.intrinsic.reset" operação, que retorna o qubit para $ \ket {0} $ medindo-o e executando condicionalmente uma operação com base no resultado.</span><span class="sxs-lookup"><span data-stu-id="0436e-125">If need be, you can use the @"microsoft.quantum.intrinsic.reset" operation, which returns the qubit to $\ket{0}$ by measuring it and conditionally performing an operation based on the result.</span></span> <span data-ttu-id="0436e-126">Essa medida destrói qualquer Entanglement com a qubits restante e, portanto, pode afetar a computação.</span><span class="sxs-lookup"><span data-stu-id="0436e-126">Such a measurement destroys any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="0436e-127">Qubits emprestado</span><span class="sxs-lookup"><span data-stu-id="0436e-127">Borrowed Qubits</span></span>

<span data-ttu-id="0436e-128">Use a `borrowing` instrução para alocar qubits para uso temporário, que não precisa estar em um estado específico.</span><span class="sxs-lookup"><span data-stu-id="0436e-128">Use the `borrowing` statement to allocate qubits for temporary use, which do not need to be in a specific state.</span></span>

<span data-ttu-id="0436e-129">Você pode usar qubits emprestados como espaço transitório durante uma computação.</span><span class="sxs-lookup"><span data-stu-id="0436e-129">You can use borrowed qubits as scratch space during a computation.</span></span>
<span data-ttu-id="0436e-130">Esses qubits geralmente não estão em um estado limpo, ou seja, eles não são necessariamente inicializados em um estado conhecido, como $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="0436e-130">These qubits are generally not in a clean state, that is, they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="0436e-131">Essas são muitas vezes chamadas de qubits "sujas" porque seu estado é desconhecido e pode até mesmo ser confusas com outras partes da memória do computador Quantum.</span><span class="sxs-lookup"><span data-stu-id="0436e-131">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="0436e-132">A associação segue o mesmo padrão e regras que a `using` instrução.</span><span class="sxs-lookup"><span data-stu-id="0436e-132">The binding follows the same pattern and rules as the `using` statement.</span></span>
<span data-ttu-id="0436e-133">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="0436e-133">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="0436e-134">O qubits emprestado está em um estado desconhecido e sai do escopo no final do bloco de instrução.</span><span class="sxs-lookup"><span data-stu-id="0436e-134">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="0436e-135">O tomador de confirmações para deixar o qubits no mesmo estado em que estavam emprestados; ou seja, seu estado no início e o final do bloco de instrução devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="0436e-135">The borrower commits to leaving the qubits in the same state they were in when they borrowed them; that is, their state at the beginning and the end of the statement block should be the same.</span></span>
<span data-ttu-id="0436e-136">Como esse estado não é necessariamente um estado clássico, na maioria dos casos, os escopos emprestados não devem conter medidas.</span><span class="sxs-lookup"><span data-stu-id="0436e-136">Because this state is not necessarily a classical state, in most cases borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="0436e-137">Ao emprestar qubits, o sistema primeiro tenta preencher a solicitação de qubits que estão em uso, mas que não são acessadas durante o corpo da `borrowing` instrução.</span><span class="sxs-lookup"><span data-stu-id="0436e-137">When borrowing qubits, the system first tries to fill the request from qubits that are in use but not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="0436e-138">Se não houver tal qubits suficiente, ele alocará novas qubits para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="0436e-138">If there aren't enough such qubits, then it allocates new qubits to complete the request.</span></span>

<span data-ttu-id="0436e-139">Entre os casos de uso conhecidos de qubits sujos estão implementações de Gates de CNOT de vários controle que exigem apenas poucos qubits e implementação de incrementais.</span><span class="sxs-lookup"><span data-stu-id="0436e-139">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="0436e-140">Para obter um exemplo de uso em Q #, confira o exemplo emissor [qubits](#borrowing-qubits-example) neste artigo ou a [*fatoração de papel usando 2n + 2 qubits com multiplicação modular baseada em Toffoli*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler e Svore 2017) para um algoritmo que utiliza a qubits emprestada.</span><span class="sxs-lookup"><span data-stu-id="0436e-140">For an example of their use in Q#, see [Borrowing Qubits Example](#borrowing-qubits-example) in this article, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="0436e-141">Operações intrínsecas</span><span class="sxs-lookup"><span data-stu-id="0436e-141">Intrinsic Operations</span></span>

<span data-ttu-id="0436e-142">Uma vez alocado, você pode passar um qubit para funções e operações.</span><span class="sxs-lookup"><span data-stu-id="0436e-142">Once allocated, you can pass a qubit to functions and operations.</span></span>
<span data-ttu-id="0436e-143">De certa forma, isso é tudo o que um programa Q # pode fazer com um qubit, pois as ações que podem ser executadas são todas definidas como operações.</span><span class="sxs-lookup"><span data-stu-id="0436e-143">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>

<span data-ttu-id="0436e-144">Este artigo discute algumas operações de Q # úteis que você pode usar para interagir com o qubits.</span><span class="sxs-lookup"><span data-stu-id="0436e-144">This article discusses a few useful Q# operations that you can use to interact with qubits.</span></span>
<span data-ttu-id="0436e-145">Para obter mais detalhes sobre esses e outros, consulte [operações e funções intrínsecas](xref:microsoft.quantum.libraries.standard.prelude).</span><span class="sxs-lookup"><span data-stu-id="0436e-145">For more detail about these and others, see [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span> 

<span data-ttu-id="0436e-146">Primeiro, os operadores de Pauli de qubit único $X $, $Y $ e $Z $ são representados em Q # pelas operações intrínsecas [`X`](xref:microsoft.quantum.intrinsic.x) , [`Y`](xref:microsoft.quantum.intrinsic.y) e [`Z`](xref:microsoft.quantum.intrinsic.z) cada um deles tem um tipo `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="0436e-146">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations [`X`](xref:microsoft.quantum.intrinsic.x), [`Y`](xref:microsoft.quantum.intrinsic.y), and [`Z`](xref:microsoft.quantum.intrinsic.z), each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="0436e-147">Conforme descrito em [operações e funções intrínsecas](xref:microsoft.quantum.libraries.standard.prelude), considere o $X $ e, portanto, `X` como uma operação de inversão de bits ou não de porta.</span><span class="sxs-lookup"><span data-stu-id="0436e-147">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="0436e-148">Você pode usar a `X` operação para preparar Estados do formulário $ \ket{s_0 s_1 \dots s_n} $ para uma cadeia de caracteres de bits clássica $s $:</span><span class="sxs-lookup"><span data-stu-id="0436e-148">You can use the `X` operation to prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
> <span data-ttu-id="0436e-149">Posteriormente, você verá mais formas compactadas de gravar essa operação que não exigem o fluxo de controle manual.</span><span class="sxs-lookup"><span data-stu-id="0436e-149">Later, you will see more compact ways of writing this operation that do not require manual control flow.</span></span>

<span data-ttu-id="0436e-150">Você também pode preparar Estados como $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ e $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ usando o Hadamard Transform $H $, que é representado em Q # pela operação intrínseca [`H`](xref:microsoft.quantum.intrinsic.h) (também do tipo (qubit = unidade de> é adj + CTL) "):</span><span class="sxs-lookup"><span data-stu-id="0436e-150">You can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation [`H`](xref:microsoft.quantum.intrinsic.h) (also of type (Qubit => Unit is Adj + Ctl)\`):</span></span>

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

## <a name="measurements"></a><span data-ttu-id="0436e-151">Medidas</span><span class="sxs-lookup"><span data-stu-id="0436e-151">Measurements</span></span>

<span data-ttu-id="0436e-152">As medidas de qubits individuais podem ser executadas em diferentes bases, cada uma representada por um eixo Pauli na [esfera Bloch](xref:microsoft.quantum.glossary#bloch-sphere).</span><span class="sxs-lookup"><span data-stu-id="0436e-152">Measurements of individual qubits can be performed in different bases, each represented by a Pauli axis on the [Bloch sphere](xref:microsoft.quantum.glossary#bloch-sphere).</span></span>
<span data-ttu-id="0436e-153">A *base computacional* refere-se à `PauliZ` base e é a base mais comum usada para medição.</span><span class="sxs-lookup"><span data-stu-id="0436e-153">The *computational basis* refers to the `PauliZ` basis, and is the most common basis used for measurement.</span></span>

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a><span data-ttu-id="0436e-154">Meça um único qubit na `PauliZ` base</span><span class="sxs-lookup"><span data-stu-id="0436e-154">Measure a single qubit in the `PauliZ` basis</span></span>

<span data-ttu-id="0436e-155">Use a [`M`](xref:microsoft.quantum.intrinsic.m) operação, que é uma operação não-unitário intrínseca interna, para medir um único qubit `PauliZ` com base e atribuir um valor clássico ao resultado.</span><span class="sxs-lookup"><span data-stu-id="0436e-155">Use the [`M`](xref:microsoft.quantum.intrinsic.m) operation, which is a built-in intrinsic non-unitary operation, to measure a single qubit in the `PauliZ` basis and assign a classical value to the result.</span></span>
<span data-ttu-id="0436e-156">`M`tem um tipo de retorno reservado, `Result` , que só pode ter valores `Zero` ou `One` correspondentes aos Estados medidos $ \ket {0} $ ou $ \ket {1} $-indicando que o resultado não é mais um estado Quantum.</span><span class="sxs-lookup"><span data-stu-id="0436e-156">`M` has a reserved return type, `Result`, which can only take values `Zero` or `One` corresponding to the measured states $\ket{0}$ or $\ket{1}$ - indicating that the result is no longer a quantum state.</span></span>

<span data-ttu-id="0436e-157">Um exemplo simples é a operação a seguir, que aloca um qubit no estado $ \ket {0} $ e, em seguida, aplica uma operação Hadamard `H` a ele e mede o resultado na `PauliZ` base.</span><span class="sxs-lookup"><span data-stu-id="0436e-157">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

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

### <a name="measure-one-or-more-qubits-in-specific-bases"></a><span data-ttu-id="0436e-158">Medir um ou mais qubits em bases específicas</span><span class="sxs-lookup"><span data-stu-id="0436e-158">Measure one or more qubits in specific bases</span></span>

<span data-ttu-id="0436e-159">Para medir uma matriz de um ou mais qubits em bases específicas, você pode usar a [`Measure`](xref:microsoft.quantum.intrinsic.measure) operação.</span><span class="sxs-lookup"><span data-stu-id="0436e-159">To measure an array of one or more qubits in specific bases, you can use the [`Measure`](xref:microsoft.quantum.intrinsic.measure) operation.</span></span>

<span data-ttu-id="0436e-160">As entradas para `Measure` são uma matriz de `Pauli` tipos (por exemplo, `[PauliX, PauliZ, PauliZ]` ) e uma matriz de qubits.</span><span class="sxs-lookup"><span data-stu-id="0436e-160">The inputs to `Measure` are an array of `Pauli` types (for example, `[PauliX, PauliZ, PauliZ]`) and an array of qubits.</span></span>

<span data-ttu-id="0436e-161">Um exemplo um pouco mais complicado é dado pela seguinte operação, que retorna o valor booliano `true` se todos os qubits em um registro do tipo `Qubit[]` estiverem no estado zero quando medido em uma base de Pauli especificada e que retorna de `false` outra forma.</span><span class="sxs-lookup"><span data-stu-id="0436e-161">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

<span data-ttu-id="0436e-162">Observe que esse exemplo ainda só `Measure` é executado em qubits individuais, um de cada vez, mas a operação pode ser estendida para medidas conjuntas em vários qubits.</span><span class="sxs-lookup"><span data-stu-id="0436e-162">Note that this example still only performs `Measure` on individual qubits one at a time, but the operation can be extended to joint measurements on multiple qubits.</span></span>

## <a name="borrowing-qubits-example"></a><span data-ttu-id="0436e-163">Exemplo de qubits de empréstimo</span><span class="sxs-lookup"><span data-stu-id="0436e-163">Borrowing Qubits Example</span></span>

<span data-ttu-id="0436e-164">Há exemplos na Canon que usam a `borrowing` palavra-chave, como a função a seguir `MultiControlledXBorrow` .</span><span class="sxs-lookup"><span data-stu-id="0436e-164">There are examples in the canon that use the `borrowing` keyword, such as the following function `MultiControlledXBorrow`.</span></span> <span data-ttu-id="0436e-165">Se `controls` o denotar o qubits de controle a ser adicionado a uma `X` operação, o número de [ancillas](xref:microsoft.quantum.glossary#ancilla) sujas adicionado por essa implementação será `Length(controls)-2` .</span><span class="sxs-lookup"><span data-stu-id="0436e-165">If `controls` denotes the control qubits to add to an `X` operation, then the number of dirty [ancillas](xref:microsoft.quantum.glossary#ancilla) added by this implementation is `Length(controls)-2`.</span></span>

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

<span data-ttu-id="0436e-166">Observe que este exemplo usou o uso extensivo do `With` combinador, em seu formato aplicável para operações que dão suporte a adjoint, por exemplo, `WithA` .</span><span class="sxs-lookup"><span data-stu-id="0436e-166">Note that this example used extensive use of the `With` combinator, in its form that is applicable for operations that support adjoint, for example, `WithA`.</span></span>
<span data-ttu-id="0436e-167">Esse é um bom estilo de programação, pois adicionar controle a estruturas que envolve `With` propaga controle somente para a operação interna.</span><span class="sxs-lookup"><span data-stu-id="0436e-167">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="0436e-168">Observe também que, além do `body` da operação, uma implementação do `controlled` corpo da operação foi fornecida explicitamente, em vez de recorrer a uma `controlled auto` instrução.</span><span class="sxs-lookup"><span data-stu-id="0436e-168">Also note that, in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="0436e-169">O motivo disso é que, devido à estrutura do circuito, é fácil adicionar mais controles, o que é benéfico em comparação à adição de controle a cada portão no `body` .</span><span class="sxs-lookup"><span data-stu-id="0436e-169">The reason for this is that, because of the structure of the circuit, it is easy to add further controls, which is beneficial compared to adding control to each gate in the `body`.</span></span> 

<span data-ttu-id="0436e-170">É instrutivo comparar esse código com outra função Canon `MultiControlledXClean` que atinge o mesmo objetivo de implementar uma operação controlada por multiplicação `X` , no entanto, que usa várias qubits limpas usando o `using` mecanismo.</span><span class="sxs-lookup"><span data-stu-id="0436e-170">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="0436e-171">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="0436e-171">Next steps</span></span>

<span data-ttu-id="0436e-172">Saiba mais sobre o [fluxo de controle](xref:microsoft.quantum.guide.controlflow) em Q #.</span><span class="sxs-lookup"><span data-stu-id="0436e-172">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>