---
title: 'Operações e funções em p #'
description: Como definir e chamar operações e funções, bem como as especializações de operação controladas e adjacentes.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
ms.openlocfilehash: 08eaf150a38afd789f8a23f567ff111d002bac07
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884217"
---
# <a name="operations-and-functions-in-q"></a><span data-ttu-id="9718a-103">Operações e funções em p #</span><span class="sxs-lookup"><span data-stu-id="9718a-103">Operations and Functions in Q#</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="9718a-104">Definindo novas operações</span><span class="sxs-lookup"><span data-stu-id="9718a-104">Defining New Operations</span></span>

<span data-ttu-id="9718a-105">As operações são o núcleo de Q #.</span><span class="sxs-lookup"><span data-stu-id="9718a-105">Operations are the core of Q#.</span></span>
<span data-ttu-id="9718a-106">Depois de declarados, eles podem ser chamados de aplicativos .NET clássicos, por exemplo, usando um simulador ou outras operações em Q #.</span><span class="sxs-lookup"><span data-stu-id="9718a-106">Once declared, they can either be called from classical .NET applications, for example, using a simulator or by other operations within Q#.</span></span>
<span data-ttu-id="9718a-107">Cada operação definida em Q # pode chamar qualquer número de outras operações, incluindo as operações intrínsecas internas definidas pelo idioma.</span><span class="sxs-lookup"><span data-stu-id="9718a-107">Each operation defined in Q# can call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="9718a-108">A maneira específica em que Q # define essas operações intrínsecas depende do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="9718a-108">The particular way in which Q# defines these intrinsic operations depends on the target machine.</span></span>
<span data-ttu-id="9718a-109">Quando compilada, cada operação é representada como um tipo de classe do .NET que pode ser fornecido para os computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="9718a-109">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

<span data-ttu-id="9718a-110">Cada arquivo de origem Q # pode definir qualquer número de operações.</span><span class="sxs-lookup"><span data-stu-id="9718a-110">Each Q# source file can define any number of operations.</span></span>
<span data-ttu-id="9718a-111">Os nomes de operação devem ser exclusivos em um namespace e não podem entrar em conflito com nomes de tipo ou função.</span><span class="sxs-lookup"><span data-stu-id="9718a-111">Operation names must be unique within a namespace and can not conflict with type or function names.</span></span>

<span data-ttu-id="9718a-112">Uma declaração de operação consiste na palavra-chave `operation` , seguida pelo símbolo que é o nome da operação, uma tupla de identificador tipada que define os argumentos para a operação, dois-pontos `:` , uma anotação de tipo que descreve o tipo de resultado da operação, opcionalmente uma anotação com as características da operação, uma chave de abertura e o corpo da declaração da operação, entre chaves `{ }` .</span><span class="sxs-lookup"><span data-stu-id="9718a-112">An operation declaration consists of the keyword `operation`, followed by the symbol that is the operation's name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation's result type, optionally an annotation with the operation characteristics, an open brace, and then the body of the operation declaration, enclosed in braces `{ }`.</span></span>

<span data-ttu-id="9718a-113">Cada operação usa uma entrada, produz uma saída e especifica a implementação para uma ou mais especializações de operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-113">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="9718a-114">As especializações possíveis e como defini-las e chamá-las são detalhadas nas diferentes seções deste artigo.</span><span class="sxs-lookup"><span data-stu-id="9718a-114">The possible specializations, and how to define and call them, are detailed in the different sections of this article.</span></span>
<span data-ttu-id="9718a-115">Por enquanto, considere a seguinte operação, que define apenas uma especialização de corpo padrão e usa um único qubit como sua entrada e, em seguida, chama a <xref:microsoft.quantum.intrinsic.x> operação interna nessa entrada:</span><span class="sxs-lookup"><span data-stu-id="9718a-115">For now, consider the following operation, which defines only a default body specialization and takes a single qubit as its input, then calls the built-in <xref:microsoft.quantum.intrinsic.x> operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="9718a-116">A palavra-chave `operation` começa a definição da operação, seguida pelo nome; aqui, `BitFlip` .</span><span class="sxs-lookup"><span data-stu-id="9718a-116">The keyword `operation` begins the operation definition, followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="9718a-117">Em seguida, o tipo de entrada é definido ( `Qubit` ), junto com um nome, `target` , para se referir à entrada dentro da nova operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-117">Next, the type of input is defined (`Qubit`), along with a name, `target`, for referring to the input within the new operation.</span></span>
<span data-ttu-id="9718a-118">Por fim, `Unit` define que a saída da operação está vazia.</span><span class="sxs-lookup"><span data-stu-id="9718a-118">Lastly, `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="9718a-119">`Unit`é usado da mesma forma `void` no C# e em outras linguagens imperativas e é equivalente a `unit` em F # e a outras linguagens funcionais.</span><span class="sxs-lookup"><span data-stu-id="9718a-119">`Unit` is used similarly to `void` in C# and other imperative languages and is equivalent to `unit` in F# and other functional languages.</span></span>

<span data-ttu-id="9718a-120">As operações também podem retornar tipos mais interessantes do que `Unit` .</span><span class="sxs-lookup"><span data-stu-id="9718a-120">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="9718a-121">Por exemplo, a <xref:microsoft.quantum.intrinsic.m> operação retorna uma saída do tipo `Result` , representando tendo realizado uma medição.</span><span class="sxs-lookup"><span data-stu-id="9718a-121">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span>  <span data-ttu-id="9718a-122">Você pode passá-lo de uma operação para outra operação ou usá-lo com a `let` palavra-chave para definir uma nova variável.</span><span class="sxs-lookup"><span data-stu-id="9718a-122">You can pass it from an operation to another operation or use it with the `let` keyword to define a new variable.</span></span>

<span data-ttu-id="9718a-123">Essa abordagem permite representar a computação clássica que interage com as operações Quantum em um nível baixo, como na [codificação superdensa](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span><span class="sxs-lookup"><span data-stu-id="9718a-123">This approach allows for representing classical computation that interacts with quantum operations at a low level, such as in [superdense coding](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> <span data-ttu-id="9718a-124">Cada operação em Q # usa exatamente uma entrada e retorna exatamente uma saída.</span><span class="sxs-lookup"><span data-stu-id="9718a-124">Each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="9718a-125">Várias entradas e saídas são representadas usando *tuplas*, que coletam vários valores juntos em um único valor.</span><span class="sxs-lookup"><span data-stu-id="9718a-125">Multiple inputs and outputs are represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="9718a-126">Nesse sentido, Q # é uma linguagem de "tupla-in-out".</span><span class="sxs-lookup"><span data-stu-id="9718a-126">In this regard, Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="9718a-127">Após esse conceito, um conjunto de parênteses vazios, `()` , deve ser lido como a tupla "vazia", que tem o tipo `Unit` .</span><span class="sxs-lookup"><span data-stu-id="9718a-127">Following this concept, a set of empty parentheses, `()`, should then be read as the "empty" tuple, which has the type `Unit`.</span></span>

## <a name="controlled-and-adjoint-operations"></a><span data-ttu-id="9718a-128">Operações controladas e adjacentes</span><span class="sxs-lookup"><span data-stu-id="9718a-128">Controlled and Adjoint Operations</span></span>

<span data-ttu-id="9718a-129">Se uma operação implementa uma transformação unitário, como é o caso de muitas operações em Q #, é possível definir como a operação age quando *adjointed* ou *controlada*.</span><span class="sxs-lookup"><span data-stu-id="9718a-129">If an operation implements a unitary transformation, as is the case for many operations in Q#, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="9718a-130">Uma especialização *adjacente* de uma operação especifica como o "inverso" da operação age, enquanto uma especialização *controlada* especifica como uma operação age quando seu aplicativo é condicionado no estado de um registro de Quantum específico.</span><span class="sxs-lookup"><span data-stu-id="9718a-130">An *adjoint* specialization of an operation specifies how the "inverse" of the operation acts, while a *controlled* specialization specifies how an operation acts when its application is conditioned on the state of a particular quantum register.</span></span>

<span data-ttu-id="9718a-131">Adjoints de operações Quantum são cruciais para muitos aspectos da computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="9718a-131">Adjoints of quantum operations are crucial to many aspects of quantum computing.</span></span> <span data-ttu-id="9718a-132">Para obter um exemplo de uma dessas situações discutida junto com uma técnica útil de programação de Q #, consulte [conjugados](#conjugations) neste artigo.</span><span class="sxs-lookup"><span data-stu-id="9718a-132">For an example of one such situation discussed alongside a useful Q# programming technique, see [Conjugations](#conjugations) in this article.</span></span> 

<span data-ttu-id="9718a-133">A versão controlada de uma operação é uma nova operação que aplica efetivamente a operação base somente se todas as qubits de controle estiverem em um estado especificado.</span><span class="sxs-lookup"><span data-stu-id="9718a-133">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="9718a-134">Se o controle qubits estiver em superposição, a operação base será aplicada coerentemente à parte apropriada da superposição.</span><span class="sxs-lookup"><span data-stu-id="9718a-134">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="9718a-135">Portanto, as operações controladas geralmente são usadas para gerar Entanglement.</span><span class="sxs-lookup"><span data-stu-id="9718a-135">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="9718a-136">Naturalmente, uma especialização *adjacente controlada* poderia existir também, especificando o aplicativo controlado de um adjacente de uma operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-136">Naturally, a *controlled adjoint* specialization could exist as well, specifying the controlled application of an operation's adjoint.</span></span>

> [!NOTE]
> <span data-ttu-id="9718a-137">Se $U $ for a transformação unitário implementada por uma operação `U` , `Adjoint U` o representará a transformação unitário $U ^ \dagger $, que é a transpoção conjugada complexa.</span><span class="sxs-lookup"><span data-stu-id="9718a-137">If $U$ is the unitary transformation implemented by an operation `U`, then `Adjoint U` represents the unitary transformation $U^\dagger$, which is the complex conjugate transpose.</span></span>
> <span data-ttu-id="9718a-138">Aplicar sucessivamente uma operação e, em seguida, seu adjacente a um estado deixa o estado inalterado, conforme ilustrado pelo fato de que $UU ^ \dagger = U ^ \dagger U = \id $, a matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="9718a-138">Successively applying an operation and then its adjoint to a state leaves the state unchanged, as illustrated by the fact that $UU^\dagger = U^\dagger U = \id$, the identity matrix.</span></span>
> <span data-ttu-id="9718a-139">A representação unitário de uma operação controlada é ligeiramente mais nuance, mas você pode encontrar mais detalhes em [conceitos de computação Quantum: vários qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span><span class="sxs-lookup"><span data-stu-id="9718a-139">The unitary representation of a controlled operation is slightly more nuanced, but you can find more details at [Quantum computing concepts: multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

<span data-ttu-id="9718a-140">A seção a seguir descreve como chamar essas várias especializações no código de Q # e como definir operações para dar suporte a elas.</span><span class="sxs-lookup"><span data-stu-id="9718a-140">The following section describes how to call these various specializations in your Q# code, and how to define operations to support them.</span></span>

### <a name="calling-operation-specializations"></a><span data-ttu-id="9718a-141">Chamando especializações de operação</span><span class="sxs-lookup"><span data-stu-id="9718a-141">Calling operation specializations</span></span>

<span data-ttu-id="9718a-142">Um *functor* em Q # é um alocador que define uma nova operação de outra operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-142">A *functor* in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="9718a-143">Os dois transmissão functors padrão em Q # são `Adjoint` e `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="9718a-143">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

