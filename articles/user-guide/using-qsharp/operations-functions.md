---
title: 'Operações e funções em p #'
description: Como definir e chamar operações e funções, bem como as especializações de operação controladas e adjacentes.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
ms.openlocfilehash: bc9695b85b68807801225ccbc903a4622b450768
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431063"
---
# <a name="operations-and-functions-in-q"></a><span data-ttu-id="d2d52-103">Operações e funções em p #</span><span class="sxs-lookup"><span data-stu-id="d2d52-103">Operations and Functions in Q#</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="d2d52-104">Definindo novas operações</span><span class="sxs-lookup"><span data-stu-id="d2d52-104">Defining New Operations</span></span>

<span data-ttu-id="d2d52-105">As operações são o núcleo de Q #.</span><span class="sxs-lookup"><span data-stu-id="d2d52-105">Operations are the core of Q#.</span></span>
<span data-ttu-id="d2d52-106">Depois de declarados, eles podem ser chamados a partir de aplicativos .NET clássicos, por exemplo, usando um simulador ou por outras operações em Q #.</span><span class="sxs-lookup"><span data-stu-id="d2d52-106">Once declared, they can either be called from classical .NET applications, e.g., using a simulator, or by other operations within Q#.</span></span>
<span data-ttu-id="d2d52-107">Cada operação definida em Q # pode então chamar qualquer número de outras operações, incluindo as operações intrínsecas internas definidas pelo idioma.</span><span class="sxs-lookup"><span data-stu-id="d2d52-107">Each operation defined in Q# may then call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="d2d52-108">A maneira específica em que essas operações intrínsecas são definidas depende da máquina de destino.</span><span class="sxs-lookup"><span data-stu-id="d2d52-108">The particular way in which these intrinsic operations are defined depends on the target machine.</span></span>
<span data-ttu-id="d2d52-109">Quando compilada, cada operação é representada como um tipo de classe do .NET que pode ser fornecido para os computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="d2d52-109">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

<span data-ttu-id="d2d52-110">Cada arquivo de origem Q # pode definir qualquer número de operações.</span><span class="sxs-lookup"><span data-stu-id="d2d52-110">Each Q# source file may define any number of operations.</span></span>
<span data-ttu-id="d2d52-111">Os nomes de operação devem ser exclusivos em um namespace e podem não entrar em conflito com os nomes de tipo ou função.</span><span class="sxs-lookup"><span data-stu-id="d2d52-111">Operation names must be unique within a namespace and may not conflict with type or function names.</span></span>

<span data-ttu-id="d2d52-112">Uma declaração de operação consiste na palavra-chave `operation` , seguida pelo símbolo que é o nome da operação, uma tupla de identificador tipada que define os argumentos para a operação, dois-pontos `:` , uma anotação de tipo que descreve o tipo de resultado da operação, opcionalmente uma anotação com as características da operação, uma chave `{` de abertura, o corpo da declaração da operação e uma chave de fechamento final `}` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-112">An operation declaration consists of the keyword `operation`, followed by the symbol that is the operation's name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation's result type, optionally an annotation with the operation characteristics, an open brace `{`, the body of the operation declaration, and a final closing brace `}`.</span></span>

<span data-ttu-id="d2d52-113">Cada operação usa uma entrada, produz uma saída e especifica a implementação para uma ou mais especializações de operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-113">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="d2d52-114">As especializações possíveis e como defini-las e chamá-las são detalhadas mais adiante.</span><span class="sxs-lookup"><span data-stu-id="d2d52-114">The possible specializations, and how to define/call them, are detailed further below.</span></span>
<span data-ttu-id="d2d52-115">Por enquanto, considere a seguinte operação, que define apenas uma especialização de corpo padrão e usa um único qubit como sua entrada e, em seguida, chama a <xref:microsoft.quantum.intrinsic.x> operação interna nessa entrada:</span><span class="sxs-lookup"><span data-stu-id="d2d52-115">For now, consider the following operation, which defines only a default body specialization and takes a single qubit as its input, then calls the built-in <xref:microsoft.quantum.intrinsic.x> operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="d2d52-116">A palavra-chave `operation` começa a definição da operação e é seguida pelo nome; aqui, `BitFlip` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-116">The keyword `operation` begins the operation definition, and is followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="d2d52-117">Em seguida, o tipo da entrada é definido como `Qubit` , junto com um nome `target` para fazer referência à entrada dentro da nova operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-117">Next, the type of the input is defined as `Qubit`, along with a name `target` for referring to the input within the new operation.</span></span>
<span data-ttu-id="d2d52-118">Da mesma forma, o `Unit` define que a saída da operação está vazia.</span><span class="sxs-lookup"><span data-stu-id="d2d52-118">Similarly, the `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="d2d52-119">Isso é usado da mesma forma `void` no C# e em outras linguagens imperativas e é equivalente a `unit` em F # e a outras linguagens funcionais.</span><span class="sxs-lookup"><span data-stu-id="d2d52-119">This is used similarly to `void` in C# and other imperative languages, and is equivalent to `unit` in F# and other functional languages.</span></span>

<span data-ttu-id="d2d52-120">As operações também podem retornar tipos mais interessantes do que `Unit` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-120">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="d2d52-121">Por exemplo, a <xref:microsoft.quantum.intrinsic.m> operação retorna uma saída do tipo `Result` , representando tendo realizado uma medição.</span><span class="sxs-lookup"><span data-stu-id="d2d52-121">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span> <span data-ttu-id="d2d52-122">Podemos passar a saída de uma operação para outra operação ou pode usá-la com a `let` palavra-chave para definir uma nova variável.</span><span class="sxs-lookup"><span data-stu-id="d2d52-122">We can either pass the output from an operation to another operation, or can use it with the `let` keyword to define a new variable.</span></span>

<span data-ttu-id="d2d52-123">Isso permite representar a computação clássica que interage com as operações Quantum em um nível baixo, como na [codificação superdensa](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span><span class="sxs-lookup"><span data-stu-id="d2d52-123">This allows for representing classical computation that interacts with quantum operations at a low level, such as in [superdense coding](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span></span>

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
> <span data-ttu-id="d2d52-124">Cada operação em Q # usa exatamente uma entrada e retorna exatamente uma saída.</span><span class="sxs-lookup"><span data-stu-id="d2d52-124">Each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="d2d52-125">Várias entradas e saídas são representadas usando *tuplas*, que coletam vários valores juntos em um único valor.</span><span class="sxs-lookup"><span data-stu-id="d2d52-125">Multiple inputs and outputs are then represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="d2d52-126">Informalmente, dizemos que Q # é uma linguagem de "tupla na tupla".</span><span class="sxs-lookup"><span data-stu-id="d2d52-126">Informally, we say that Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="d2d52-127">Após esse conceito, `()` deve ser lido como a tupla "vazia", que tem o tipo `Unit` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-127">Following this concept, `()` should then be read as the "empty" tuple, which has the type `Unit`.</span></span>


## <a name="controlled-and-adjoint-operations"></a><span data-ttu-id="d2d52-128">Operações controladas e adjacentes</span><span class="sxs-lookup"><span data-stu-id="d2d52-128">Controlled and Adjoint Operations</span></span>

<span data-ttu-id="d2d52-129">Se uma operação implementa uma transformação unitário, como é o caso de muitas operações em Q #, é possível definir como a operação age quando *adjointed* ou *controlada*.</span><span class="sxs-lookup"><span data-stu-id="d2d52-129">If an operation implements a unitary transformation, as is the case for many operations in Q#, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="d2d52-130">Uma especialização *adjacente* de uma operação especifica como o "inverso" da operação age, enquanto uma especialização *controlada* especifica como uma operação age quando seu aplicativo é condicionado no estado de um registro de Quantum específico.</span><span class="sxs-lookup"><span data-stu-id="d2d52-130">An *adjoint* specialization of an operation specifies how the "inverse" of the operation acts, while a *controlled* specialization specifies how an operation acts when its application is conditioned on the state of a particular quantum register.</span></span>

<span data-ttu-id="d2d52-131">Adjoints de operações Quantum são cruciais para muitos aspectos da computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="d2d52-131">Adjoints of quantum operations are crucial to many aspects of quantum computing.</span></span> <span data-ttu-id="d2d52-132">Além disso, na seção [conjugados](#conjugations) , você encontrará uma dessas situações discutida junto com uma técnica útil de programação de Q #.</span><span class="sxs-lookup"><span data-stu-id="d2d52-132">Further below, in the [Conjugations](#conjugations) section, you will find one such situation discussed alongside a useful Q# programming technique.</span></span>

<span data-ttu-id="d2d52-133">A versão controlada de uma operação é uma nova operação que aplica efetivamente a operação base somente se todas as qubits de controle estiverem em um estado especificado.</span><span class="sxs-lookup"><span data-stu-id="d2d52-133">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="d2d52-134">Se o controle qubits estiver em superposição, a operação base será aplicada coerentemente à parte apropriada da superposição.</span><span class="sxs-lookup"><span data-stu-id="d2d52-134">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="d2d52-135">Portanto, as operações controladas geralmente são usadas para gerar Entanglement.</span><span class="sxs-lookup"><span data-stu-id="d2d52-135">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="d2d52-136">Naturalmente, uma especialização *adjacente controlada* poderia existir também, especificando o aplicativo controlado de um adjacente de uma operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-136">Naturally, a *controlled adjoint* specialization could exist as well, specifying the controlled application of an operation's adjoint.</span></span>

> [!NOTE]
> <span data-ttu-id="d2d52-137">Se $U $ for a transformação unitário implementada por uma operação `U` , `Adjoint U` o representará a transformação unitário $U ^ \dagger $, que é a transpoção conjugada complexa.</span><span class="sxs-lookup"><span data-stu-id="d2d52-137">If $U$ is the unitary transformation implemented by an operation `U`, then `Adjoint U` represents the unitary transformation $U^\dagger$, which is the complex conjugate transpose.</span></span>
> <span data-ttu-id="d2d52-138">Aplicar sucessivamente uma operação e, em seguida, seu adjacente a um estado deixa o estado inalterado, conforme ilustrado pelo fato de que $UU ^ \dagger = U ^ \dagger U = \id $, a matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="d2d52-138">Successively applying an operation and then its adjoint to a state leaves the state unchanged, as illustrated by the fact that $UU^\dagger = U^\dagger U = \id$, the identity matrix.</span></span>
> <span data-ttu-id="d2d52-139">A representação unitário de uma operação controlada é ligeiramente mais nuance, mas você pode encontrar mais detalhes em [conceitos de computação Quantum: vários qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span><span class="sxs-lookup"><span data-stu-id="d2d52-139">The unitary representation of a controlled operation is slightly more nuanced, but you can find more details at [Quantum computing concepts: multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

<span data-ttu-id="d2d52-140">A seção a seguir descreve como chamar essas várias especializações no código Q #.</span><span class="sxs-lookup"><span data-stu-id="d2d52-140">The following section describes how to call these various specializations in your Q# code.</span></span>
<span data-ttu-id="d2d52-141">Abaixo, detalhamos como definir operações para dar suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="d2d52-141">Below, we detail how to define operations to support them.</span></span>

### <a name="calling-operation-specializations"></a><span data-ttu-id="d2d52-142">Chamando especializações de operação</span><span class="sxs-lookup"><span data-stu-id="d2d52-142">Calling operation specializations</span></span>

<span data-ttu-id="d2d52-143">Um *functor* em Q # é um alocador que define uma nova operação de outra operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-143">A *functor* in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="d2d52-144">Os dois transmissão functors padrão em Q # são `Adjoint` e `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-144">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

