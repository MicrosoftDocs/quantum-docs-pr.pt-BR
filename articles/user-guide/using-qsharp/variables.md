---
title: 'Variáveis em Q #'
description: Descrição do preenchimento
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
ms.openlocfilehash: 456c05d4ca66a747e0cc514a30c6bbb33610f481
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327774"
---
# <a name="variables-in-q"></a><span data-ttu-id="54ca3-103">Variáveis em Q #</span><span class="sxs-lookup"><span data-stu-id="54ca3-103">Variables in Q#</span></span>

<span data-ttu-id="54ca3-104">Q # distingue entre símbolos mutáveis e imutáveis, ou "Variables", que são associados/atribuídos a expressões.</span><span class="sxs-lookup"><span data-stu-id="54ca3-104">Q# distinguishes between mutable and immutable symbols, or "variables", which are bound/assigned to expressions.</span></span>
<span data-ttu-id="54ca3-105">Em geral, o uso de símbolos imutáveis é incentivado porque permite que o compilador execute mais otimizações.</span><span class="sxs-lookup"><span data-stu-id="54ca3-105">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="54ca3-106">O lado esquerdo de uma associação consiste em uma tupla de símbolos e no lado direito de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="54ca3-106">The left-hand-side of a binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

## <a name="immutable-variables"></a><span data-ttu-id="54ca3-107">Variáveis imutáveis</span><span class="sxs-lookup"><span data-stu-id="54ca3-107">Immutable Variables</span></span>

<span data-ttu-id="54ca3-108">Um valor de qualquer tipo em Q # pode ser atribuído a uma variável para reutilização em uma operação ou função usando a `let` palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="54ca3-108">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>

<span data-ttu-id="54ca3-109">Uma associação imutável consiste na palavra-chave `let` , seguida por uma tupla de símbolo ou símbolo, um sinal de igual `=` , uma expressão para associar os símbolos a e um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="54ca3-109">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="54ca3-110">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="54ca3-110">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="54ca3-111">Isso atribui uma determinada matriz de operadores Pauli ao nome da variável (ou "Symbol"), `measurementOperator` .</span><span class="sxs-lookup"><span data-stu-id="54ca3-111">This assigns a particular array of Pauli operators to the variable name (or "symbol"), `measurementOperator`.</span></span>

> [!NOTE]
> <span data-ttu-id="54ca3-112">Não precisamos especificar explicitamente o tipo da nossa nova variável, uma vez que a expressão no lado direito da `let` instrução não é ambígua e o tipo é inferido pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="54ca3-112">We did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="54ca3-113">As variáveis definidas usando `let` são *imutáveis*, o que significa que, uma vez definida, ela não pode mais ser alterada de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="54ca3-113">Variables defined using `let` are *immutable*, meaning that once it has been defined, it can no longer be changed in any way.</span></span>
<span data-ttu-id="54ca3-114">Isso permite várias otimizações úteis, incluindo a otimização da lógica clássica que atua em variáveis a serem reordenadas para aplicar a `Adjoint` variante de uma operação.</span><span class="sxs-lookup"><span data-stu-id="54ca3-114">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

## <a name="mutable-variables"></a><span data-ttu-id="54ca3-115">Variáveis mutáveis</span><span class="sxs-lookup"><span data-stu-id="54ca3-115">Mutable Variables</span></span>

<span data-ttu-id="54ca3-116">Como alternativa à criação de uma variável com `let` , a `mutable` palavra-chave criará uma variável mutável que *pode* ser revinculada depois de ser inicialmente criada usando `set` -se a palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="54ca3-116">As an alternative to creating a variable with `let`, the `mutable` keyword will create a mutable variable that *can* be re-bound after it is initially created by using the `set` keyword.</span></span>

<span data-ttu-id="54ca3-117">Símbolos declarados e associados como parte de uma `mutable` instrução podem ser reassociados a um valor diferente posteriormente no código.</span><span class="sxs-lookup"><span data-stu-id="54ca3-117">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> <span data-ttu-id="54ca3-118">Se um símbolo for reassociado mais tarde no código, seu tipo não será alterado e o valor vinculado recentemente precisará ser compatível com esse tipo.</span><span class="sxs-lookup"><span data-stu-id="54ca3-118">If a symbol is rebound later in the code, its type does not change, and the newly bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="54ca3-119">Reassociação de símbolos mutáveis</span><span class="sxs-lookup"><span data-stu-id="54ca3-119">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="54ca3-120">Uma variável mutável pode ser reassociada usando uma `set` instrução.</span><span class="sxs-lookup"><span data-stu-id="54ca3-120">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="54ca3-121">Essa reassociação consiste na palavra-chave `set` , seguida por uma tupla de símbolo ou símbolo, um sinal de igual `=` , uma expressão para reassociar os símbolos a e um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="54ca3-121">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="54ca3-122">Aqui, fornecemos alguns exemplos possíveis de técnicas de instrução de reassociação</span><span class="sxs-lookup"><span data-stu-id="54ca3-122">Here, we provide some possible examples of rebinding statement techniques</span></span>