<span data-ttu-id="9718a-144">Transmissão functors têm acesso à implementação da operação base ao definir a implementação da nova operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-144">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="9718a-145">Portanto, o transmissão functors pode executar funções mais complexas do que as funções tradicionais de nível superior.</span><span class="sxs-lookup"><span data-stu-id="9718a-145">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span> <span data-ttu-id="9718a-146">Transmissão functors não tem uma representação no sistema do tipo Q #.</span><span class="sxs-lookup"><span data-stu-id="9718a-146">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="9718a-147">Portanto, no momento, não é possível associá-los a uma variável ou passá-los como argumentos.</span><span class="sxs-lookup"><span data-stu-id="9718a-147">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="9718a-148">Use um functor aplicando-o a uma operação, que retorna uma nova operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-148">Use a functor by applying it to an operation, which returns a new operation.</span></span>
<span data-ttu-id="9718a-149">Por exemplo, aplicar o `Adjoint` functor à `Y` operação retorna a nova operação `Adjoint Y` .</span><span class="sxs-lookup"><span data-stu-id="9718a-149">For example, applying the `Adjoint` functor to the `Y` operation returns the new operation `Adjoint Y`.</span></span> <span data-ttu-id="9718a-150">Você pode invocar a nova operação como qualquer outra operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-150">You can invoke the new operation like any other operation.</span></span>
<span data-ttu-id="9718a-151">Para uma operação para dar suporte ao aplicativo do `Adjoint` ou `Controlled` transmissão functors, seu tipo de retorno precisa ser necessariamente `Unit` .</span><span class="sxs-lookup"><span data-stu-id="9718a-151">For an operation to support the application of the `Adjoint` or `Controlled` functors, its return type necessarily needs to be `Unit`.</span></span> 

#### <a name="adjoint-functor"></a><span data-ttu-id="9718a-152">`Adjoint`functor</span><span class="sxs-lookup"><span data-stu-id="9718a-152">`Adjoint` functor</span></span>

<span data-ttu-id="9718a-153">Assim, `Adjoint Y(q1)` o aplica o `Adjoint` functor à `Y` operação para gerar uma nova operação e aplica essa nova operação ao `q1` .</span><span class="sxs-lookup"><span data-stu-id="9718a-153">Thus, `Adjoint Y(q1)` applies the `Adjoint` functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>
<span data-ttu-id="9718a-154">A nova operação tem a mesma assinatura e tipo que a operação base `Y` .</span><span class="sxs-lookup"><span data-stu-id="9718a-154">The new operation has the same signature and type as the base operation `Y`.</span></span>
<span data-ttu-id="9718a-155">Em particular, a nova operação também dá suporte a e `Adjoint` dá suporte a `Controlled` If e somente se a operação base tiver feito.</span><span class="sxs-lookup"><span data-stu-id="9718a-155">In particular, the new operation also supports `Adjoint`, and supports `Controlled` if and only if the base operation did.</span></span>
<span data-ttu-id="9718a-156">O `Adjoint` functor é seu próprio inverso; ou seja, `Adjoint Adjoint Op` é sempre o mesmo que `Op` .</span><span class="sxs-lookup"><span data-stu-id="9718a-156">The `Adjoint` functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled-functor"></a><span data-ttu-id="9718a-157">`Controlled`functor</span><span class="sxs-lookup"><span data-stu-id="9718a-157">`Controlled` functor</span></span>

<span data-ttu-id="9718a-158">Da mesma forma, `Controlled X(controls, target)` o aplica o `Controlled` functor à `X` operação para gerar uma nova operação e aplica essa nova operação ao `controls` e ao `target` .</span><span class="sxs-lookup"><span data-stu-id="9718a-158">Similarly, `Controlled X(controls, target)` applies the `Controlled` functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

> [!NOTE]
> <span data-ttu-id="9718a-159">Em Q #, as versões controladas sempre usam uma matriz de qubits de controle, e o controle é sempre baseado em todos os qubits de controle que estão no `PauliZ` estado computacional () `One` , $ \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="9718a-159">In Q#, controlled versions always take an array of control qubits, and the controlling is always based on all of the control qubits being in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
> <span data-ttu-id="9718a-160">O controle com base em outros Estados é obtido aplicando a operação unitário apropriada ao qubits de controle antes da operação controlada e, em seguida, aplicando as inversas da operação unitário após a operação controlada.</span><span class="sxs-lookup"><span data-stu-id="9718a-160">Controlling based on other states is achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
> <span data-ttu-id="9718a-161">Por exemplo, a aplicação de uma `X` operação a um qubit de controle antes e depois de uma operação controlada faz com que a operação controle o `Zero` estado ($ \ket {0} $) para esse qubit; a aplicação de uma `H` operação antes e depois dos controles no `PauliX` `One` estado, que é-1 eigenvalue de Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ em vez do `PauliZ` `One` estado.</span><span class="sxs-lookup"><span data-stu-id="9718a-161">For example, applying an `X` operation to a control qubit before and after a controlled operation causes the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after controls on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="9718a-162">Dada uma expressão de operação, você pode formar uma nova expressão de operação usando o `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="9718a-162">Given an operation expression, you can form a new operation expression by using the `Controlled` functor.</span></span>
<span data-ttu-id="9718a-163">A assinatura da nova operação é baseada na assinatura da operação original.</span><span class="sxs-lookup"><span data-stu-id="9718a-163">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="9718a-164">O tipo de resultado é o mesmo, mas o tipo de entrada é de duas tuplas com uma matriz qubit que mantém o controle qubit (s) como o primeiro elemento e os argumentos da operação original como o segundo elemento.</span><span class="sxs-lookup"><span data-stu-id="9718a-164">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="9718a-165">A nova operação dá suporte a `Controlled` e dará suporte a `Adjoint` If e somente se a operação original tiver feito isso.</span><span class="sxs-lookup"><span data-stu-id="9718a-165">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="9718a-166">Se a operação original levou apenas um único argumento, a [equivalência de tupla singleton](xref:microsoft.quantum.guide.types) entra em cena aqui.</span><span class="sxs-lookup"><span data-stu-id="9718a-166">If the original operation took only a single argument, then [singleton tuple equivalence](xref:microsoft.quantum.guide.types) comes into play here.</span></span>
<span data-ttu-id="9718a-167">Por exemplo, `Controlled X` é a versão controlada da `X` operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-167">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span> 
<span data-ttu-id="9718a-168">`X`tem tipo `(Qubit => Unit is Adj + Ctl)` , portanto, `Controlled X` tem tipo `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; devido à equivalência de tupla singleton, isso é o mesmo que `((Qubit[], Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="9718a-168">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="9718a-169">Se a operação base levou vários argumentos, lembre-se de colocar os argumentos correspondentes da versão controlada da operação entre parênteses para convertê-los em uma tupla.</span><span class="sxs-lookup"><span data-stu-id="9718a-169">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="9718a-170">Por exemplo, `Controlled Rz` é a versão controlada da `Rz` operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-170">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span> 
<span data-ttu-id="9718a-171">`Rz`tem tipo `((Double, Qubit) => Unit is Adj + Ctl)` , portanto, `Controlled Rz` tem tipo `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="9718a-171">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="9718a-172">Portanto, `Controlled Rz(controls, (0.1, target))` seria uma invocação válida de `Controlled Rz` (Observe os parênteses `0.1, target` ).</span><span class="sxs-lookup"><span data-stu-id="9718a-172">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="9718a-173">Como outro exemplo, `CNOT(control, target)` pode ser implementado como `Controlled X([control], target)` .</span><span class="sxs-lookup"><span data-stu-id="9718a-173">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="9718a-174">Se um destino deve ser controlado por dois qubits de controle (CCNOT), use uma `Controlled X([control1, control2], target)` instrução.</span><span class="sxs-lookup"><span data-stu-id="9718a-174">If a target should be controlled by two control qubits (CCNOT), use a `Controlled X([control1, control2], target)` statement.</span></span>