<span data-ttu-id="d2d52-145">Transmissão functors têm acesso à implementação da operação base ao definir a implementação da nova operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-145">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="d2d52-146">Portanto, o transmissão functors pode executar funções mais complexas do que as funções tradicionais de nível superior.</span><span class="sxs-lookup"><span data-stu-id="d2d52-146">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span> <span data-ttu-id="d2d52-147">Transmissão functors não tem uma representação no sistema do tipo Q #.</span><span class="sxs-lookup"><span data-stu-id="d2d52-147">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="d2d52-148">Portanto, no momento, não é possível associá-los a uma variável ou passá-los como argumentos.</span><span class="sxs-lookup"><span data-stu-id="d2d52-148">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="d2d52-149">Um functor é usado aplicando-o a uma operação, retornando uma nova operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-149">A functor is used by applying it to an operation, returning a new operation.</span></span>
<span data-ttu-id="d2d52-150">Por exemplo, a operação resultante da aplicação do `Adjoint` functor à `Y` operação é escrita como `Adjoint Y` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-150">For example, the operation that results from applying the `Adjoint` functor to the `Y` operation is written as `Adjoint Y`.</span></span>
<span data-ttu-id="d2d52-151">A nova operação pode ser invocada como qualquer outra operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-151">The new operation may then be invoked like any other operation.</span></span>
<span data-ttu-id="d2d52-152">Para uma operação para dar suporte ao aplicativo do `Adjoint` e/ou `Controlled` transmissão functors, seu tipo de retorno precisa ser necessariamente `Unit` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-152">For an operation to support application of the `Adjoint` and/or `Controlled` functors, its return type necessarily needs to be `Unit`.</span></span> 

#### <a name="adjoint-functor"></a><span data-ttu-id="d2d52-153">`Adjoint`functor</span><span class="sxs-lookup"><span data-stu-id="d2d52-153">`Adjoint` functor</span></span>

<span data-ttu-id="d2d52-154">Assim, `Adjoint Y(q1)` o aplica o functor de modo adjacente à `Y` operação para gerar uma nova operação e aplica essa nova operação ao `q1` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-154">Thus, `Adjoint Y(q1)` applies the Adjoint functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>
<span data-ttu-id="d2d52-155">A nova operação tem a mesma assinatura e tipo que a operação base `Y` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-155">The new operation has the same signature and type as the base operation `Y`.</span></span>
<span data-ttu-id="d2d52-156">Em particular, a nova operação também permite e `Adjoint` permitirá `Controlled` se e somente se a operação base tivesse sido.</span><span class="sxs-lookup"><span data-stu-id="d2d52-156">In particular, the new operation also allows `Adjoint`, and will allow `Controlled` if and only if the base operation did.</span></span>
<span data-ttu-id="d2d52-157">O functor de adjacente é seu próprio inverso; ou seja, `Adjoint Adjoint Op` é sempre o mesmo que `Op` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-157">The Adjoint functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled-functor"></a><span data-ttu-id="d2d52-158">`Controlled`functor</span><span class="sxs-lookup"><span data-stu-id="d2d52-158">`Controlled` functor</span></span>

<span data-ttu-id="d2d52-159">Da mesma forma, `Controlled X(controls, target)` o aplica o functor controlado à `X` operação para gerar uma nova operação e aplica essa nova operação ao `controls` e ao `target` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-159">Similarly, `Controlled X(controls, target)` applies the Controlled functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

> [!NOTE]
> <span data-ttu-id="d2d52-160">Em Q #, as versões controladas sempre usam uma matriz de qubits de controle e o estado especificado é sempre para todos os qubits de controle que estão no estado computacional ( `PauliZ` ) `One` , $ \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="d2d52-160">In Q#, controlled versions always take an array of control qubits, and the specified state is always for all of the control qubits to be in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
> <span data-ttu-id="d2d52-161">O controle com base em outros Estados pode ser obtido aplicando a operação unitário apropriada ao qubits de controle antes da operação controlada e, em seguida, aplicando os inversos da operação unitário após a operação controlada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-161">Controlling based on other states may be achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
> <span data-ttu-id="d2d52-162">Por exemplo, aplicar uma `X` operação a um controle qubit antes e depois de uma operação controlada fará com que a operação controle o `Zero` estado ($ \ket {0} $) para esse qubit; aplicar uma `H` operação antes e depois controlará o `PauliX` `One` estado, que é-1 eigenvalue de Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ em vez do `PauliZ` `One` estado.</span><span class="sxs-lookup"><span data-stu-id="d2d52-162">For example, applying an `X` operation to a control qubit before and after a controlled operation will cause the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after will control on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="d2d52-163">Dada uma expressão de operação, uma nova expressão de operação pode ser formada usando o `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="d2d52-163">Given an operation expression, a new operation expression may be formed using the `Controlled` functor.</span></span>
<span data-ttu-id="d2d52-164">A assinatura da nova operação é baseada na assinatura da operação original.</span><span class="sxs-lookup"><span data-stu-id="d2d52-164">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="d2d52-165">O tipo de resultado é o mesmo, mas o tipo de entrada é de duas tuplas com uma matriz qubit que mantém o controle qubit (s) como o primeiro elemento e os argumentos da operação original como o segundo elemento.</span><span class="sxs-lookup"><span data-stu-id="d2d52-165">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="d2d52-166">A nova operação dá suporte a `Controlled` e dará suporte a `Adjoint` If e somente se a operação original tiver feito isso.</span><span class="sxs-lookup"><span data-stu-id="d2d52-166">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="d2d52-167">Se a operação original levou apenas um único argumento, a equivalência de tupla singleton entrará em ação aqui.</span><span class="sxs-lookup"><span data-stu-id="d2d52-167">If the original operation took only a single argument, then singleton tuple equivalence will come into play here.</span></span>
<span data-ttu-id="d2d52-168">Por exemplo, `Controlled X` é a versão controlada da `X` operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-168">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span> 
<span data-ttu-id="d2d52-169">`X`tem tipo `(Qubit => Unit is Adj + Ctl)` , portanto, `Controlled X` tem tipo `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; devido à equivalência de tupla singleton, isso é o mesmo que `((Qubit[], Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-169">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="d2d52-170">Se a operação base levou vários argumentos, lembre-se de colocar os argumentos correspondentes da versão controlada da operação entre parênteses para convertê-los em uma tupla.</span><span class="sxs-lookup"><span data-stu-id="d2d52-170">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="d2d52-171">Por exemplo, `Controlled Rz` é a versão controlada da `Rz` operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-171">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span> 
<span data-ttu-id="d2d52-172">`Rz`tem tipo `((Double, Qubit) => Unit is Adj + Ctl)` , portanto, `Controlled Rz` tem tipo `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-172">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="d2d52-173">Portanto, `Controlled Rz(controls, (0.1, target))` seria uma invocação válida de `Controlled Rz` (Observe os parênteses `0.1, target` ).</span><span class="sxs-lookup"><span data-stu-id="d2d52-173">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="d2d52-174">Como outro exemplo, `CNOT(control, target)` pode ser implementado como `Controlled X([control], target)` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-174">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="d2d52-175">Se um destino deve ser controlado por dois qubits de controle (CCNOT), podemos usar a `Controlled X([control1, control2], target)` instrução.</span><span class="sxs-lookup"><span data-stu-id="d2d52-175">If a target should be controlled by 2 control qubits (CCNOT), we can use `Controlled X([control1, control2], target)` statement.</span></span>