### <a name="apply-and-reassign-statements"></a><span data-ttu-id="54ca3-123">Instruções de aplicar e reatribuir</span><span class="sxs-lookup"><span data-stu-id="54ca3-123">Apply-and-Reassign Statements</span></span>

<span data-ttu-id="54ca3-124">Um tipo específico de `set` instrução que chamamos de instrução de *aplicação e reatribuição* fornece uma maneira conveniente de concatenação se o lado direito consistir no aplicativo de um operador binário e o resultado for ser reassociado ao argumento esquerdo para o operador.</span><span class="sxs-lookup"><span data-stu-id="54ca3-124">A particular kind of `set`-statement we refer to as an *apply-and-reassign* statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="54ca3-125">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="54ca3-125">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="54ca3-126">incrementa o valor do contador `counter` em cada iteração do `for` loop.</span><span class="sxs-lookup"><span data-stu-id="54ca3-126">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="54ca3-127">O código acima é equivalente a</span><span class="sxs-lookup"><span data-stu-id="54ca3-127">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

<span data-ttu-id="54ca3-128">Instruções semelhantes estão disponíveis para todos os operadores binários nos quais o tipo do lado esquerdo corresponde ao tipo de expressão.</span><span class="sxs-lookup"><span data-stu-id="54ca3-128">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="54ca3-129">Isso fornece, por exemplo, uma maneira conveniente de acumular valores.</span><span class="sxs-lookup"><span data-stu-id="54ca3-129">This provides for example a convenient way to accumulate values.</span></span>

<span data-ttu-id="54ca3-130">Por exemplo, suponhamos `qubits` é um regsiter de qubits:</span><span class="sxs-lookup"><span data-stu-id="54ca3-130">For example, supposing `qubits` is a regsiter of qubits:</span></span>
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

### <a name="update-and-reassign-statements"></a><span data-ttu-id="54ca3-131">Instruções UPDATE-and-REASSIGN</span><span class="sxs-lookup"><span data-stu-id="54ca3-131">Update-and-Reassign Statements</span></span>

<span data-ttu-id="54ca3-132">Existe uma concatenação semelhante para [expressões de copiar e atualizar](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) no lado direito.</span><span class="sxs-lookup"><span data-stu-id="54ca3-132">A similar concatenation exists for [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) on the right-hand-side.</span></span>
<span data-ttu-id="54ca3-133">De modo correspondente, as instruções *Update-and-REASSIGN* existem para *itens nomeados* em tipos definidos pelo usuário, bem como para *itens de matriz*.</span><span class="sxs-lookup"><span data-stu-id="54ca3-133">Correspondingly, *update-and-reassign* statements exist for *named items* in user-defined types as well as for *array items*.</span></span>  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

<span data-ttu-id="54ca3-134">No caso de matrizes, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) em nossas bibliotecas padrão fornece as ferramentas necessárias para muitas necessidades comuns de inicialização e manipulação de matriz e, portanto, ajudam a evitar a necessidade de atualizar itens de matriz em primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="54ca3-134">In the case of arrays, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) in our standard libraries provides the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> 

<span data-ttu-id="54ca3-135">As instruções UPDATE-and-REASSIGN fornecem uma alternativa, se necessário:</span><span class="sxs-lookup"><span data-stu-id="54ca3-135">Update-and-reassign statements provide an alternative if needed:</span></span>

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

<span data-ttu-id="54ca3-136">Usando as ferramentas de biblioteca para matrizes fornecidas no [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) , podemos, por exemplo, definir facilmente uma função que retorna uma matriz de Paulis em que o Pauli no índice `i` usa o valor determinado e todas as outras entradas são a identidade.</span><span class="sxs-lookup"><span data-stu-id="54ca3-136">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can, for example, easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity.</span></span>