#### `Controlled Adjoint` 

<span data-ttu-id="9718a-175">O `Controlled` e o `Adjoint` transmissão functorsm o áudio, portanto, não há nenhuma diferença entre aplicar `Controlled Adjoint Op` ou `Adjoint Controlled Op` .</span><span class="sxs-lookup"><span data-stu-id="9718a-175">The `Controlled` and `Adjoint` functors commute, so there is no difference between applying `Controlled Adjoint Op` or `Adjoint Controlled Op`.</span></span>


## <a name="defining-controlled-and-adjoint-implementations"></a><span data-ttu-id="9718a-176">Definindo implementações controladas e adjacentes</span><span class="sxs-lookup"><span data-stu-id="9718a-176">Defining Controlled and Adjoint Implementations</span></span>

<span data-ttu-id="9718a-177">Na primeira declaração de operação nos exemplos anteriores, as operações `BitFlip` e `DecodeSuperdense` foram definidas com assinaturas `(Qubit => Unit)` e `((Qubit, Qubit) => (Result, Result))` , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9718a-177">In the first operation declaration in the previous examples, the operations `BitFlip` and `DecodeSuperdense` were defined with signatures `(Qubit => Unit)` and `((Qubit, Qubit) => (Result, Result))`, respectively.</span></span>
<span data-ttu-id="9718a-178">Como `DecodeSuperdense` inclui medições, ela não é uma operação unitário e, portanto, nenhuma especialização não adjacente pode existir (Lembre-se do requisito relacionado que tal operação retorna `Unit` ).</span><span class="sxs-lookup"><span data-stu-id="9718a-178">As `DecodeSuperdense` includes measurements, it is not a unitary operation, and therefore neither controlled not adjoint specializations could exist (recall the related requirement that such an operation return `Unit`).</span></span>
<span data-ttu-id="9718a-179">No entanto, como `BitFlip` simplesmente executa a <xref:microsoft.quantum.intrinsic.x> operação unitário, você poderia defini-la com ambas as especializações.</span><span class="sxs-lookup"><span data-stu-id="9718a-179">However, as `BitFlip` simply performs the unitary <xref:microsoft.quantum.intrinsic.x> operation, you could have defined it with both specializations.</span></span>