#### `Controlled Adjoint` 

<span data-ttu-id="d2d52-176">O `Controlled` e o `Adjoint` transmissão functorsm o áudio, portanto, não há nenhuma diferença entre aplicar `Controlled Adjoint Op` ou `Adjoint Controlled Op` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-176">The `Controlled` and `Adjoint` functors commute, so there is no difference between applying `Controlled Adjoint Op` or `Adjoint Controlled Op`.</span></span>


## <a name="defining-controlled-and-adjoint-implementations"></a><span data-ttu-id="d2d52-177">Definindo implementações controladas e adjacentes</span><span class="sxs-lookup"><span data-stu-id="d2d52-177">Defining Controlled and Adjoint Implementations</span></span>

<span data-ttu-id="d2d52-178">Nos exemplos de declaração de primeira operação acima, as operações `BitFlip` e `DecodeSuperdense` foram definidas com assinaturas `(Qubit => Unit)` e `((Qubit, Qubit) => (Result, Result))` , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d2d52-178">In the first operation declaration examples above, the operations `BitFlip` and `DecodeSuperdense` were defined with signatures `(Qubit => Unit)` and `((Qubit, Qubit) => (Result, Result))`, respectively.</span></span>
<span data-ttu-id="d2d52-179">Como `DecodeSuperdense` inclui medições, ela não é uma operação unitário e, portanto, nenhuma especialização não adjacente pode existir (Lembre-se do requisito relacionado que tal operação retorna `Unit` ).</span><span class="sxs-lookup"><span data-stu-id="d2d52-179">As `DecodeSuperdense` includes measurements, it is not a unitary operation, and therefore neither controlled not adjoint specializations could exist (recall the related requirement that such an operation return `Unit`).</span></span>
<span data-ttu-id="d2d52-180">No entanto, como `BitFlip` simplesmente executa a <xref:microsoft.quantum.intrinsic.x> operação unitário, poderíamos defini-la com ambas as especializações.</span><span class="sxs-lookup"><span data-stu-id="d2d52-180">However, as `BitFlip` simply performs the unitary <xref:microsoft.quantum.intrinsic.x> operation, we could have defined it with both specializations.</span></span>