<span data-ttu-id="54ca3-137">Aqui estão duas definições dessa função, com a segunda aproveitando as ferramentas em nossa disposição.</span><span class="sxs-lookup"><span data-stu-id="54ca3-137">Here are two definitions of such a function, with the second taking advantage of the tools at our disposal.</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli or PauliI dep. on whether index==location
    }    
    return pauliArray;
}
```

<span data-ttu-id="54ca3-138">Em vez de iterar em cada índice na matriz e defini-la condicionalmente como `PauliI` or `Pauli` , podemos usar `ConstantArray` de [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) para criar uma matriz de e, `PauliI` em seguida, simplesmente retornar uma expressão Copy-and-Update, na qual alteramos o valor específico no índice `location` :</span><span class="sxs-lookup"><span data-stu-id="54ca3-138">Instead of iterating over each index in the array, and conditionally setting it to `PauliI` or `Pauli`, we can instead use `ConstantArray` from [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) to create an array of `PauliI`'s, and then simply returning a copy-and-update expression in which we've changed the specifc value at index `location`:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a><span data-ttu-id="54ca3-139">Desconstrução de tupla</span><span class="sxs-lookup"><span data-stu-id="54ca3-139">Tuple Deconstruction</span></span>

<span data-ttu-id="54ca3-140">Além de atribuir uma única variável, as `let` `mutable` palavras-chave e---ou, na verdade, qualquer outro constructo de associação, como `set` (descrito abaixo),---também permitir o desempacotamento do conteúdo de um [tipo de tupla](xref:microsoft.quantum.guide.types#tuple-types).</span><span class="sxs-lookup"><span data-stu-id="54ca3-140">In addition to assigning a single variable, the `let` and `mutable` keywords---or in fact any other binding construct, such as `set` (described below)---also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.guide.types#tuple-types).</span></span>
<span data-ttu-id="54ca3-141">Uma atribuição desse formulário é mencionada para *desconstruir* os elementos dessa tupla.</span><span class="sxs-lookup"><span data-stu-id="54ca3-141">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>

<span data-ttu-id="54ca3-142">Se o lado direito da associação for uma tupla, essa tupla poderá ser desconstruída após a atribuição.</span><span class="sxs-lookup"><span data-stu-id="54ca3-142">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="54ca3-143">Essas desconstruções podem envolver tuplas aninhadas e qualquer desconstrução completa ou parcial é válida, desde que a forma da tupla no lado direito seja compatível com a forma da tupla de símbolo.</span><span class="sxs-lookup"><span data-stu-id="54ca3-143">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>

<span data-ttu-id="54ca3-144">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="54ca3-144">For example:</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a><span data-ttu-id="54ca3-145">Escopos de associação</span><span class="sxs-lookup"><span data-stu-id="54ca3-145">Binding Scopes</span></span>

<span data-ttu-id="54ca3-146">Em geral, as ligações de símbolo saem do escopo e se tornam inoperantes no final do bloco de instrução em que ocorrem.</span><span class="sxs-lookup"><span data-stu-id="54ca3-146">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="54ca3-147">Há duas exceções a essa regra:</span><span class="sxs-lookup"><span data-stu-id="54ca3-147">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="54ca3-148">A associação da variável loop de um `for` loop está no escopo do corpo do loop for, mas não após o final do loop.</span><span class="sxs-lookup"><span data-stu-id="54ca3-148">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="54ca3-149">Todas as três partes de um `repeat` / `until` loop (o corpo, o teste e a correção) são tratadas como um único escopo, de modo que os símbolos associados ao corpo estão disponíveis no teste e na correção.</span><span class="sxs-lookup"><span data-stu-id="54ca3-149">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="54ca3-150">Para ambos os tipos de loops, cada passagem do loop é executada em seu próprio escopo, portanto, as associações de uma passagem anterior não estarão disponíveis em uma passagem posterior.</span><span class="sxs-lookup"><span data-stu-id="54ca3-150">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>
<span data-ttu-id="54ca3-151">Os detalhes sobre esses loops podem ser encontrados no [fluxo de controle](xref:microsoft.quantum.guide.controlflow).</span><span class="sxs-lookup"><span data-stu-id="54ca3-151">Details on these loops can be found at [Control Flow](xref:microsoft.quantum.guide.controlflow).</span></span>

<span data-ttu-id="54ca3-152">Associações de símbolo de blocos externos são herdadas por blocos internos.</span><span class="sxs-lookup"><span data-stu-id="54ca3-152">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="54ca3-153">Um símbolo só pode ser associado uma vez por bloco; é ilegal definir um símbolo com o mesmo nome de outro símbolo que está dentro do escopo (sem "sombreamento").</span><span class="sxs-lookup"><span data-stu-id="54ca3-153">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="54ca3-154">As sequências a seguir seriam legais:</span><span class="sxs-lookup"><span data-stu-id="54ca3-154">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="54ca3-155">e</span><span class="sxs-lookup"><span data-stu-id="54ca3-155">and</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
...                 // n is not bound to a value
```

<span data-ttu-id="54ca3-156">Mas isso seria ilegal:</span><span class="sxs-lookup"><span data-stu-id="54ca3-156">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="54ca3-157">como seria:</span><span class="sxs-lookup"><span data-stu-id="54ca3-157">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="next-steps"></a><span data-ttu-id="54ca3-158">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="54ca3-158">Next steps</span></span>

<span data-ttu-id="54ca3-159">Saiba mais sobre como [trabalhar com qubits](xref:microsoft.quantum.guide.qubits) em Q #.</span><span class="sxs-lookup"><span data-stu-id="54ca3-159">Learn about [Working With Qubits](xref:microsoft.quantum.guide.qubits) in Q#.</span></span>