<span data-ttu-id="9718a-180">Esta seção fornece detalhes sobre como incluir a existência de especializações em suas declarações de operação do Q #, portanto, dando-lhes a capacidade de chamada em conjunto com o `Adjoint` ou o `Controlled` transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="9718a-180">This section details how to include the existence of specializations in your Q# operation declarations, hence giving them the ability to called in conjunction with the `Adjoint` or `Controlled` functors.</span></span>
<span data-ttu-id="9718a-181">Para obter mais informações sobre algumas das situações em que elas são válidas ou não válidas para declarar determinadas especializações, consulte [circunstâncias de definição válida de especializações](#circumstances-for-validly-defining-specializations) neste artigo.</span><span class="sxs-lookup"><span data-stu-id="9718a-181">For more information about some of the situations in which it is either valid or not valid to declare certain specializations, see [Circumstances for validly defining specializations](#circumstances-for-validly-defining-specializations) in this article.</span></span>

<span data-ttu-id="9718a-182">As características da operação definem quais tipos de transmissão functors você pode aplicar à operação declarada e qual efeito eles têm.</span><span class="sxs-lookup"><span data-stu-id="9718a-182">Operation characteristics define what kinds of functors you can apply to the declared operation, and what effect they have.</span></span> <span data-ttu-id="9718a-183">A existência dessas especializações pode ser declarada como parte da assinatura da operação, especificamente por meio de uma anotação com as características da operação: `is Adj` `is Ctl` ou, ou `is Adj + Ctl` .</span><span class="sxs-lookup"><span data-stu-id="9718a-183">The existence of these specializations can be declared as part of the operation signature, specifically through an annotation with the operation characteristics: either `is Adj`, `is Ctl`, or `is Adj + Ctl`.</span></span>
<span data-ttu-id="9718a-184">A implementação real de cada especialização pode ser definida *implicitamente* ou *explicitamente* .</span><span class="sxs-lookup"><span data-stu-id="9718a-184">The actual implementation of each specialization can either be *implicitly* or *explicitly* defined.</span></span>

### <a name="implicitly-specifying-implementations"></a><span data-ttu-id="9718a-185">Especificando implicitamente implementações</span><span class="sxs-lookup"><span data-stu-id="9718a-185">Implicitly specifying implementations</span></span>

<span data-ttu-id="9718a-186">Nesse caso, o corpo da declaração da operação consiste exclusivamente na implementação padrão.</span><span class="sxs-lookup"><span data-stu-id="9718a-186">In this case, the body of the operation declaration consists solely of the default implementation.</span></span> <span data-ttu-id="9718a-187">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9718a-187">For example:</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
<span data-ttu-id="9718a-188">Aqui, a implementação correspondente para cada uma dessas especializações declaradas implicitamente é gerada automaticamente pelo compilador, a ser executada se o `Adjoint` ou `Controlled` transmissão functors forem usados.</span><span class="sxs-lookup"><span data-stu-id="9718a-188">Here, the corresponding implementation for each such implicitly declared specialization is automatically generated by the compiler, to be performed if the `Adjoint` or `Controlled` functors are used.</span></span>

<span data-ttu-id="9718a-189">Portanto, uma chamada de `Adjoint PrepareEntangledPair` resultaria no compilador que implementasse o adpositivo de `CNOT` e, em seguida, o adjacente de `H` .</span><span class="sxs-lookup"><span data-stu-id="9718a-189">So, a call of `Adjoint PrepareEntangledPair` would result in the compiler implementing the adjoint of `CNOT` and then the adjoint of `H`.</span></span>
<span data-ttu-id="9718a-190">Essas operações individuais são autoadjacentes, portanto, a operação resultante `Adjoint PrepareEntangledPair` simplesmente consistiria em aplicar `CNOT(here, there)` e depois `H(here)` .</span><span class="sxs-lookup"><span data-stu-id="9718a-190">These individual operations are both self-adjoint, so the resulting `Adjoint PrepareEntangledPair` operation would simply consist of applying `CNOT(here, there)` and then `H(here)`.</span></span>
<span data-ttu-id="9718a-191">Portanto, você pode usar isso para escrever o `DecodeSuperdense` no exemplo anterior mais compactamente, usando o adjoin de `PrepareEntangledPair` para transformar o estado confusas de volta em um par unentangled de qubits:</span><span class="sxs-lookup"><span data-stu-id="9718a-191">Hence you can use this to write the `DecodeSuperdense` in the previous example more compactly, by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="9718a-192">A anotação com as características da operação na declaração é útil para garantir que o compilador gere automaticamente outras especializações com base na implementação padrão.</span><span class="sxs-lookup"><span data-stu-id="9718a-192">The annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="9718a-193">Há várias limitações importantes a serem consideradas ao criar operações para uso com o transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="9718a-193">There are several important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="9718a-194">O mais importante é que as especializações para uma operação que usa o valor de saída de qualquer outra operação *não podem* ser geradas automaticamente pelo compilador, pois é ambígua como reordenar as instruções nessa operação para obter o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="9718a-194">Most critically, specializations for an operation that uses the output value of any other operation *cannot* be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>

<span data-ttu-id="9718a-195">Portanto, geralmente é útil especificar explicitamente as várias implementações.</span><span class="sxs-lookup"><span data-stu-id="9718a-195">Therefore, it is often useful to explicitly specify the various implementations.</span></span>

### <a name="explicitly-specifying-implementations"></a><span data-ttu-id="9718a-196">Especificando explicitamente implementações</span><span class="sxs-lookup"><span data-stu-id="9718a-196">Explicitly specifying implementations</span></span>

<span data-ttu-id="9718a-197">No caso em que o compilador não pode gerar a implementação, você pode especificá-lo explicitamente.</span><span class="sxs-lookup"><span data-stu-id="9718a-197">In the case where the compiler cannot generate the implementation, you can specify it explicitly.</span></span> <span data-ttu-id="9718a-198">Essas declarações de especialização explícitas podem consistir em uma *diretiva de geração* adequada ou em uma implementação definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9718a-198">Such explicit specialization declarations can consist of a suitable *generation directive* or a user-defined implementation.</span></span>
<span data-ttu-id="9718a-199">A seguir, há uma gama completa de possibilidades, com alguns exemplos de especialização explícita.</span><span class="sxs-lookup"><span data-stu-id="9718a-199">Following are the full range of possibilities, with some examples of explicit specialization.</span></span> 


#### <a name="explicit-specialization-declarations"></a><span data-ttu-id="9718a-200">Declarações de especialização explícitas</span><span class="sxs-lookup"><span data-stu-id="9718a-200">Explicit specialization declarations</span></span>

<span data-ttu-id="9718a-201">As operações de Q # podem conter as seguintes declarações de especialização explícitas:</span><span class="sxs-lookup"><span data-stu-id="9718a-201">Q# operations can contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="9718a-202">A `body` especialização especifica a implementação da operação sem nenhum transmissão functors aplicado.</span><span class="sxs-lookup"><span data-stu-id="9718a-202">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="9718a-203">A `adjoint` especialização especifica a implementação da operação com o `Adjoint` functor aplicado.</span><span class="sxs-lookup"><span data-stu-id="9718a-203">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="9718a-204">A `controlled` especialização especifica a implementação da operação com o `Controlled` functor aplicado.</span><span class="sxs-lookup"><span data-stu-id="9718a-204">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="9718a-205">A `controlled adjoint` especialização especifica a implementação da operação com o `Adjoint` e o `Controlled` transmissão functors aplicados.</span><span class="sxs-lookup"><span data-stu-id="9718a-205">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="9718a-206">Essa especialização também pode ser nomeada `adjoint controlled` , já que as duas transmissão functorsm.</span><span class="sxs-lookup"><span data-stu-id="9718a-206">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="9718a-207">Uma especialização de operação consiste na marca de especialização (por exemplo, `body` ou `adjoint` ) seguida de uma das:</span><span class="sxs-lookup"><span data-stu-id="9718a-207">An operation specialization consists of the specialization tag (for example, `body` or `adjoint`) followed by one of:</span></span>

- <span data-ttu-id="9718a-208">Uma declaração explícita, conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="9718a-208">An explicit declaration as described in the following.</span></span>
- <span data-ttu-id="9718a-209">Uma *diretiva* que informa ao compilador *como* gerar a especialização, uma das:</span><span class="sxs-lookup"><span data-stu-id="9718a-209">A *directive* that tells the compiler *how* to generate the specialization, one of:</span></span>
  - <span data-ttu-id="9718a-210">`intrinsic`, que indica que o computador de destino fornece a especialização.</span><span class="sxs-lookup"><span data-stu-id="9718a-210">`intrinsic`, which indicates that the target machine provides the specialization.</span></span>
  - <span data-ttu-id="9718a-211">`distribute`, usado com as `controlled` `controlled adjoint` especializações e.</span><span class="sxs-lookup"><span data-stu-id="9718a-211">`distribute`, used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="9718a-212">Quando usado com `controlled` , ele indica que o compilador deve calcular a especialização aplicando-se `Controlled` a todas as operações no `body` .</span><span class="sxs-lookup"><span data-stu-id="9718a-212">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="9718a-213">Quando usado com `controlled adjoint` , ele indica que o compilador deve calcular a especialização aplicando-se `Controlled` a todas as operações na `adjoint` especialização.</span><span class="sxs-lookup"><span data-stu-id="9718a-213">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="9718a-214">`invert`, que indica que o compilador deve calcular a `adjoint` especialização invertendo o `body` , por exemplo, revertendo a ordem das operações e aplicando o adjacente a cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="9718a-214">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, for example, reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="9718a-215">Quando usado com `adjoint controlled` , isso indica que o compilador deve calcular a especialização invertendo a `controlled` especialização.</span><span class="sxs-lookup"><span data-stu-id="9718a-215">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="9718a-216">`self`, para indicar que a especialização de adjacente é igual à `body` especialização.</span><span class="sxs-lookup"><span data-stu-id="9718a-216">`self`, to indicate that the adjoint specialization is the same as the `body` specialization.</span></span>
    <span data-ttu-id="9718a-217">Usar `self` o é legal para `adjoint` as `adjoint controlled` especializações e.</span><span class="sxs-lookup"><span data-stu-id="9718a-217">Using `self` is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="9718a-218">Para `adjoint controlled` , `self` implica que a `adjoint controlled` especialização é a mesma que a `controlled` especialização.</span><span class="sxs-lookup"><span data-stu-id="9718a-218">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="9718a-219">`auto`, para indicar que o compilador deve selecionar uma diretiva apropriada a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="9718a-219">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="9718a-220">Você não pode usar `auto` para a `body` especialização.</span><span class="sxs-lookup"><span data-stu-id="9718a-220">You cannot use`auto` for the `body` specialization.</span></span>

<span data-ttu-id="9718a-221">As diretivas e `auto` todas exigem um ponto-e-vírgula de fechamento `;` .</span><span class="sxs-lookup"><span data-stu-id="9718a-221">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="9718a-222">A `auto` diretiva será resolvida para a seguinte diretiva gerada se uma declaração explícita do `body` for fornecida:</span><span class="sxs-lookup"><span data-stu-id="9718a-222">The `auto` directive resolves to the following generated directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="9718a-223">A `adjoint` especialização gera de acordo com a diretiva `invert` .</span><span class="sxs-lookup"><span data-stu-id="9718a-223">The `adjoint` specialization generates according to the directive `invert`.</span></span>
- <span data-ttu-id="9718a-224">A `controlled` especialização gera de acordo com a diretiva `distribute` .</span><span class="sxs-lookup"><span data-stu-id="9718a-224">The `controlled` specialization generates according to the directive `distribute`.</span></span>
- <span data-ttu-id="9718a-225">A `adjoint controlled` especialização gera de acordo com a diretiva `invert` se uma declaração explícita para `controlled` é fornecida, mas não uma para `adjoint` , e de `distribute` outra forma.</span><span class="sxs-lookup"><span data-stu-id="9718a-225">The `adjoint controlled` specialization  generates according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="9718a-226">Se uma operação for autoadjacente, especifique explicitamente a prejunção ou a especialização de adjacente controlada por meio da diretiva de geração `self` para permitir que o compilador use essas informações para fins de otimização.</span><span class="sxs-lookup"><span data-stu-id="9718a-226">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="9718a-227">Uma declaração de especialização que contém uma implementação definida pelo usuário consiste em uma tupla de argumento seguida por um bloco de instrução com o código Q # que implementa a especialização.</span><span class="sxs-lookup"><span data-stu-id="9718a-227">A specialization declaration containing a user-defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="9718a-228">Na lista de argumentos, `...` é usado para representar os argumentos declarados para a operação como um todo.</span><span class="sxs-lookup"><span data-stu-id="9718a-228">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="9718a-229">Para `body` e `adjoint` , a lista de argumentos deve ser sempre `(...)` ; para `controlled` e `adjoint controlled` , a lista de argumentos deve ser um símbolo que representa a matriz de controle qubits, seguida por `...` , entre parênteses; por exemplo, `(controls,...)` .</span><span class="sxs-lookup"><span data-stu-id="9718a-229">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

### <a name="examples"></a><span data-ttu-id="9718a-230">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9718a-230">Examples</span></span>

<span data-ttu-id="9718a-231">Uma declaração de operação pode ser tão simples quanto a seguinte, que define a operação primitiva de Pauli X:</span><span class="sxs-lookup"><span data-stu-id="9718a-231">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
<span data-ttu-id="9718a-232">Observe que o adjoin da operação Pauli X é definido com a diretiva `self` porque, por definição, `X` é seu próprio inverso.</span><span class="sxs-lookup"><span data-stu-id="9718a-232">Note that the adjoint of the Pauli X operation is defined with the directive `self` because by definition `X` is its own inverse.</span></span>

<span data-ttu-id="9718a-233">No exemplo anterior `PrepareEntangledPair` , o código é equivalente ao seguinte código que contém declarações de especialização explícitas:</span><span class="sxs-lookup"><span data-stu-id="9718a-233">In the earlier `PrepareEntangledPair` example, the code is equivalent to the following code containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="9718a-234">A palavra-chave `auto` indica que o compilador deve determinar como gerar a implementação de especialização.</span><span class="sxs-lookup"><span data-stu-id="9718a-234">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>

#### <a name="user-defined-specialization-implementation"></a><span data-ttu-id="9718a-235">Implementação de especialização definida pelo usuário</span><span class="sxs-lookup"><span data-stu-id="9718a-235">User-defined specialization implementation</span></span>

<span data-ttu-id="9718a-236">Se o compilador não puder gerar a implementação para determinada especialização automaticamente ou se uma implementação mais eficiente puder ser fornecida, você poderá definir manualmente a implementação.</span><span class="sxs-lookup"><span data-stu-id="9718a-236">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then you can manually define the implementation.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="9718a-237">No exemplo anterior, `adjoint invert;` indica que a especialização de adjacente deve ser gerada pela inversão da implementação do corpo e `controlled adjoint invert;` indica que a especialização adjacente controlada deve ser gerada pela inversão da implementação fornecida da especialização controlada.</span><span class="sxs-lookup"><span data-stu-id="9718a-237">In the previous example, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="9718a-238">Se uma ou mais especializações além do corpo padrão precisarem ser declaradas explicitamente, a implementação do corpo padrão precisará ser encapsulada em uma declaração de especialização adequada também:</span><span class="sxs-lookup"><span data-stu-id="9718a-238">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="circumstances-for-validly-defining-specializations"></a><span data-ttu-id="9718a-239">Circunstâncias de definição válida de especializações</span><span class="sxs-lookup"><span data-stu-id="9718a-239">Circumstances for validly defining specializations</span></span>

#### <a name="operation-declarations-with-adjointcontrolled"></a><span data-ttu-id="9718a-240">Declarações de operação com adjoind/controlled</span><span class="sxs-lookup"><span data-stu-id="9718a-240">Operation declarations with adjoint/controlled</span></span>

<span data-ttu-id="9718a-241">É legal especificar uma operação sem nenhuma versão adjacente ou controlada.</span><span class="sxs-lookup"><span data-stu-id="9718a-241">It is legal to specify an operation with no adjoint or controlled versions.</span></span> <span data-ttu-id="9718a-242">Por exemplo, as operações de medição não têm porque elas não são invertível ou controláveis.</span><span class="sxs-lookup"><span data-stu-id="9718a-242">For instance, measurement operations have neither because they are not invertible or controllable.</span></span>

<span data-ttu-id="9718a-243">Uma operação dá suporte a `Adjoint` e `Controlled` transmissão functors se sua declaração contiver uma declaração implícita ou explícita das respectivas especializações.</span><span class="sxs-lookup"><span data-stu-id="9718a-243">An operation supports the `Adjoint` and `Controlled` functors if its declaration contains an implicit or explicit declaration of the respective specializations.</span></span>

<span data-ttu-id="9718a-244">Uma especialização adjacente/controlada explícita implica a existência de uma especialização adjacente/controlada.</span><span class="sxs-lookup"><span data-stu-id="9718a-244">An explicitly declared adjoint/controlled specialization implies the existence of an adjoint/controlled specialization.</span></span> 

<span data-ttu-id="9718a-245">Para uma operação cujo corpo contém loops repetir-até-êxito, instruções SET, medidas, instruções de retorno ou chamadas para outras operações que não dão suporte a `Adjoint` functor, a geração automática de uma especialização de adjacente após a `invert` `auto` diretiva ou não é possível.</span><span class="sxs-lookup"><span data-stu-id="9718a-245">For an operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

<span data-ttu-id="9718a-246">Para uma operação cujo corpo contém chamadas para outras operações que não dão suporte ao `Controlled` functor, a geração automática de uma especialização controlada após a `distribute` `auto` diretiva ou não é possível.</span><span class="sxs-lookup"><span data-stu-id="9718a-246">For an operation whose body contains calls to other operations that do not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

#### <a name="controlled-adjoint"></a><span data-ttu-id="9718a-247">Adjacente controlado</span><span class="sxs-lookup"><span data-stu-id="9718a-247">Controlled Adjoint</span></span>

<span data-ttu-id="9718a-248">A versão adjacente controlada de uma operação especifica como implementar uma versão controlada pelo Quantum do adjoin da operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-248">The controlled adjoint version of an operation specifies how to implement a quantum-controlled version of the adjoint of the operation.</span></span>
<span data-ttu-id="9718a-249">É legal especificar uma operação sem nenhuma versão adjacente controlada; por exemplo, as operações de medição não têm nenhuma versão adjacente controlada porque não são controláveis nem invertível.</span><span class="sxs-lookup"><span data-stu-id="9718a-249">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="9718a-250">Uma especialização de adjacente controlada para uma operação precisa existir se e somente se houver uma especialização de somente um e um adjacente.</span><span class="sxs-lookup"><span data-stu-id="9718a-250">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="9718a-251">Nesse caso, a existência da especialização adjacente controlada é inferida.</span><span class="sxs-lookup"><span data-stu-id="9718a-251">In that case, the existence of the controlled adjoint specialization is inferred.</span></span> <span data-ttu-id="9718a-252">Se nenhuma implementação for definida explicitamente, a compilação gerará uma especialização apropriada.</span><span class="sxs-lookup"><span data-stu-id="9718a-252">If no implementation is explicitly defined, the compile generates an appropriate specialization.</span></span>

<span data-ttu-id="9718a-253">Para uma operação cujo corpo contém chamadas para outras operações que não têm uma versão adjacente controlada, a geração automática de uma especialização de adjacente após a `invert` `distribute` diretiva, ou `auto` não é possível.</span><span class="sxs-lookup"><span data-stu-id="9718a-253">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute`, or `auto` directive is not possible.</span></span>


### <a name="type-compatibility"></a><span data-ttu-id="9718a-254">Compatibilidade de tipo</span><span class="sxs-lookup"><span data-stu-id="9718a-254">Type Compatibility</span></span>

<span data-ttu-id="9718a-255">Use uma operação com transmissão functors adicionais com suporte em qualquer lugar em que você use uma operação com menos transmissão functors, mas a mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="9718a-255">Use an operation with additional functors supported anywhere you use an operation with fewer functors but the same signature.</span></span> <span data-ttu-id="9718a-256">Por exemplo, use uma operação do tipo `(Qubit => Unit is Adj)` em qualquer lugar em que você use uma operação do tipo `(Qubit => Unit)` .</span><span class="sxs-lookup"><span data-stu-id="9718a-256">For instance, use an operation of type `(Qubit => Unit is Adj)` anywhere you use an operation of type `(Qubit => Unit)`.</span></span>

<span data-ttu-id="9718a-257">Q # é *covariant* com relação a tipos de retorno que podem ser chamados: um callable que retorna um tipo `'A` é compatível com um callable com o mesmo tipo de entrada e um tipo de resultado compatível com `'A` .</span><span class="sxs-lookup"><span data-stu-id="9718a-257">Q# is *covariant* with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that is compatible with `'A` .</span></span>

<span data-ttu-id="9718a-258">Q # é *contravariant* em relação aos tipos de entrada: um callable que usa um tipo `'A` como entrada é compatível com um callable com o mesmo tipo de resultado e um tipo de entrada compatível com `'A` .</span><span class="sxs-lookup"><span data-stu-id="9718a-258">Q# is *contravariant* with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="9718a-259">Ou seja, dadas as definições a seguir,</span><span class="sxs-lookup"><span data-stu-id="9718a-259">That is, given the following definitions,</span></span>

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="9718a-260">É possível</span><span class="sxs-lookup"><span data-stu-id="9718a-260">you can</span></span>

- <span data-ttu-id="9718a-261">Invoque a função `ConjugateInvertWith` com um `inner` argumento de `Invert` ou `ApplyUnitary` .</span><span class="sxs-lookup"><span data-stu-id="9718a-261">Invoke the function `ConjugateInvertWith` with an `inner` argument of either `Invert` or `ApplyUnitary`.</span></span>
- <span data-ttu-id="9718a-262">Invocar a função `ConjugateUnitaryWith` com um `inner` argumento de `ApplyUnitary` , mas não `Invert` .</span><span class="sxs-lookup"><span data-stu-id="9718a-262">Invoke the function `ConjugateUnitaryWith` with an `inner` argument of `ApplyUnitary`, but not `Invert`.</span></span>
- <span data-ttu-id="9718a-263">Retornar um valor do tipo `(Qubit[] => Unit is Adj + Ctl)` de `ConjugateInvertWith` .</span><span class="sxs-lookup"><span data-stu-id="9718a-263">Return a value of type `(Qubit[] => Unit is Adj + Ctl)` from `ConjugateInvertWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9718a-264">A p # 0,3 introduziu uma diferença significativa no comportamento de tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9718a-264">Q# 0.3 introduced a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="9718a-265">Os tipos definidos pelo usuário são tratados como uma versão encapsulada do tipo subjacente, em vez de como um subtipo.</span><span class="sxs-lookup"><span data-stu-id="9718a-265">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="9718a-266">Isso significa que um valor de um tipo definido pelo usuário não é utilizável em que você espera que um valor do tipo subjacente seja.</span><span class="sxs-lookup"><span data-stu-id="9718a-266">This means that a value of a user-defined type is not usable where you expect a value of the underlying type is.</span></span>


### <a name="conjugations"></a><span data-ttu-id="9718a-267">Conjugações</span><span class="sxs-lookup"><span data-stu-id="9718a-267">Conjugations</span></span>

<span data-ttu-id="9718a-268">Em contraste com os bits clássicos, liberar memória Quantum é um pouco mais envolvida, uma vez que a redefinição oculta de qubits pode ter efeitos indesejados na computação restante se o qubits ainda for confusas.</span><span class="sxs-lookup"><span data-stu-id="9718a-268">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="9718a-269">Esses efeitos podem ser evitados de forma adequada "desfazer" as computações realizadas antes de liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="9718a-269">These effects can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="9718a-270">Um padrão comum na computação Quantum é, portanto, o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9718a-270">A common pattern in quantum computing is hence the following:</span></span> 

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

<span data-ttu-id="9718a-271">A partir da nossa versão 0,9, o Q # dá suporte a uma instrução Conjugation que implementa a transformação anterior.</span><span class="sxs-lookup"><span data-stu-id="9718a-271">Starting with our 0.9 release, Q# supports a conjugation statement that implements the preceding transformation.</span></span> <span data-ttu-id="9718a-272">Usando essa instrução, a operação `ApplyWith` pode ser implementada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9718a-272">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

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
<span data-ttu-id="9718a-273">Essa instrução de conjugação se torna muito mais útil se as transformações externas e internas não estão prontamente disponíveis como operações, mas são mais convenientes de descrever por um bloco consistindo em várias instruções.</span><span class="sxs-lookup"><span data-stu-id="9718a-273">Such a conjugation statement becomes far more useful if the outer and inner transformations are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="9718a-274">A transformação inversa para as instruções definidas no bloco Within é gerada automaticamente pelo compilador e executada após a conclusão do bloco de aplicação.</span><span class="sxs-lookup"><span data-stu-id="9718a-274">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and run after the apply-block completes.</span></span>
<span data-ttu-id="9718a-275">Como as variáveis mutáveis usadas como parte do bloco Within não podem ser reassociadas no bloco Apply, a transformação gerada é garantida como sendo a adjoin do cálculo no bloco Within.</span><span class="sxs-lookup"><span data-stu-id="9718a-275">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 


## <a name="defining-new-functions"></a><span data-ttu-id="9718a-276">Definindo novas funções</span><span class="sxs-lookup"><span data-stu-id="9718a-276">Defining New Functions</span></span>

<span data-ttu-id="9718a-277">As funções são puramente determinísticas, rotinas clássicas em Q #, que são diferentes das operações, pois elas não têm permissão para ter nenhum efeito além de calcular um valor de saída.</span><span class="sxs-lookup"><span data-stu-id="9718a-277">Functions are purely deterministic, classical routines in Q#, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="9718a-278">Em particular, as funções não podem chamar operações; agir sobre, alocar ou emprestar qubits; números aleatórios de exemplo; ou, de outra forma, dependem do estado após o valor de entrada para uma função.</span><span class="sxs-lookup"><span data-stu-id="9718a-278">In particular, functions cannot call operations; act on, allocate, or borrow qubits; sample random numbers; or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="9718a-279">Como consequência, as funções Q # são *puras*, pois elas sempre mapeiam os mesmos valores de entrada para os mesmos valores de saída.</span><span class="sxs-lookup"><span data-stu-id="9718a-279">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="9718a-280">Esse comportamento permite que o compilador Q # reordene com segurança como e quando chamar funções ao gerar especializações de operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-280">This behavior allows the Q# compiler to safely reorder how and when to call functions when generating operation specializations.</span></span>

<span data-ttu-id="9718a-281">Cada arquivo de origem Q # pode definir qualquer número de funções.</span><span class="sxs-lookup"><span data-stu-id="9718a-281">Each Q# source file can define any number of functions.</span></span>
<span data-ttu-id="9718a-282">Os nomes de função devem ser exclusivos em um namespace e não podem entrar em conflito com os nomes de operação ou tipo.</span><span class="sxs-lookup"><span data-stu-id="9718a-282">Function names must be unique within a namespace and cannot conflict with operation or type names.</span></span>

<span data-ttu-id="9718a-283">A definição de uma função funciona de forma semelhante à definição de uma operação, exceto que nenhuma especialização adjacente ou controlada pode ser definida para uma função.</span><span class="sxs-lookup"><span data-stu-id="9718a-283">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="9718a-284">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9718a-284">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

<span data-ttu-id="9718a-285">ou</span><span class="sxs-lookup"><span data-stu-id="9718a-285">or</span></span> 

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```

### <a name="classical-logic-in-functions--good"></a><span data-ttu-id="9718a-286">Lógica clássica em funções = = bom</span><span class="sxs-lookup"><span data-stu-id="9718a-286">Classical logic in functions == good</span></span>

<span data-ttu-id="9718a-287">Sempre que for possível fazer isso, é útil escrever a lógica clássica em termos de funções em vez de operações para que as operações possam usá-las mais prontamente.</span><span class="sxs-lookup"><span data-stu-id="9718a-287">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations so that operations can more readily use it.</span></span> <span data-ttu-id="9718a-288">Por exemplo, se você tivesse escrito a `Square` declaração anterior como uma *operação*, o compilador não teria conseguido garantir que chamá-la com a mesma entrada produzirá consistentemente as mesmas saídas.</span><span class="sxs-lookup"><span data-stu-id="9718a-288">For example, if you had written the earlier `Square` declaration as an *operation*, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="9718a-289">Para enfatizar a diferença entre funções e operações, considere o problema de amostragem clássica de um número aleatório de dentro de uma operação Q #:</span><span class="sxs-lookup"><span data-stu-id="9718a-289">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="9718a-290">Cada vez que `U` é chamado, ele tem uma ação diferente em `target` .</span><span class="sxs-lookup"><span data-stu-id="9718a-290">Each time that `U` is called, it has a different action on `target`.</span></span>
<span data-ttu-id="9718a-291">Em particular, o compilador não pode garantir que, se você adicionar uma `adjoint auto` declaração de especialização a `U` , `U(target); Adjoint U(target);` atue como identidade (ou seja, como não operacional).</span><span class="sxs-lookup"><span data-stu-id="9718a-291">In particular, the compiler cannot guarantee that if you add an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="9718a-292">Isso viola a definição do adjoin definido em [vetores e matrizes](xref:microsoft.quantum.concepts.vectors), de modo que permitir que o compilador gere automaticamente uma especialização adjacente em uma operação na qual você chama a operação <xref:microsoft.quantum.math.randomreal> interromperia as garantias fornecidas pelo compilador; <xref:microsoft.quantum.math.randomreal> é uma operação para a qual não existe nenhuma versão adjacente ou controlada.</span><span class="sxs-lookup"><span data-stu-id="9718a-292">This violates the definition of the adjoint defined in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing the compiler to auto-generate an adjoint specialization in an operation where you call the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="9718a-293">Por outro lado, permitir que chamadas de função, como `Square` é seguro, e garante ao compilador que ele só precisa preservar a entrada para `Square` manter sua saída estável.</span><span class="sxs-lookup"><span data-stu-id="9718a-293">On the other hand, allowing function calls such as `Square` is safe, and assures the compiler that it only needs to preserve the input to `Square` to keep its output stable.</span></span>
<span data-ttu-id="9718a-294">Portanto, isolar o máximo de lógica clássica possível em funções facilita a reutilização dessa lógica em outras funções e operações semelhantes.</span><span class="sxs-lookup"><span data-stu-id="9718a-294">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>


## <a name="generic-type-parameterized-callables"></a><span data-ttu-id="9718a-295">Chamadores genéricos (com parâmetros de tipo)</span><span class="sxs-lookup"><span data-stu-id="9718a-295">Generic (Type-Parameterized) Callables</span></span>

<span data-ttu-id="9718a-296">Muitas funções e operações que você talvez queira definir não dependem muito dos tipos de suas entradas, mas, em vez disso, apenas usam implicitamente seus tipos por meio de alguma outra função ou operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-296">Many functions and operations that you might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="9718a-297">Por exemplo, considere o conceito de *mapa* comum a muitas linguagens funcionais; dada uma função $f (x) $ e uma coleção de valores $ \{ x_1, x_2, \dots, x_n \} $, MAP retorna uma nova coleção $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $.</span><span class="sxs-lookup"><span data-stu-id="9718a-297">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="9718a-298">Para implementar isso em Q #, aproveite o fato de que as funções são a primeira classe.</span><span class="sxs-lookup"><span data-stu-id="9718a-298">To implement this in Q#, take advantage of the fact that functions are first class.</span></span>
<span data-ttu-id="9718a-299">Aqui está um exemplo rápido de `Map` , usando `T` como um espaço reservado enquanto você descobrir quais tipos são necessários.</span><span class="sxs-lookup"><span data-stu-id="9718a-299">Here is a quick example of `Map`, using `T` as a placeholder while you figure out what types you need.</span></span>

```qsharp
function Map(fn : (T -> T), values : T[]) : T[] {
    mutable mappedValues = new T[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="9718a-300">Observe que essa função parece muito semelhante, independentemente de quais tipos reais você substitui.</span><span class="sxs-lookup"><span data-stu-id="9718a-300">Note that this function looks very much the same no matter what actual types you substitute in.</span></span>
<span data-ttu-id="9718a-301">Um mapa de inteiros para Paulis, por exemplo, parece muito o mesmo que um mapa de números de ponto flutuante para cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="9718a-301">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

```qsharp
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="9718a-302">Em princípio, você poderia escrever uma versão do `Map` para cada par de tipos que encontrar, mas isso apresenta várias dificuldades.</span><span class="sxs-lookup"><span data-stu-id="9718a-302">In principle, you could write a version of `Map` for every pair of types that you encounter, but this introduces several difficulties.</span></span>
<span data-ttu-id="9718a-303">Por exemplo, se você encontrar um bug no `Map` , deverá garantir que a correção seja aplicada uniformemente em todas as versões do `Map` .</span><span class="sxs-lookup"><span data-stu-id="9718a-303">For instance, if you find a bug in `Map`, then you must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="9718a-304">Além disso, se você construir uma nova tupla ou UDT, agora você também deve construir um novo `Map` para ir junto com o novo tipo.</span><span class="sxs-lookup"><span data-stu-id="9718a-304">Moreover, if you construct a new tuple or UDT, then you must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="9718a-305">Embora isso seja indesejado para um pequeno número dessas funções, à medida que você coleta cada vez mais funções da mesma forma que `Map` , o custo da introdução de novos tipos torna-se razoavelmente grande em ordem razoavelmente curta.</span><span class="sxs-lookup"><span data-stu-id="9718a-305">While this is tractable for a small number of such functions, as you collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="9718a-306">No entanto, grande parte dessa dificuldade resulta do fato de que você não deu ao compilador as informações de que ele precisa para reconhecer como as diferentes versões do `Map` estão relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9718a-306">However, much of this difficulty results from the fact that you have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="9718a-307">Efetivamente, você deseja que o compilador trate `Map` como algum tipo de função matemática de *tipos* q # para funções q #.</span><span class="sxs-lookup"><span data-stu-id="9718a-307">Effectively, you want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>

<span data-ttu-id="9718a-308">P # formalizes essa noção, permitindo que funções e operações tenham *parâmetros de tipo*, bem como seus parâmetros de tupla comuns.</span><span class="sxs-lookup"><span data-stu-id="9718a-308">Q# formalizes this notion by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="9718a-309">Nos exemplos anteriores, você deseja considerar `Map` como tendo parâmetros de tipo `Int, Pauli` no primeiro caso e `Double, String` no segundo caso.</span><span class="sxs-lookup"><span data-stu-id="9718a-309">In the previous examples, you wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="9718a-310">Para a maior parte, use esses parâmetros de tipo como se fossem tipos comuns.</span><span class="sxs-lookup"><span data-stu-id="9718a-310">For the most part, use these type parameters as though they were ordinary types.</span></span> <span data-ttu-id="9718a-311">Use valores de parâmetros de tipo para criar matrizes e tuplas, chamar funções e operações e atribuir a variáveis comuns ou mutáveis.</span><span class="sxs-lookup"><span data-stu-id="9718a-311">Use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="9718a-312">O caso mais extremo de dependência indireta é o de qubits, em que um programa Q # não pode depender diretamente da estrutura do `Qubit` tipo, mas **deve** passar esses tipos para outras operações e funções.</span><span class="sxs-lookup"><span data-stu-id="9718a-312">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="9718a-313">Retornando ao exemplo anterior, você vê que `Map` precisa ter parâmetros de tipo, um para representar a entrada para `fn` e um para representar a saída de `fn` .</span><span class="sxs-lookup"><span data-stu-id="9718a-313">Returning to the earlier example, then, you see that `Map` needs to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="9718a-314">Em Q #, isso é escrito pela adição de colchetes angulares (ou seja `<>` , não brakets $ \braket {} $!) após o nome de uma função ou operação em sua declaração e listando cada parâmetro de tipo.</span><span class="sxs-lookup"><span data-stu-id="9718a-314">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="9718a-315">O nome de cada parâmetro de tipo deve começar com um tique `'` , indicando que ele é um parâmetro de tipo e não um tipo comum (também conhecido como um tipo *concreto* ).</span><span class="sxs-lookup"><span data-stu-id="9718a-315">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="9718a-316">Portanto, `Map` , é escrito:</span><span class="sxs-lookup"><span data-stu-id="9718a-316">Thus, `Map`, is written:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="9718a-317">Observe que a definição de `Map<'Input, 'Output>` parece extremamente semelhante às versões do previoius.</span><span class="sxs-lookup"><span data-stu-id="9718a-317">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the previoius versions.</span></span>
<span data-ttu-id="9718a-318">A única diferença é que você informou explicitamente o compilador que `Map` não depende diretamente do que `'Input` e `'Output` são, mas funciona para dois tipos usando-os indiretamente por meio de `fn` .</span><span class="sxs-lookup"><span data-stu-id="9718a-318">The only difference is that you have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="9718a-319">Depois de definido `Map<'Input, 'Output>` dessa forma, você pode chamá-lo como se fosse uma função comum:</span><span class="sxs-lookup"><span data-stu-id="9718a-319">Once you have defined `Map<'Input, 'Output>` in this way, you can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="9718a-320">Escrever funções e operações genéricas é um lugar em que "tupla-in-out" é uma maneira muito útil de pensar em funções e operações do Q #.</span><span class="sxs-lookup"><span data-stu-id="9718a-320">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="9718a-321">Como cada função usa exatamente uma entrada e retorna exatamente uma saída, uma entrada do tipo `'T -> 'U` corresponde a *qualquer* função Q # qualquer.</span><span class="sxs-lookup"><span data-stu-id="9718a-321">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="9718a-322">Da mesma forma, você pode passar qualquer operação para uma entrada do tipo `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="9718a-322">Similarly, you can pass any operation to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="9718a-323">Como um segundo exemplo, considere o desafio de escrever uma função que retorne a composição de duas outras funções:</span><span class="sxs-lookup"><span data-stu-id="9718a-323">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="9718a-324">Aqui, você deve especificar exatamente o que `A` , `B` e `C` estão, limitando seriamente o utilitário de nossa nova `Compose` função.</span><span class="sxs-lookup"><span data-stu-id="9718a-324">Here, you must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="9718a-325">Afinal, `Compose` só depende de `A` , `B` e `C` *através* `innerFn` de e `outerFn` .</span><span class="sxs-lookup"><span data-stu-id="9718a-325">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="9718a-326">Como alternativa, você pode adicionar parâmetros de tipo ao `Compose` que indicam que ele funciona para *qualquer* `A` , `B` e `C` , desde que esses parâmetros correspondam aos esperados por `innerFn` e `outerFn` :</span><span class="sxs-lookup"><span data-stu-id="9718a-326">As an alternative, then, you can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="9718a-327">As bibliotecas padrão de Q # fornecem uma variedade de operações e funções parametrizadas por tipo para facilitar o expressar o fluxo de controle de ordem mais alta.</span><span class="sxs-lookup"><span data-stu-id="9718a-327">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="9718a-328">Eles são abordados mais detalhadamente no [Guia de biblioteca padrão do Q #](xref:microsoft.quantum.libraries.standard.intro).</span><span class="sxs-lookup"><span data-stu-id="9718a-328">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>


## <a name="callables-as-first-class-values"></a><span data-ttu-id="9718a-329">É chamado como valores de primeira classe</span><span class="sxs-lookup"><span data-stu-id="9718a-329">Callables as First-Class Values</span></span>

<span data-ttu-id="9718a-330">Uma técnica crítica para o raciocínio sobre o fluxo de controle e a lógica clássica usando funções em vez de operações é utilizar essas operações e funções em Q # são de *primeira classe*.</span><span class="sxs-lookup"><span data-stu-id="9718a-330">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="9718a-331">Ou seja, eles são cada um dos valores no idioma que estão no seu próprio direito.</span><span class="sxs-lookup"><span data-stu-id="9718a-331">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="9718a-332">Por exemplo, este é um código Q # perfeitamente válido, se um pouco indireto:</span><span class="sxs-lookup"><span data-stu-id="9718a-332">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="9718a-333">O valor da variável `ourH` no trecho anterior é, então, a operação <xref:microsoft.quantum.intrinsic.h> , de modo que você pode chamar esse valor como qualquer outra operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-333">The value of the variable `ourH` in the previous snippet is then the operation <xref:microsoft.quantum.intrinsic.h>, such that you can call that value like any other operation.</span></span>
<span data-ttu-id="9718a-334">Com essa capacidade, você pode gravar operações que usam operações como parte de sua entrada, formando conceitos de fluxo de controle de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="9718a-334">With this ability, you can write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="9718a-335">Por exemplo, você pode imaginar que queira "quadrado" uma operação aplicando-a duas vezes ao mesmo qubit de destino.</span><span class="sxs-lookup"><span data-stu-id="9718a-335">For instance, you could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a><span data-ttu-id="9718a-336">Retornando operações de uma função</span><span class="sxs-lookup"><span data-stu-id="9718a-336">Returning operations from a function</span></span>

<span data-ttu-id="9718a-337">É importante enfatizar que você também pode retornar operações como parte das saídas, de modo que você pode isolar alguns tipos de lógica condicional clássica como uma função clássica, que retorna uma descrição de um programa Quantum na forma de uma operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-337">It's important to emphasize that you can also return operations as a part of outputs, such that you can isolate some kinds of classical conditional logic as a classical function, which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="9718a-338">Como exemplo simples, considere o exemplo de teleportação, no qual a parte que recebe uma mensagem clássica de dois bits precisa usar a mensagem para decodificar seu qubit no estado de Teleporta adequado.</span><span class="sxs-lookup"><span data-stu-id="9718a-338">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="9718a-339">Você poderia escrever isso em termos de uma função que usa esses dois bits clássicos e retorna a operação de decodificação apropriada.</span><span class="sxs-lookup"><span data-stu-id="9718a-339">You could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

<span data-ttu-id="9718a-340">Essa nova função é realmente uma função, se você chamá-la com os mesmos valores de `hereBit` e `thereBit` , sempre obterá a mesma operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-340">This new function is indeed a function, in that if you call it with the same values of `hereBit` and `thereBit`, you always get back the same operation.</span></span>
<span data-ttu-id="9718a-341">Assim, o decodificador pode ser executado com segurança dentro de operações sem ter que ter em razão de como a lógica de decodificação interage com as definições das diferentes especializações de operação.</span><span class="sxs-lookup"><span data-stu-id="9718a-341">Thus, the decoder can safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="9718a-342">Ou seja, a lógica clássica dentro de uma função é isolada, garantindo ao compilador que a chamada de função pode ser reordenada com impunity, desde que a entrada seja preservada.</span><span class="sxs-lookup"><span data-stu-id="9718a-342">That is, the classical logic inside a function is isolated, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>


## <a name="partial-application"></a><span data-ttu-id="9718a-343">Aplicativo parcial</span><span class="sxs-lookup"><span data-stu-id="9718a-343">Partial Application</span></span>

<span data-ttu-id="9718a-344">Você pode fazer significativamente mais com funções que retornam operações usando o *aplicativo parcial*, no qual você fornece uma ou mais partes da entrada para uma função ou operação sem realmente chamá-la.</span><span class="sxs-lookup"><span data-stu-id="9718a-344">You can do significantly more with functions that return operations by using *partial application*, in which you provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="9718a-345">No exemplo anterior `ApplyTwice` , você pode indicar que não deseja especificar, imediatamente, a qual qubit a operação de entrada deve ser aplicada:</span><span class="sxs-lookup"><span data-stu-id="9718a-345">In the earlier `ApplyTwice` example, you can indicate that you don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="9718a-346">Nesse caso, a variável local `twiceOp` contém a operação parcialmente aplicada `ApplyTwice(op, _)` , em que `_` indica partes da entrada que ainda não foram especificadas.</span><span class="sxs-lookup"><span data-stu-id="9718a-346">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where `_` indicates parts of the input that have not yet been specified.</span></span>
<span data-ttu-id="9718a-347">Quando você chama `twiceOp` na próxima linha, passa como entrada para a operação parcialmente aplicada todas as partes restantes da entrada para a operação original.</span><span class="sxs-lookup"><span data-stu-id="9718a-347">When you call `twiceOp` in the next line, you pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="9718a-348">Assim, o trecho anterior é efetivamente idêntico a ter chamado `ApplyTwice(op, target)` diretamente, salvar para que você tenha introduzido uma nova variável local para que possa atrasar a chamada enquanto fornece algumas partes da entrada.</span><span class="sxs-lookup"><span data-stu-id="9718a-348">Thus, the previous snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that you have introduced a new local variable so you can delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="9718a-349">Como uma operação que foi parcialmente aplicada não é realmente chamada até que toda a sua entrada tenha sido fornecida, você pode aplicar operações parcialmente de forma segura, mesmo a partir de funções.</span><span class="sxs-lookup"><span data-stu-id="9718a-349">Since an operation that has been partially applied is not actually called until its entire input has been provided, you can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="9718a-350">Em princípio, a lógica clássica dentro `SquareOperation` poderia ter sido muito mais envolvida, mas ainda é isolada do restante de uma operação pelas garantias que o compilador pode oferecer sobre as funções.</span><span class="sxs-lookup"><span data-stu-id="9718a-350">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span> <span data-ttu-id="9718a-351">A biblioteca padrão Q # usa essa abordagem para expressar o fluxo de controle clássico de forma que os programas Quantum possam ser usados prontamente.</span><span class="sxs-lookup"><span data-stu-id="9718a-351">The Q# standard library uses this approach throughout for expressing classical control flow in a way that quantum programs can readily use.</span></span>


## <a name="recursion"></a><span data-ttu-id="9718a-352">Recursão</span><span class="sxs-lookup"><span data-stu-id="9718a-352">Recursion</span></span>

<span data-ttu-id="9718a-353">Os chamadores do Q # podem ser recursivos direta ou indiretamente.</span><span class="sxs-lookup"><span data-stu-id="9718a-353">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="9718a-354">Ou seja, uma operação ou função pode chamar a si mesma ou chamar outro callable que chama direta ou indiretamente a operação que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="9718a-354">That is, an operation or function can call itself, or it can call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="9718a-355">No entanto, há dois comentários importantes sobre o uso da recursão:</span><span class="sxs-lookup"><span data-stu-id="9718a-355">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="9718a-356">O uso da recursão nas operações provavelmente interfere em determinadas otimizações.</span><span class="sxs-lookup"><span data-stu-id="9718a-356">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="9718a-357">Essa interferência pode ter um impacto significativo no tempo de execução do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="9718a-357">This interference can have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="9718a-358">Durante a execução em um dispositivo Quantum real, o espaço de pilha pode ser limitado e, portanto, a recursão profunda pode levar a um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="9718a-358">When running on an actual quantum device, stack space might be limited, and so deep recursion can lead to a runtime error.</span></span>
  <span data-ttu-id="9718a-359">Em particular, o compilador e o tempo de execução do Q # não identificam e otimizam a recursão da cauda.</span><span class="sxs-lookup"><span data-stu-id="9718a-359">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9718a-360">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9718a-360">Next steps</span></span>

<span data-ttu-id="9718a-361">Saiba mais sobre [variáveis](xref:microsoft.quantum.guide.variables) em Q #.</span><span class="sxs-lookup"><span data-stu-id="9718a-361">Learn about [Variables](xref:microsoft.quantum.guide.variables) in Q#.</span></span>