<span data-ttu-id="d2d52-181">Aqui, detalhamos como incluir a existência de especializações em suas declarações de operação de Q #, portanto, dando-lhes a capacidade de chamada em conjunto com o `Adjoint` and/or `Controlled` transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="d2d52-181">Here, we detail how to include the existence of specializations in your Q# operation declarations, hence giving them the ability to called in conjunction with the `Adjoint` and/or `Controlled` functors.</span></span>
<span data-ttu-id="d2d52-182">Além [disso,](#circumstances-for-validly-defining-specializations)descrevemos algumas das situações em que elas são válidas ou não válidas para declarar determinadas especializações.</span><span class="sxs-lookup"><span data-stu-id="d2d52-182">Further [below](#circumstances-for-validly-defining-specializations), we describe some of the situations in which it is either valid or not valid to declare certain specializations.</span></span>

<span data-ttu-id="d2d52-183">As características da operação definem quais tipos de transmissão functors podem ser aplicados à operação declarada e qual efeito eles têm.</span><span class="sxs-lookup"><span data-stu-id="d2d52-183">Operation characteristics define what kinds of functors can be applied to the declared operation, and what effect they have.</span></span> <span data-ttu-id="d2d52-184">A existência dessas especializações pode ser declarada como parte da assinatura da operação, especificamente por meio de uma anotação com as características da operação: `is Adj` `is Ctl` ou, ou `is Adj + Ctl` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-184">The existence of these specializations can be declared as part of the operation signature, specifically through an annotation with the operation characteristics: either `is Adj`, `is Ctl`, or `is Adj + Ctl`.</span></span>
<span data-ttu-id="d2d52-185">A implementação real de cada especialização pode ser definida *implicitamente* ou *explicitamente* .</span><span class="sxs-lookup"><span data-stu-id="d2d52-185">The actual implementation of each specialization can either be *implicitly* or *explicitly* defined.</span></span>

### <a name="implicitly-specifying-implementations"></a><span data-ttu-id="d2d52-186">Especificando implicitamente implementações</span><span class="sxs-lookup"><span data-stu-id="d2d52-186">Implicitly specifying implementations</span></span>

<span data-ttu-id="d2d52-187">Nesse caso, o corpo da declaração da operação consiste exclusivamente na implementação padrão.</span><span class="sxs-lookup"><span data-stu-id="d2d52-187">In this case, the body of the operation declaration consists solely of the default implementation.</span></span> <span data-ttu-id="d2d52-188">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d2d52-188">For example:</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
<span data-ttu-id="d2d52-189">Aqui, a implementação correspondente para cada uma dessas especializações declaradas implicitamente é gerada automaticamente pelo compilador, a ser executada se o `Adjoint` ou `Controlled` transmissão functors forem usados.</span><span class="sxs-lookup"><span data-stu-id="d2d52-189">Here, the corresponding implementation for each such implicitly declared specialization is automatically generated by the compiler, to be performed if the `Adjoint` or `Controlled` functors are used.</span></span>

<span data-ttu-id="d2d52-190">Portanto, uma chamada de `Adjoint PrepareEntangledPair` resultaria no compilador que implementasse o adpositivo de `CNOT` e, em seguida, o adjacente de `H` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-190">So, a call of `Adjoint PrepareEntangledPair` would result in the compiler implementing the adjoint of `CNOT` and then the adjoint of `H`.</span></span>
<span data-ttu-id="d2d52-191">Essas operações individuais são autoadjacentes, portanto, a operação resultante `Adjoint PrepareEntangledPair` simplesmente consistiria em aplicar `CNOT(here, there)` e depois `H(here)` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-191">These individual operations are both self-adjoint, so the resulting `Adjoint PrepareEntangledPair` operation would simply consist of applying `CNOT(here, there)` and then `H(here)`.</span></span>
<span data-ttu-id="d2d52-192">Portanto, podemos usar isso para escrever o `DecodeSuperdense` exemplo acima de forma mais compacta, usando o erro de `PrepareEntangledPair` para transformar o estado confusas de volta em um par unentangled de qubits:</span><span class="sxs-lookup"><span data-stu-id="d2d52-192">Hence we can use this to write the `DecodeSuperdense` example above more compactly, by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="d2d52-193">A anotação com as características da operação na declaração é útil para garantir que o compilador gere automaticamente outras especializações com base na implementação padrão.</span><span class="sxs-lookup"><span data-stu-id="d2d52-193">The annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="d2d52-194">Há várias limitações importantes a serem consideradas ao criar operações para uso com o transmissão functors.</span><span class="sxs-lookup"><span data-stu-id="d2d52-194">There are a number of important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="d2d52-195">O mais importante é que as especializações para uma operação que usa o valor de saída de qualquer outra operação *não podem* ser geradas automaticamente pelo compilador, pois é ambígua como reordenar as instruções nessa operação para obter o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="d2d52-195">Most critically, specializations for an operation that uses the output value of any other operation *cannot* be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>

<span data-ttu-id="d2d52-196">Portanto, geralmente é útil especificar explicitamente as várias implementações.</span><span class="sxs-lookup"><span data-stu-id="d2d52-196">Therefore, it is often useful to explicitly specify the various implementations.</span></span>

### <a name="explicitly-specifying-implementations"></a><span data-ttu-id="d2d52-197">Especificando explicitamente implementações</span><span class="sxs-lookup"><span data-stu-id="d2d52-197">Explicitly specifying implementations</span></span>

<span data-ttu-id="d2d52-198">No caso em que a implementação não pode ser gerada pelo compilador, ela pode ser especificada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="d2d52-198">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="d2d52-199">Essas declarações de especialização explícitas podem consistir em uma *diretiva de geração* adequada ou em uma implementação definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d2d52-199">Such explicit specialization declarations can consist of a suitable *generation directive* or a user-defined implementation.</span></span>
<span data-ttu-id="d2d52-200">Aqui, fornecemos a gama completa de possibilidades, com exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2d52-200">Here we provide the full range of possibilities, with examples following below.</span></span>


#### <a name="explicit-specialization-declarations"></a><span data-ttu-id="d2d52-201">Declarações de especialização explícitas</span><span class="sxs-lookup"><span data-stu-id="d2d52-201">Explicit specialization declarations</span></span>

<span data-ttu-id="d2d52-202">As operações de Q # podem conter as seguintes declarações de especialização explícitas:</span><span class="sxs-lookup"><span data-stu-id="d2d52-202">Q# operations may contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="d2d52-203">A `body` especialização especifica a implementação da operação sem nenhum transmissão functors aplicado.</span><span class="sxs-lookup"><span data-stu-id="d2d52-203">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="d2d52-204">A `adjoint` especialização especifica a implementação da operação com o `Adjoint` functor aplicado.</span><span class="sxs-lookup"><span data-stu-id="d2d52-204">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="d2d52-205">A `controlled` especialização especifica a implementação da operação com o `Controlled` functor aplicado.</span><span class="sxs-lookup"><span data-stu-id="d2d52-205">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="d2d52-206">A `controlled adjoint` especialização especifica a implementação da operação com o `Adjoint` e o `Controlled` transmissão functors aplicados.</span><span class="sxs-lookup"><span data-stu-id="d2d52-206">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="d2d52-207">Essa especialização também pode ser nomeada `adjoint controlled` , já que as duas transmissão functorsm.</span><span class="sxs-lookup"><span data-stu-id="d2d52-207">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="d2d52-208">Uma especialização de operação consiste na marca de especialização (por exemplo `body` , ou `adjoint` , etc.) seguida de uma das:</span><span class="sxs-lookup"><span data-stu-id="d2d52-208">An operation specialization consists of the specialization tag (e.g. `body`, or `adjoint`, etc.) followed by one of:</span></span>

- <span data-ttu-id="d2d52-209">Uma declaração explícita, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="d2d52-209">An explicit declaration as described below.</span></span>
- <span data-ttu-id="d2d52-210">Uma *diretiva* que informa ao compilador *como* gerar a especialização, uma das:</span><span class="sxs-lookup"><span data-stu-id="d2d52-210">A *directive* that tells the compiler *how* to generate the specialization, one of:</span></span>
  - <span data-ttu-id="d2d52-211">`intrinsic`, que indica que a especialização é fornecida pelo computador de destino.</span><span class="sxs-lookup"><span data-stu-id="d2d52-211">`intrinsic`, which indicates that the specialization is provided by the target machine.</span></span>
  - <span data-ttu-id="d2d52-212">`distribute`, que pode ser usado com as `controlled` `controlled adjoint` especializações e.</span><span class="sxs-lookup"><span data-stu-id="d2d52-212">`distribute`, which may be used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="d2d52-213">Quando usado com `controlled` , ele indica que o compilador deve calcular a especialização aplicando-se `Controlled` a todas as operações no `body` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-213">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="d2d52-214">Quando usado com `controlled adjoint` , ele indica que o compilador deve calcular a especialização aplicando-se `Controlled` a todas as operações na `adjoint` especialização.</span><span class="sxs-lookup"><span data-stu-id="d2d52-214">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="d2d52-215">`invert`, que indica que o compilador deve calcular a `adjoint` especialização invertendo o `body` , ou seja, revertendo a ordem das operações e aplicando o adjacente a cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="d2d52-215">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, i.e. reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="d2d52-216">Quando usado com `adjoint controlled` , isso indica que o compilador deve calcular a especialização invertendo a `controlled` especialização.</span><span class="sxs-lookup"><span data-stu-id="d2d52-216">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="d2d52-217">`self`, para indicar que a especialização de adjacente é a mesma que a `body` especialização.</span><span class="sxs-lookup"><span data-stu-id="d2d52-217">`self`, to indicate that the adjoint specialization is the the same as the `body` specialization.</span></span>
    <span data-ttu-id="d2d52-218">Isso é legal para as `adjoint` `adjoint controlled` especializações e.</span><span class="sxs-lookup"><span data-stu-id="d2d52-218">This is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="d2d52-219">Para `adjoint controlled` , `self` implica que a `adjoint controlled` especialização é a mesma que a `controlled` especialização.</span><span class="sxs-lookup"><span data-stu-id="d2d52-219">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="d2d52-220">`auto`, para indicar que o compilador deve selecionar uma diretiva apropriada a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-220">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="d2d52-221">`auto`Não pode ser usado para a `body` especialização.</span><span class="sxs-lookup"><span data-stu-id="d2d52-221">`auto` may not be used for the `body` specialization.</span></span>

<span data-ttu-id="d2d52-222">As diretivas e `auto` todas exigem um ponto-e-vírgula de fechamento `;` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-222">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="d2d52-223">A `auto` diretiva será resolvida para a seguinte diretiva de geração se uma declaração explícita do `body` for fornecida:</span><span class="sxs-lookup"><span data-stu-id="d2d52-223">The `auto` directive resolves to the following generation directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="d2d52-224">A `adjoint` especialização é gerada de acordo com a diretiva `invert` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-224">The `adjoint` specialization is generated according to the directive `invert`.</span></span>
- <span data-ttu-id="d2d52-225">A `controlled` especialização é gerada de acordo com a diretiva `distribute` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-225">The `controlled` specialization is generated according to the directive `distribute`.</span></span>
- <span data-ttu-id="d2d52-226">A `adjoint controlled` especialização será gerada de acordo com a diretiva `invert` se uma declaração explícita para `controlled` for fornecida, mas não uma para e `adjoint` , `distribute` caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d2d52-226">The `adjoint controlled` specialization is generated according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="d2d52-227">Se uma operação for autoadjacente, especifique explicitamente a prejunção ou a especialização de adjacente controlada por meio da diretiva de geração `self` para permitir que o compilador use essas informações para fins de otimização.</span><span class="sxs-lookup"><span data-stu-id="d2d52-227">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="d2d52-228">Uma declaração de especialização contendo uma implementação definida pelo usuário consiste em uma tupla de argumento seguida por um bloco de instrução com o código Q # que implementa a especialização.</span><span class="sxs-lookup"><span data-stu-id="d2d52-228">A specialization declaration containing a user defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="d2d52-229">Na lista de argumentos, `...` é usado para representar os argumentos declarados para a operação como um todo.</span><span class="sxs-lookup"><span data-stu-id="d2d52-229">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="d2d52-230">Para `body` e `adjoint` , a lista de argumentos deve ser sempre `(...)` ; para `controlled` e `adjoint controlled` , a lista de argumentos deve ser um símbolo que representa a matriz de controle qubits, seguida por `...` , entre parênteses; por exemplo, `(controls,...)` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-230">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

### <a name="examples"></a><span data-ttu-id="d2d52-231">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2d52-231">Examples</span></span>

<span data-ttu-id="d2d52-232">Uma declaração de operação pode ser tão simples quanto a seguinte, que define a operação primitiva de Pauli X:</span><span class="sxs-lookup"><span data-stu-id="d2d52-232">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
<span data-ttu-id="d2d52-233">Observe que o adjoin da operação Pauli X é definido com a diretiva `self` porque, por definição, `X` é seu próprio inverso.</span><span class="sxs-lookup"><span data-stu-id="d2d52-233">Note that the adjoint of the Pauli X operation is defined with the directive `self` because by definition `X` is its own inverse.</span></span>

<span data-ttu-id="d2d52-234">O código `PrepareEntangledPair` acima, por exemplo, é equivalente ao código abaixo que contém declarações de especialização explícitas:</span><span class="sxs-lookup"><span data-stu-id="d2d52-234">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

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
<span data-ttu-id="d2d52-235">A palavra-chave `auto` indica que o compilador deve determinar como gerar a implementação de especialização.</span><span class="sxs-lookup"><span data-stu-id="d2d52-235">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>

#### <a name="user-defined-specialization-implementation"></a><span data-ttu-id="d2d52-236">Implementação de especialização definida pelo usuário</span><span class="sxs-lookup"><span data-stu-id="d2d52-236">User-defined specialization implementation</span></span>

<span data-ttu-id="d2d52-237">Se o compilador não puder gerar a implementação para determinada especialização automaticamente ou se uma implementação mais eficiente puder ser fornecida, a implementação também poderá ser definida manualmente.</span><span class="sxs-lookup"><span data-stu-id="d2d52-237">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="d2d52-238">No exemplo acima, `adjoint invert;` indica que a especialização de adjacente deve ser gerada pela inversão da implementação do corpo e `controlled adjoint invert;` indica que a especialização adjacente controlada deve ser gerada por meio da inversão da implementação fornecida da especialização controlada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-238">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="d2d52-239">Se uma ou mais especializações além do corpo padrão precisarem ser declaradas explicitamente, a implementação do corpo padrão precisará ser encapsulada em uma declaração de especialização adequada também:</span><span class="sxs-lookup"><span data-stu-id="d2d52-239">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

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

### <a name="circumstances-for-validly-defining-specializations"></a><span data-ttu-id="d2d52-240">Circunstâncias de definição válida de especializações</span><span class="sxs-lookup"><span data-stu-id="d2d52-240">Circumstances for validly defining specializations</span></span>

#### <a name="operation-declarations-with-adjointcontrolled"></a><span data-ttu-id="d2d52-241">Declarações de operação com adjoind/controlled</span><span class="sxs-lookup"><span data-stu-id="d2d52-241">Operation declarations with adjoint/controlled</span></span>

<span data-ttu-id="d2d52-242">É legal especificar uma operação sem nenhuma versão adjacente ou controlada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-242">It is legal to specify an operation with no adjoint or controlled versions.</span></span> <span data-ttu-id="d2d52-243">Por exemplo, as operações de medição não têm nenhum, porque elas não são invertível ou controláveis.</span><span class="sxs-lookup"><span data-stu-id="d2d52-243">For instance, measurement operations have neither, because they are not invertible or controllable.</span></span>

<span data-ttu-id="d2d52-244">Uma operação dá suporte a `Adjoint` e/ou `Controlled` transmissão functors se sua declaração contiver uma declaração implícita ou explícita das respectivas especializações.</span><span class="sxs-lookup"><span data-stu-id="d2d52-244">An operation supports the `Adjoint` and/or `Controlled` functors if its declaration contains an implicit or explicit declaration of the respective specializations.</span></span>

<span data-ttu-id="d2d52-245">Uma especialização adjacente/controlada explícita implica a existência de uma especialização adjacente/controlada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-245">An explicitly declared adjoint/controlled specialization implies the existence of an adjoint/controlled specialization.</span></span> 

<span data-ttu-id="d2d52-246">Para uma operação cujo corpo contém loops repetir-até-êxito, instruções SET, medidas, instruções de retorno ou chamadas para outras operações que não dão suporte a `Adjoint` functor, a geração automática de uma especialização de adjacente após a `invert` `auto` diretiva ou não é possível.</span><span class="sxs-lookup"><span data-stu-id="d2d52-246">For an operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

<span data-ttu-id="d2d52-247">Para uma operação cujo corpo contém chamadas para outras operações que não dão suporte ao `Controlled` functor, a geração automática de uma especialização controlada após a `distribute` `auto` diretiva ou não é possível.</span><span class="sxs-lookup"><span data-stu-id="d2d52-247">For an operation whose body contains calls to other operations that does not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

#### <a name="controlled-adjoint"></a><span data-ttu-id="d2d52-248">Adjacente controlado</span><span class="sxs-lookup"><span data-stu-id="d2d52-248">Controlled Adjoint</span></span>

<span data-ttu-id="d2d52-249">A versão adjacente controlada de uma operação especifica como uma versão controlada pelo Quantum do adjoin da operação é implementada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-249">The controlled adjoint version of an operation specifies how a quantum-controlled version of the adjoint of the operation is implemented.</span></span>
<span data-ttu-id="d2d52-250">É legal especificar uma operação sem nenhuma versão adjacente controlada; por exemplo, as operações de medição não têm nenhuma versão adjacente controlada porque não são controláveis nem invertível.</span><span class="sxs-lookup"><span data-stu-id="d2d52-250">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="d2d52-251">Uma especialização de adjacente controlada para uma operação precisa existir se e somente se houver uma especialização de somente um e um adjacente.</span><span class="sxs-lookup"><span data-stu-id="d2d52-251">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="d2d52-252">Nesse caso, a existência da especialização adjacente controlada é inferida e uma especialização apropriada é gerada pelo compilador se nenhuma implementação tiver sido definida explicitamente.</span><span class="sxs-lookup"><span data-stu-id="d2d52-252">In that case, the existence of the controlled adjoint specialization is inferred and an appropriate specialization is generated by the compiler if no implementation has been defined explicitly.</span></span> 

<span data-ttu-id="d2d52-253">Para uma operação cujo corpo contém chamadas para outras operações que não têm uma versão adjacente controlada, a geração automática de uma especialização de adjacente após a `invert` `distribute` `auto` diretiva ou não é possível.</span><span class="sxs-lookup"><span data-stu-id="d2d52-253">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute` or `auto` directive is not possible.</span></span>


### <a name="type-compatibility"></a><span data-ttu-id="d2d52-254">Compatibilidade de tipo</span><span class="sxs-lookup"><span data-stu-id="d2d52-254">Type Compatibility</span></span>

<span data-ttu-id="d2d52-255">Uma operação com suporte adicional a transmissão functors pode ser usada em qualquer lugar de uma operação com menos transmissão functors, mas a mesma assinatura é esperada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-255">An operation with additional functors supported may be used anywhere an operation with fewer functors but the same signature is expected.</span></span>
<span data-ttu-id="d2d52-256">Por exemplo, uma operação do tipo `(Qubit => Unit is Adj)` pode ser usada em qualquer lugar em que uma operação do tipo `(Qubit => Unit)` é esperada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-256">For instance, an operation of type `(Qubit => Unit is Adj)` may be used anywhere an operation of type `(Qubit => Unit)` is expected.</span></span>

<span data-ttu-id="d2d52-257">Q # é *covariant* com relação a tipos de retorno que podem ser chamados: um callable que retorna um tipo `'A` é compatível com um callable com o mesmo tipo de entrada e um tipo de resultado `'A` compatível com.</span><span class="sxs-lookup"><span data-stu-id="d2d52-257">Q# is *covariant* with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that `'A` is compatible with.</span></span>

<span data-ttu-id="d2d52-258">Q # é *contravariant* em relação aos tipos de entrada: um callable que usa um tipo `'A` como entrada é compatível com um callable com o mesmo tipo de resultado e um tipo de entrada compatível com `'A` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-258">Q# is *contravariant* with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="d2d52-259">Ou seja, dadas as seguintes definições:</span><span class="sxs-lookup"><span data-stu-id="d2d52-259">That is, given the following definitions:</span></span>

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

<span data-ttu-id="d2d52-260">o seguinte é verdadeiro:</span><span class="sxs-lookup"><span data-stu-id="d2d52-260">the following are true:</span></span>

- <span data-ttu-id="d2d52-261">A função `ConjugateInvertWith` pode ser chamada com um `inner` argumento de `Invert` ou `ApplyUnitary` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-261">The function `ConjugateInvertWith` may be invoked with an `inner` argument of either `Invert` or `ApplyUnitary`.</span></span>
- <span data-ttu-id="d2d52-262">A função `ConjugateUnitaryWith` pode ser chamada com um `inner` argumento de `ApplyUnitary` , mas não `Invert` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-262">The function `ConjugateUnitaryWith` may be invoked with an `inner` argument of `ApplyUnitary`, but not `Invert`.</span></span>
- <span data-ttu-id="d2d52-263">Um valor do tipo `(Qubit[] => Unit is Adj + Ctl)` pode ser retornado de `ConjugateInvertWith` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-263">A value of type `(Qubit[] => Unit is Adj + Ctl)` may be returned from `ConjugateInvertWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2d52-264">A p # 0,3 introduziu uma diferença significativa no comportamento de tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d2d52-264">Q# 0.3 introduced a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="d2d52-265">Os tipos definidos pelo usuário são tratados como uma versão encapsulada do tipo subjacente, em vez de como um subtipo.</span><span class="sxs-lookup"><span data-stu-id="d2d52-265">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="d2d52-266">Isso significa que um valor de um tipo definido pelo usuário não é utilizável, em que um valor do tipo subjacente é esperado.</span><span class="sxs-lookup"><span data-stu-id="d2d52-266">This means that a value of a user-defined type is not usable where a value of the underlying type is expected.</span></span>


### <a name="conjugations"></a><span data-ttu-id="d2d52-267">Conjugações</span><span class="sxs-lookup"><span data-stu-id="d2d52-267">Conjugations</span></span>

<span data-ttu-id="d2d52-268">Em contraste com os bits clássicos, liberar memória Quantum é um pouco mais envolvida, uma vez que a redefinição oculta de qubits pode ter efeitos indesejados na computação restante se o qubits ainda for confusas.</span><span class="sxs-lookup"><span data-stu-id="d2d52-268">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="d2d52-269">Isso pode ser evitado com o "desfazendo" adequadamente os cálculos executados antes de liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="d2d52-269">This can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="d2d52-270">Um padrão comum na computação Quantum é, portanto, o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d2d52-270">A common pattern in quantum computing is hence the following:</span></span> 

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

<span data-ttu-id="d2d52-271">A partir da nossa versão 0,9, damos suporte a uma instrução Conjugation que implementa a transformação acima.</span><span class="sxs-lookup"><span data-stu-id="d2d52-271">Starting with our 0.9 release, we support a conjugation statement that implements the transformation above.</span></span> <span data-ttu-id="d2d52-272">Usando essa instrução, a operação `ApplyWith` pode ser implementada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d2d52-272">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

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
<span data-ttu-id="d2d52-273">Uma instrução de conjugação, obviamente, se torna muito mais útil se as transformações externa e interna não estão prontamente disponíveis como operações, mas são mais convenientes de descrever por um bloco que consiste em várias instruções.</span><span class="sxs-lookup"><span data-stu-id="d2d52-273">Such a conjugation statement obviously becomes far more useful if the outer and inner transformation are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="d2d52-274">A transformação inversa para as instruções definidas no bloco Within é gerada automaticamente pelo compilador e executada após a conclusão do bloco de aplicação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-274">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and executed after the apply-block completes.</span></span>
<span data-ttu-id="d2d52-275">Como as variáveis mutáveis usadas como parte do bloco Within não podem ser reassociadas no bloco Apply, a transformação gerada é garantida como sendo a adjoin do cálculo no bloco Within.</span><span class="sxs-lookup"><span data-stu-id="d2d52-275">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 


## <a name="defining-new-functions"></a><span data-ttu-id="d2d52-276">Definindo novas funções</span><span class="sxs-lookup"><span data-stu-id="d2d52-276">Defining New Functions</span></span>

<span data-ttu-id="d2d52-277">As funções são puramente determinísticas, rotinas clássicas em Q #, que são diferentes das operações, pois elas não têm permissão para ter nenhum efeito além de calcular um valor de saída.</span><span class="sxs-lookup"><span data-stu-id="d2d52-277">Functions are purely deterministic, classical routines in Q#, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="d2d52-278">Em particular, as funções não podem chamar operações; agir sobre, alocar ou emprestar qubits; números aleatórios de exemplo; ou, de outra forma, dependem do estado após o valor de entrada para uma função.</span><span class="sxs-lookup"><span data-stu-id="d2d52-278">In particular, functions cannot call operations; act on, allocate, or borrow qubits; sample random numbers; or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="d2d52-279">Como consequência, as funções Q # são *puras*, pois elas sempre mapeiam os mesmos valores de entrada para os mesmos valores de saída.</span><span class="sxs-lookup"><span data-stu-id="d2d52-279">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="d2d52-280">Isso permite que o compilador Q # reordene com segurança como e quando as funções são chamadas ao gerar especializações de operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-280">This allows the Q# compiler to safely reorder how and when functions are called when generating operation specializations.</span></span>

<span data-ttu-id="d2d52-281">Cada arquivo de origem Q # pode definir qualquer número de funções.</span><span class="sxs-lookup"><span data-stu-id="d2d52-281">Each Q# source file may define any number of functions.</span></span>
<span data-ttu-id="d2d52-282">Os nomes de função devem ser exclusivos em um namespace e podem não entrar em conflito com os nomes de operação ou tipo.</span><span class="sxs-lookup"><span data-stu-id="d2d52-282">Function names must be unique within a namespace and may not conflict with operation or type names.</span></span>

<span data-ttu-id="d2d52-283">A definição de uma função funciona de forma semelhante à definição de uma operação, exceto que nenhuma especialização adjacente ou controlada pode ser definida para uma função.</span><span class="sxs-lookup"><span data-stu-id="d2d52-283">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="d2d52-284">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d2d52-284">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

<span data-ttu-id="d2d52-285">ou</span><span class="sxs-lookup"><span data-stu-id="d2d52-285">or</span></span> 

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

### <a name="classical-logic-in-functions--good"></a><span data-ttu-id="d2d52-286">Lógica clássica em funções = = bom</span><span class="sxs-lookup"><span data-stu-id="d2d52-286">Classical logic in functions == good</span></span>

<span data-ttu-id="d2d52-287">Sempre que for possível fazer isso, é útil escrever a lógica clássica em termos de funções em vez de operações, para que ela possa ser usada mais prontamente em operações.</span><span class="sxs-lookup"><span data-stu-id="d2d52-287">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations, so that it can be more readily used from within operations.</span></span>
<span data-ttu-id="d2d52-288">Por exemplo, se tivéssemos escrito a `Square` declaração acima como uma *operação*, o compilador não teria conseguido garantir que chamá-la com a mesma entrada produziria consistentemente as mesmas saídas.</span><span class="sxs-lookup"><span data-stu-id="d2d52-288">For example, if we had written the `Square` declaration above as an *operation*, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="d2d52-289">Para enfatizar a diferença entre funções e operações, considere o problema de amostragem clássica de um número aleatório de dentro de uma operação Q #:</span><span class="sxs-lookup"><span data-stu-id="d2d52-289">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="d2d52-290">Cada vez que `U` for chamado, ele terá uma ação diferente no `target` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-290">Each time that `U` is called, it will have a different action on `target`.</span></span>
<span data-ttu-id="d2d52-291">Em particular, o compilador não pode garantir que, se adicionamos uma `adjoint auto` declaração de especialização a `U` , `U(target); Adjoint U(target);` atua como identidade (ou seja, como não operacional).</span><span class="sxs-lookup"><span data-stu-id="d2d52-291">In particular, the compiler cannot guarantee that if we added an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="d2d52-292">Isso viola a definição do adjacente que vimos em [vetores e matrizes](xref:microsoft.quantum.concepts.vectors), de modo que permitir a geração automática de uma especialização adjacente em uma operação em que chamamos a operação <xref:microsoft.quantum.math.randomreal> interromperia as garantias fornecidas pelo compilador; <xref:microsoft.quantum.math.randomreal> é uma operação para a qual não existe nenhuma versão adjacente ou controlada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-292">This violates the definition of the adjoint that we saw in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing to auto-generate an adjoint specialization in an operation where we have called the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="d2d52-293">Por outro lado, permitir chamadas de função como `Square` é seguro, pois o compilador pode ter certeza de que ele só precisa preservar a entrada para `Square` para manter sua saída estável.</span><span class="sxs-lookup"><span data-stu-id="d2d52-293">On the other hand, allowing function calls such as `Square` is safe, in that the compiler can be assured that it only needs to preserve the input to `Square` in order to keep its output stable.</span></span>
<span data-ttu-id="d2d52-294">Portanto, isolar o máximo de lógica clássica possível em funções facilita a reutilização dessa lógica em outras funções e operações semelhantes.</span><span class="sxs-lookup"><span data-stu-id="d2d52-294">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>


## <a name="generic-type-parameterized-callables"></a><span data-ttu-id="d2d52-295">Chamadores genéricos (com parâmetros de tipo)</span><span class="sxs-lookup"><span data-stu-id="d2d52-295">Generic (Type-Parameterized) Callables</span></span>

<span data-ttu-id="d2d52-296">Muitas funções e operações que desejamos definir não dependem muito dos tipos de suas entradas, mas, em vez disso, apenas usam implicitamente seus tipos por meio de alguma outra função ou operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-296">Many functions and operations that we might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="d2d52-297">Por exemplo, considere o conceito de *mapa* comum a muitas linguagens funcionais; dada uma função $f (x) $ e uma coleção de valores $ \{ x_1, x_2, \dots, x_n \} $, MAP retorna uma nova coleção $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $.</span><span class="sxs-lookup"><span data-stu-id="d2d52-297">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="d2d52-298">Para implementar isso em Q #, podemos aproveitar essas funções como primeira classe.</span><span class="sxs-lookup"><span data-stu-id="d2d52-298">To implement this in Q#, we can take advantage of that functions are first class.</span></span>
<span data-ttu-id="d2d52-299">Vamos escrever um exemplo rápido de `Map` , usando ★ como um espaço reservado enquanto configuramos quais tipos precisamos.</span><span class="sxs-lookup"><span data-stu-id="d2d52-299">Let's write out a quick example of `Map`, using ★ as a placeholder while we figure out what types we need.</span></span>

```qsharp
function Map(fn : (★ -> ★), values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="d2d52-300">Observe que essa função parece muito boa, independentemente de quais tipos reais substituímos.</span><span class="sxs-lookup"><span data-stu-id="d2d52-300">Note this function looks very much the same no matter what actual types we substitute in.</span></span>
<span data-ttu-id="d2d52-301">Um mapa de inteiros para Paulis, por exemplo, parece muito o mesmo que um mapa de números de ponto flutuante para cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="d2d52-301">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

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

<span data-ttu-id="d2d52-302">Em princípio, poderíamos escrever uma versão do `Map` para cada par de tipos que encontramos, mas isso apresenta uma série de dificuldades.</span><span class="sxs-lookup"><span data-stu-id="d2d52-302">In principle, we could write a version of `Map` for every pair of types that we encounter, but this introduces a number of difficulties.</span></span>
<span data-ttu-id="d2d52-303">Por exemplo, se encontrarmos um bug no `Map` , devemos garantir que a correção seja aplicada uniformemente em todas as versões do `Map` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-303">For instance, if we find a bug in `Map`, then we must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="d2d52-304">Além disso, se construirmos uma nova tupla ou UDT, agora devemos também construir um novo `Map` para ir junto com o novo tipo.</span><span class="sxs-lookup"><span data-stu-id="d2d52-304">Moreover, if we construct a new tuple or UDT, then we must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="d2d52-305">Embora isso seja indevido a um pequeno número de funções desse tipo, à medida que coletamos cada vez mais funções da mesma forma que `Map` , o custo da introdução de novos tipos torna-se razoavelmente grande em ordem razoavelmente curta.</span><span class="sxs-lookup"><span data-stu-id="d2d52-305">While this is tractable for a small number of such functions, as we collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="d2d52-306">No entanto, grande parte dessa dificuldade resulta de que o compilador não deu as informações de que ele precisa para reconhecer como as diferentes versões do `Map` estão relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d2d52-306">Much of this difficulty results, however, from that the we have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="d2d52-307">Efetivamente, queremos que o compilador trate `Map` como um tipo de função matemática de *tipos* q # para funções q #.</span><span class="sxs-lookup"><span data-stu-id="d2d52-307">Effectively, we want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>

<span data-ttu-id="d2d52-308">Essa noção é formalizada permitindo que funções e operações tenham *parâmetros de tipo*, bem como seus parâmetros de tupla comuns.</span><span class="sxs-lookup"><span data-stu-id="d2d52-308">This notion is formalized by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="d2d52-309">Nos exemplos acima, desejamos considerar `Map` como tendo parâmetros de tipo `Int, Pauli` no primeiro caso e `Double, String` no segundo caso.</span><span class="sxs-lookup"><span data-stu-id="d2d52-309">In the examples above, we wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="d2d52-310">Na maior parte, esses parâmetros de tipo podem ser usados como se fossem tipos comuns: usamos valores de parâmetros de tipo para criar matrizes e tuplas, chamar funções e operações e atribuir a variáveis comuns ou mutáveis.</span><span class="sxs-lookup"><span data-stu-id="d2d52-310">For the most part, these type parameters can then be used as though they were ordinary types: we use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="d2d52-311">O caso mais extremo de dependência indireta é o de qubits, em que um programa Q # não pode depender diretamente da estrutura do `Qubit` tipo, mas **deve** passar esses tipos para outras operações e funções.</span><span class="sxs-lookup"><span data-stu-id="d2d52-311">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type, but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="d2d52-312">Retornando ao exemplo acima, podemos ver que precisamos `Map` ter parâmetros de tipo, um para representar a entrada para `fn` e um para representar a saída de `fn` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-312">Returning to the example above, then, we can see that we need `Map` to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="d2d52-313">Em Q #, isso é escrito pela adição de colchetes angulares (ou seja `<>` , não brakets $ \braket {} $!) após o nome de uma função ou operação em sua declaração e listando cada parâmetro de tipo.</span><span class="sxs-lookup"><span data-stu-id="d2d52-313">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="d2d52-314">O nome de cada parâmetro de tipo deve começar com um tique `'` , indicando que ele é um parâmetro de tipo e não um tipo comum (também conhecido como um tipo *concreto* ).</span><span class="sxs-lookup"><span data-stu-id="d2d52-314">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="d2d52-315">Por `Map` isso, escrevemos:</span><span class="sxs-lookup"><span data-stu-id="d2d52-315">For `Map`, we thus write:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="d2d52-316">Observe que a definição de `Map<'Input, 'Output>` parece extremamente semelhante às versões que escrevemos antes.</span><span class="sxs-lookup"><span data-stu-id="d2d52-316">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the versions we wrote out before.</span></span>
<span data-ttu-id="d2d52-317">A única diferença é que nós informamos explicitamente o compilador que `Map` não depende diretamente do `'Input` que e `'Output` são, mas funciona para dois tipos usando-os indiretamente por meio de `fn` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-317">The only difference is that we have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="d2d52-318">Depois de definirmos `Map<'Input, 'Output>` dessa forma, podemos chamá-lo como se fosse uma função comum:</span><span class="sxs-lookup"><span data-stu-id="d2d52-318">Once we have defined `Map<'Input, 'Output>` in this way, we can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="d2d52-319">Escrever funções e operações genéricas é um lugar em que "tupla-in-out" é uma maneira muito útil de pensar em funções e operações do Q #.</span><span class="sxs-lookup"><span data-stu-id="d2d52-319">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="d2d52-320">Como cada função usa exatamente uma entrada e retorna exatamente uma saída, uma entrada do tipo `'T -> 'U` corresponde a *qualquer* função Q # qualquer.</span><span class="sxs-lookup"><span data-stu-id="d2d52-320">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="d2d52-321">Da mesma forma, qualquer operação pode ser passada para uma entrada do tipo `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-321">Similarly, any operation can be passed to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="d2d52-322">Como um segundo exemplo, considere o desafio de escrever uma função que retorne a composição de duas outras funções:</span><span class="sxs-lookup"><span data-stu-id="d2d52-322">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="d2d52-323">Aqui, devemos especificar exatamente o que `A` , `B` e `C` estão, limitando seriamente o utilitário de nossa nova `Compose` função.</span><span class="sxs-lookup"><span data-stu-id="d2d52-323">Here, we must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="d2d52-324">Afinal, `Compose` só depende de `A` , `B` e `C` *através* `innerFn` de e `outerFn` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-324">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="d2d52-325">Como alternativa, podemos adicionar parâmetros de tipo ao `Compose` que indiquem que ele funciona para *qualquer* `A` , `B` e `C` , desde que esses parâmetros correspondam aos esperados por `innerFn` e `outerFn` :</span><span class="sxs-lookup"><span data-stu-id="d2d52-325">As an alternative, then, we can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="d2d52-326">As bibliotecas padrão de Q # fornecem uma variedade de operações e funções parametrizadas por tipo para facilitar o expressar o fluxo de controle de ordem mais alta.</span><span class="sxs-lookup"><span data-stu-id="d2d52-326">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="d2d52-327">Eles são abordados mais detalhadamente no [Guia de biblioteca padrão do Q #](xref:microsoft.quantum.libraries.standard.intro).</span><span class="sxs-lookup"><span data-stu-id="d2d52-327">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>


## <a name="callables-as-first-class-values"></a><span data-ttu-id="d2d52-328">É chamado como valores de primeira classe</span><span class="sxs-lookup"><span data-stu-id="d2d52-328">Callables as First-Class Values</span></span>

<span data-ttu-id="d2d52-329">Uma técnica crítica para o raciocínio sobre o fluxo de controle e a lógica clássica usando funções em vez de operações é utilizar essas operações e funções em Q # são de *primeira classe*.</span><span class="sxs-lookup"><span data-stu-id="d2d52-329">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="d2d52-330">Ou seja, eles são cada um dos valores no idioma que estão no seu próprio direito.</span><span class="sxs-lookup"><span data-stu-id="d2d52-330">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="d2d52-331">Por exemplo, este é um código Q # perfeitamente válido, se um pouco indireto:</span><span class="sxs-lookup"><span data-stu-id="d2d52-331">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="d2d52-332">O valor da variável `ourH` no trecho acima é, então, a operação <xref:microsoft.quantum.intrinsic.h> , de modo que podemos chamar esse valor como qualquer outra operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-332">The value of the variable `ourH` in the snippet above is then the operation <xref:microsoft.quantum.intrinsic.h>, such that we can call that value like any other operation.</span></span>
<span data-ttu-id="d2d52-333">Isso nos permite escrever operações que usam operações como parte de sua entrada, formando conceitos de fluxo de controle de ordem mais alta.</span><span class="sxs-lookup"><span data-stu-id="d2d52-333">This allows us to write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="d2d52-334">Por exemplo, podemos imaginar que queira "quadrado" uma operação aplicando-a duas vezes ao mesmo qubit de destino.</span><span class="sxs-lookup"><span data-stu-id="d2d52-334">For instance, we could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a><span data-ttu-id="d2d52-335">Retornando operações de uma função</span><span class="sxs-lookup"><span data-stu-id="d2d52-335">Returning operations from a function</span></span>

<span data-ttu-id="d2d52-336">Enfatizamos que também podemos retornar operações como parte das saídas, de modo que possamos isolar alguns tipos de lógica condicional clássica como uma função clássica que retorna uma descrição de um programa Quantum na forma de uma operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-336">We emphasize that we can also return operations as a part of outputs, such that we can isolate some kinds of classical conditional logic as a classical function which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="d2d52-337">Como exemplo simples, considere o exemplo de teleportação, no qual a parte que recebe uma mensagem clássica de dois bits precisa usar a mensagem para decodificar seu qubit no estado de Teleporta adequado.</span><span class="sxs-lookup"><span data-stu-id="d2d52-337">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="d2d52-338">Poderíamos escrever isso em termos de uma função que pega esses dois bits clássicos e retorna a operação de decodificação adequada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-338">We could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

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

<span data-ttu-id="d2d52-339">Essa nova função é realmente uma função, já que, se o chamarmos com os mesmos valores de `hereBit` e `thereBit` , sempre retornaremos a mesma operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-339">This new function is indeed a function, in that if we call it with the same values of `hereBit` and `thereBit`, we will always get back the same operation.</span></span>
<span data-ttu-id="d2d52-340">Assim, o decodificador pode ser executado com segurança dentro de operações sem ter que ter por motivo de como a lógica de decodificação interage com as definições das diferentes especializações de operação.</span><span class="sxs-lookup"><span data-stu-id="d2d52-340">Thus, the decoder can be safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="d2d52-341">Ou seja, isolamos a lógica clássica dentro de uma função, garantindo ao compilador que a chamada de função pode ser reordenada com impunity, desde que a entrada seja preservada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-341">That is, we have isolated the classical logic inside a function, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>


## <a name="partial-application"></a><span data-ttu-id="d2d52-342">Aplicativo parcial</span><span class="sxs-lookup"><span data-stu-id="d2d52-342">Partial Application</span></span>

<span data-ttu-id="d2d52-343">Podemos fazer significativamente mais com funções que retornam operações usando o *aplicativo parcial*, no qual podemos fornecer uma ou mais partes da entrada a uma função ou operação sem realmente chamá-la.</span><span class="sxs-lookup"><span data-stu-id="d2d52-343">We can do significantly more with functions that return operations by using *partial application*, in which we can provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="d2d52-344">Por exemplo, rechamar o `ApplyTwice` exemplo acima, podemos indicar que não queremos especificar, imediatamente, a qual qubit a operação de entrada deve ser aplicada:</span><span class="sxs-lookup"><span data-stu-id="d2d52-344">For example, recalling the `ApplyTwice` example above, we can indicate that we don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="d2d52-345">Nesse caso, a variável local `twiceOp` mantém a operação parcialmente aplicada `ApplyTwice(op, _)` , em que partes da entrada que ainda não foram especificadas são indicadas por `_` .</span><span class="sxs-lookup"><span data-stu-id="d2d52-345">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where parts of the input that have not yet been specified are indicated by `_`.</span></span>
<span data-ttu-id="d2d52-346">Quando realmente chamamos `twiceOp` na próxima linha, passamos como entrada para a operação parcialmente aplicada todas as partes restantes da entrada para a operação original.</span><span class="sxs-lookup"><span data-stu-id="d2d52-346">When we actually call `twiceOp` in the next line, we pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="d2d52-347">Portanto, o trecho acima é efetivamente idêntico a ter chamado `ApplyTwice(op, target)` diretamente, salvar para que tenhamos introduzido uma nova variável local que nos permite atrasar a chamada enquanto fornece algumas partes da entrada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-347">Thus, the above snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that we have introduced a new local variable that allows us to delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="d2d52-348">Como uma operação que foi parcialmente aplicada não é realmente chamada até que toda a sua entrada tenha sido fornecida, podemos aplicar operações parcialmente de forma segura, mesmo a partir de funções.</span><span class="sxs-lookup"><span data-stu-id="d2d52-348">Since an operation that has been partially applied is not actually called until its entire input has been provided, we can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="d2d52-349">Em princípio, a lógica clássica dentro `SquareOperation` poderia ter sido muito mais envolvida, mas ainda é isolada do restante de uma operação pelas garantias que o compilador pode oferecer sobre as funções.</span><span class="sxs-lookup"><span data-stu-id="d2d52-349">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span>
<span data-ttu-id="d2d52-350">Essa abordagem será usada em toda a biblioteca padrão de Q # para expressar o fluxo de controle clássico de forma que possa ser prontamente usada em programas Quantum.</span><span class="sxs-lookup"><span data-stu-id="d2d52-350">This approach will be used throughout the Q# standard library for expressing classical control flow in a way that can be readily used within quantum programs.</span></span>


## <a name="recursion"></a><span data-ttu-id="d2d52-351">Recursão</span><span class="sxs-lookup"><span data-stu-id="d2d52-351">Recursion</span></span>

<span data-ttu-id="d2d52-352">Os chamadores do Q # podem ser recursivos direta ou indiretamente.</span><span class="sxs-lookup"><span data-stu-id="d2d52-352">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="d2d52-353">Ou seja, uma operação ou função pode chamar a si mesma ou chamar outro callable que chama direta ou indiretamente a operação que pode ser chamada.</span><span class="sxs-lookup"><span data-stu-id="d2d52-353">That is, an operation or function may call itself, or it may call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="d2d52-354">No entanto, há dois comentários importantes sobre o uso da recursão:</span><span class="sxs-lookup"><span data-stu-id="d2d52-354">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="d2d52-355">O uso da recursão nas operações provavelmente interfere em determinadas otimizações.</span><span class="sxs-lookup"><span data-stu-id="d2d52-355">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="d2d52-356">Isso pode ter um impacto significativo no tempo de execução do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="d2d52-356">This may have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="d2d52-357">Ao executar em um dispositivo Quantum real, o espaço de pilha pode ser limitado e, portanto, a recursão profunda pode levar a um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d2d52-357">When executing on an actual quantum device, stack space may be limited, and so deep recursion may lead to a runtime error.</span></span>
  <span data-ttu-id="d2d52-358">Em particular, o compilador e o tempo de execução do Q # não identificam e otimizam a recursão da cauda.</span><span class="sxs-lookup"><span data-stu-id="d2d52-358">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="whats-next"></a><span data-ttu-id="d2d52-359">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="d2d52-359">What's Next?</span></span>
<span data-ttu-id="d2d52-360">Saiba mais sobre [variáveis](xref:microsoft.quantum.guide.variables) em Q #.</span><span class="sxs-lookup"><span data-stu-id="d2d52-360">Learn about [Variables](xref:microsoft.quantum.guide.variables) in Q#.</span></span>