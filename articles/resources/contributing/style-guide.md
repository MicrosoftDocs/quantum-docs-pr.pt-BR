---
title: Guia de estilo da Microsoft Q#
description: Aprenda as convenções de nomenclatura, entrada, documentação e formatação para Q# programas e bibliotecas.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
no-loc:
- Q#
- $$v
ms.openlocfilehash: fef3cea1c11e4fef49ddbf63adb34e07675049d2
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834186"
---
# <a name="no-locq-style-guide"></a><span data-ttu-id="13891-103">Q# Guia de estilo</span><span class="sxs-lookup"><span data-stu-id="13891-103">Q# Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="13891-104">Convenções gerais</span><span class="sxs-lookup"><span data-stu-id="13891-104">General Conventions</span></span> ##

<span data-ttu-id="13891-105">As convenções sugeridas neste guia destinam-se a ajudar a tornar os programas e bibliotecas escritos Q# mais facilmente para serem lidos e compreendidos.</span><span class="sxs-lookup"><span data-stu-id="13891-105">The conventions suggested in this guide are intended to help make programs and libraries written in Q# easier to read and understand.</span></span>

## <a name="guidance"></a><span data-ttu-id="13891-106">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-106">Guidance</span></span>

<span data-ttu-id="13891-107">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-107">We suggest:</span></span>

- <span data-ttu-id="13891-108">Nunca desconsidere uma convenção, a menos que você esteja fazendo isso intencionalmente para fornecer código mais legível e compreensível para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="13891-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

## <a name="naming-conventions"></a><span data-ttu-id="13891-109">Convenções de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="13891-109">Naming Conventions</span></span> ##

<span data-ttu-id="13891-110">Na oferta do kit de desenvolvimento Quantum, nos esforçamos os nomes de função e operação que ajudam os desenvolvedores da Quantum a escrever programas que são fáceis de ler e que minimizam a surpresa.</span><span class="sxs-lookup"><span data-stu-id="13891-110">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="13891-111">Uma parte importante disso é que, quando escolhemos nomes para funções, operações e tipos, estamos estabelecendo o *vocabulário* que os programadores usam para expressar conceitos de Quantum; com nossas opções, nós nos ajudamos ou nos atrapalhamos em seus esforços para se comunicar claramente.</span><span class="sxs-lookup"><span data-stu-id="13891-111">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="13891-112">Isso faz com que a empresa tenha a certeza de que os nomes que apresentamos oferecem clareza, em vez de obscurecimento.</span><span class="sxs-lookup"><span data-stu-id="13891-112">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="13891-113">Nesta seção, detalhamos como atendemos a essa obrigação em termos de diretrizes explícitas que nos ajudam a fazer o melhor da Q# comunidade de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="13891-113">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the Q# development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="13891-114">Operações e funções</span><span class="sxs-lookup"><span data-stu-id="13891-114">Operations and Functions</span></span> ###

<span data-ttu-id="13891-115">Uma das primeiras coisas que um nome deve estabelecer é se um determinado símbolo representa uma função ou uma operação.</span><span class="sxs-lookup"><span data-stu-id="13891-115">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="13891-116">A diferença entre funções e operações é essencial para entender como um bloco de código se comporta.</span><span class="sxs-lookup"><span data-stu-id="13891-116">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="13891-117">Para comunicar a distinção entre as funções e as operações para os usuários, nós nos deparamos com Q# o uso de efeitos colaterais nos modelos.</span><span class="sxs-lookup"><span data-stu-id="13891-117">To communicate the distinction between functions and operations to users, we rely on that Q# models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="13891-118">Ou seja, uma operação *faz* algo.</span><span class="sxs-lookup"><span data-stu-id="13891-118">That is, an operation *does* something.</span></span>

<span data-ttu-id="13891-119">Por outro lado, as funções descrevem as relações matemáticas entre os dados.</span><span class="sxs-lookup"><span data-stu-id="13891-119">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="13891-120">A expressão `Sin(PI() / 2.0)` *é* `1.0` e não implica nada sobre o estado de um programa ou seu qubits.</span><span class="sxs-lookup"><span data-stu-id="13891-120">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="13891-121">Resumindo, as operações fazem coisas enquanto as funções são coisas.</span><span class="sxs-lookup"><span data-stu-id="13891-121">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="13891-122">Essa distinção sugere que nós nomeamos operações como verbos e funções como substantivos.</span><span class="sxs-lookup"><span data-stu-id="13891-122">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="13891-123">Quando um tipo definido pelo usuário é declarado, uma nova função que constrói instâncias desse tipo é definida implicitamente ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="13891-123">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="13891-124">Dessa perspectiva, os tipos definidos pelo usuário devem ser nomeados como substantivos para que o próprio tipo e a função de Construtor tenham nomes consistentes.</span><span class="sxs-lookup"><span data-stu-id="13891-124">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="13891-125">Quando for razoável, certifique-se de que os nomes de operação comecem com verbos que indiquem claramente o efeito assumido pela operação.</span><span class="sxs-lookup"><span data-stu-id="13891-125">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="13891-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="13891-126">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="13891-127">Um caso que merece menção especial é quando uma operação usa outra operação como entrada e a chama.</span><span class="sxs-lookup"><span data-stu-id="13891-127">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="13891-128">Nesses casos, a ação tomada pela operação de entrada não é clara quando a operação externa é definida, de modo que o verbo direito não é limpo imediatamente.</span><span class="sxs-lookup"><span data-stu-id="13891-128">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="13891-129">Recomendamos o verbo `Apply` , como em `ApplyIf` , `ApplyToEach` e `ApplyToFirst` .</span><span class="sxs-lookup"><span data-stu-id="13891-129">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="13891-130">Outros verbos também podem ser úteis nesse caso, como em `IterateThroughCartesianPower` .</span><span class="sxs-lookup"><span data-stu-id="13891-130">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="13891-131">Verbo</span><span class="sxs-lookup"><span data-stu-id="13891-131">Verb</span></span> | <span data-ttu-id="13891-132">Efeito esperado</span><span class="sxs-lookup"><span data-stu-id="13891-132">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="13891-133">Aplicar</span><span class="sxs-lookup"><span data-stu-id="13891-133">Apply</span></span> | <span data-ttu-id="13891-134">Uma operação fornecida como entrada é chamada</span><span class="sxs-lookup"><span data-stu-id="13891-134">An operation provided as input is called</span></span> |
| <span data-ttu-id="13891-135">Assert</span><span class="sxs-lookup"><span data-stu-id="13891-135">Assert</span></span> | <span data-ttu-id="13891-136">Uma hipótese sobre o resultado de uma possível medição de Quantum é verificada por um simulador</span><span class="sxs-lookup"><span data-stu-id="13891-136">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="13891-137">Estimativa</span><span class="sxs-lookup"><span data-stu-id="13891-137">Estimate</span></span> | <span data-ttu-id="13891-138">Um valor clássico é retornado, representando uma estimativa desenhada de uma ou mais medições</span><span class="sxs-lookup"><span data-stu-id="13891-138">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="13891-139">Medida</span><span class="sxs-lookup"><span data-stu-id="13891-139">Measure</span></span> | <span data-ttu-id="13891-140">Uma medida do Quantum é executada e seu resultado é retornado para o usuário</span><span class="sxs-lookup"><span data-stu-id="13891-140">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="13891-141">Preparar</span><span class="sxs-lookup"><span data-stu-id="13891-141">Prepare</span></span> | <span data-ttu-id="13891-142">Um determinado registro de qubits é inicializado em um estado específico</span><span class="sxs-lookup"><span data-stu-id="13891-142">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="13891-143">Amostra</span><span class="sxs-lookup"><span data-stu-id="13891-143">Sample</span></span> | <span data-ttu-id="13891-144">Um valor clássico é retornado aleatoriamente de alguma distribuição</span><span class="sxs-lookup"><span data-stu-id="13891-144">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="13891-145">Para funções, sugerimos evitar o uso de verbos em favor de substantivos comuns (consulte as diretrizes sobre os nomes apropriados abaixo) ou adjetivos:</span><span class="sxs-lookup"><span data-stu-id="13891-145">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="13891-146">Em particular, em quase todos os casos, sugerimos usar participles anteriores, quando apropriado, para indicar que um nome de função está firmemente conectado a uma ação ou efeito colateral em outro lugar em um programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="13891-146">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="13891-147">Por exemplo,  `ControlledOnInt` usa a forma de particípio da parte do verbo "Control" para indicar que a função atua como um adjetivo para modificar seu argumento.</span><span class="sxs-lookup"><span data-stu-id="13891-147">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="13891-148">Esse nome tem o benefício adicional de corresponder a semântica do `Controlled` functor interno, conforme discutido abaixo.</span><span class="sxs-lookup"><span data-stu-id="13891-148">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="13891-149">Da mesma forma, os _substantivos do agente_ podem ser usados para construir nomes de função e UDT a partir de nomes de operação, como no caso do nome `Encoder` de um UDT que esteja fortemente associado a `Encode` .</span><span class="sxs-lookup"><span data-stu-id="13891-149">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="13891-150">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-150">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-151">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-151">We suggest:</span></span>

- <span data-ttu-id="13891-152">Use verbos para nomes de operação.</span><span class="sxs-lookup"><span data-stu-id="13891-152">Use verbs for operation names.</span></span>
- <span data-ttu-id="13891-153">Use substantivos ou adjetivos para nomes de função.</span><span class="sxs-lookup"><span data-stu-id="13891-153">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="13891-154">Use substantivos para atributos e tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="13891-154">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="13891-155">Para todos os nomes que podem ser chamados, use `CamelCase` de preferência forte para `pascalCase` , `snake_case` ou `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="13891-155">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="13891-156">Em particular, verifique se os nomes que podem ser chamados começam com letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="13891-156">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="13891-157">Para todas as variáveis locais, use `pascalCase` de preferência forte para `CamelCase` , `snake_case` ou `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="13891-157">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="13891-158">Em particular, verifique se as variáveis locais começam com letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="13891-158">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="13891-159">Evite o uso de sublinhados `_` em nomes de função e de operação; em que níveis adicionais de hierarquia são necessários, use namespaces e aliases de namespace.</span><span class="sxs-lookup"><span data-stu-id="13891-159">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-160">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-160">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="13891-161">Name</span><span class="sxs-lookup"><span data-stu-id="13891-161">Name</span></span> | <span data-ttu-id="13891-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="13891-162">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="13891-163">☑</span><span class="sxs-lookup"><span data-stu-id="13891-163">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="13891-164">Limpar o uso de um verbo ("refletir") para indicar o efeito da operação.</span><span class="sxs-lookup"><span data-stu-id="13891-164">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="13891-165">☒</span><span class="sxs-lookup"><span data-stu-id="13891-165">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="13891-166">O uso da frase de substantivo sugere a função, em vez da operação.</span><span class="sxs-lookup"><span data-stu-id="13891-166">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="13891-167">☒</span><span class="sxs-lookup"><span data-stu-id="13891-167">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="13891-168">Uso de `snake_case` Q# notação contravenes.</span><span class="sxs-lookup"><span data-stu-id="13891-168">Use of `snake_case` contravenes Q# notation.</span></span> |
| <span data-ttu-id="13891-169">☒</span><span class="sxs-lookup"><span data-stu-id="13891-169">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="13891-170">Uso de sublinhados internos para a notação de contravenes de nome de operação Q# .</span><span class="sxs-lookup"><span data-stu-id="13891-170">Use of underscores internal to operation name contravenes Q# notation.</span></span> |
| <span data-ttu-id="13891-171">☑</span><span class="sxs-lookup"><span data-stu-id="13891-171">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="13891-172">O uso de frase de substantivo sugere que a função retorna uma operação.</span><span class="sxs-lookup"><span data-stu-id="13891-172">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="13891-173">☑</span><span class="sxs-lookup"><span data-stu-id="13891-173">☑</span></span> | `function EqualityFact` | <span data-ttu-id="13891-174">Limpe o uso de substantivo ("Fact") para indicar que essa é uma função, enquanto o adjetivo.</span><span class="sxs-lookup"><span data-stu-id="13891-174">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="13891-175">☒</span><span class="sxs-lookup"><span data-stu-id="13891-175">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="13891-176">O uso de verbo ("Get") sugere que se trata de uma operação.</span><span class="sxs-lookup"><span data-stu-id="13891-176">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="13891-177">☑</span><span class="sxs-lookup"><span data-stu-id="13891-177">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="13891-178">O uso de frase de substantivo claramente se refere ao resultado da chamada do Construtor UDT.</span><span class="sxs-lookup"><span data-stu-id="13891-178">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="13891-179">☒</span><span class="sxs-lookup"><span data-stu-id="13891-179">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="13891-180">O uso de frase verbal sugere que o Construtor UDT é uma operação.</span><span class="sxs-lookup"><span data-stu-id="13891-180">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="13891-181">☑</span><span class="sxs-lookup"><span data-stu-id="13891-181">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="13891-182">O uso de frase de substantivo comunica o uso do atributo.</span><span class="sxs-lookup"><span data-stu-id="13891-182">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="entry-points"></a><span data-ttu-id="13891-183">Pontos de entrada</span><span class="sxs-lookup"><span data-stu-id="13891-183">Entry Points</span></span>

<span data-ttu-id="13891-184">Ao definir um ponto de entrada em um Q# programa, o Q# compilador reconhece o [ `@EntryPoint()` atributo](xref:microsoft.quantum.core.entrypoint) , exigindo que os pontos de entrada tenham um nome específico (por exemplo: `main` , `Main` ou `__main__` ).</span><span class="sxs-lookup"><span data-stu-id="13891-184">When defining an entry point into a Q# program, the Q# compiler recognizes the [`@EntryPoint()` attribute](xref:microsoft.quantum.core.entrypoint) rather requiring that entry points have a particular name (e.g.: `main`, `Main`, or `__main__`).</span></span>
<span data-ttu-id="13891-185">Ou seja, da perspectiva de um Q# desenvolvedor, os pontos de entrada são operações comuns anotadas com o `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="13891-185">That is, from the perspective of a Q# developer, entry points are ordinary operations annotated with `@EntryPoint()`.</span></span>
<span data-ttu-id="13891-186">Além disso, os Q# pontos de entrada podem ser pontos de entrada para um aplicativo inteiro (por exemplo, em Q# programas executáveis autônomos) ou podem ser uma interface entre um Q# programa e o programa host para um aplicativo (ou seja, ao usar Q# com Python ou .net), de modo que o nome "Main" possa ser equivocado quando aplicado a um Q# ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="13891-186">Moreover, Q# entry points may be entry points for an entire application (for example, in Q# standalone executable programs), or may be an interface between a Q# program and the host program for an application (i.e.: when using Q# with Python or .NET), such that the name "main" could be misleading when applied to a Q# entry point.</span></span>

<span data-ttu-id="13891-187">Sugerimos o uso de pontos de entrada de nomenclatura para refletir o uso do `@EntryPoint()` atributo usando o Conselho geral para as operações de nomenclatura listadas acima.</span><span class="sxs-lookup"><span data-stu-id="13891-187">We suggest using naming entry points to reflect the use of the `@EntryPoint()` attribute by using the general advice for naming operations listed above.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="13891-188">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-188">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-189">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-189">We suggest:</span></span>

- <span data-ttu-id="13891-190">Não nomeie operações de ponto de entrada como "Main".</span><span class="sxs-lookup"><span data-stu-id="13891-190">Do not name entry point operations as "main."</span></span>
- <span data-ttu-id="13891-191">Nome de operações de ponto de entrada como operações comuns.</span><span class="sxs-lookup"><span data-stu-id="13891-191">Name entry point operations as ordinary operations.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-192">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-192">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="13891-193">Name</span><span class="sxs-lookup"><span data-stu-id="13891-193">Name</span></span> | <span data-ttu-id="13891-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="13891-194">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="13891-195">☑</span><span class="sxs-lookup"><span data-stu-id="13891-195">☑</span></span> | `@EntryPoint() operation RunSimulation` | <span data-ttu-id="13891-196">Comunica claramente a finalidade do ponto de entrada por meio do nome da operação.</span><span class="sxs-lookup"><span data-stu-id="13891-196">Clearly communicates purpose of entry point through operation name.</span></span> |
| <span data-ttu-id="13891-197">☒</span><span class="sxs-lookup"><span data-stu-id="13891-197">☒</span></span> | <s>`@EntryPoint() operation Main`</s> | <span data-ttu-id="13891-198">O uso de `Main` não comunica claramente a finalidade do ponto de entrada e é redundante com o `@EntryPoint()` atributo.</span><span class="sxs-lookup"><span data-stu-id="13891-198">Use of `Main` doesn't clearly communicate purpose of entry point, and is redundant with `@EntryPoint()` attribute.</span></span> |

***

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="13891-199">Abreviação e abreviações</span><span class="sxs-lookup"><span data-stu-id="13891-199">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="13891-200">O aviso acima não obstante, há muitas formas de abreviação que vêem o uso comum e generalizado na computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="13891-200">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="13891-201">Sugerimos usar a abreviação existente e comum onde ela existe, especialmente para operações intrínsecas à operação de um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="13891-201">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="13891-202">Por exemplo, escolhemos o nome `X` em vez de `ApplyX` e `Rz` em vez de `RotateAboutZ` .</span><span class="sxs-lookup"><span data-stu-id="13891-202">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="13891-203">Ao usar esse formato abreviado, os nomes de operação devem estar em letras maiúsculas (por exemplo: `MAJ` ).</span><span class="sxs-lookup"><span data-stu-id="13891-203">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="13891-204">É necessário ter cuidado ao aplicar essa Convenção no caso de acrônimos comumente usados e inicialismos como "QFT" para "transformação de Fourier do Quantum".</span><span class="sxs-lookup"><span data-stu-id="13891-204">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="13891-205">Sugerimos as seguintes convenções gerais do .NET para o uso de acrônimos e inicialismos em nomes completos, que prescrevem que:</span><span class="sxs-lookup"><span data-stu-id="13891-205">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="13891-206">acrônimos de duas letras e inicialismos são nomeados em letras maiúsculas (por exemplo: `BE` para "big-endian"),</span><span class="sxs-lookup"><span data-stu-id="13891-206">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="13891-207">todos os acrônimos mais longos e inicialismos são nomeados em `CamelCase` (por exemplo: `Qft` para "transformação de Fourier do Quantum")</span><span class="sxs-lookup"><span data-stu-id="13891-207">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="13891-208">Assim, uma operação que implementa o QFT poderia ser chamada de `QFT` abreviação ou escrita como `ApplyQft` .</span><span class="sxs-lookup"><span data-stu-id="13891-208">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="13891-209">Para operações e funções comumente usadas, pode ser desejável fornecer um nome abreviado como um _alias_ para um formulário mais longo:</span><span class="sxs-lookup"><span data-stu-id="13891-209">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[<span data-ttu-id="13891-210">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-210">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-211">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-211">We suggest:</span></span>

- <span data-ttu-id="13891-212">Considere os nomes abreviados comumente aceitos e amplamente usados quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="13891-212">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="13891-213">Use maiúsculas para abreviar.</span><span class="sxs-lookup"><span data-stu-id="13891-213">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="13891-214">Use letras maiúsculas para acrônimos curtos (duas letras) e inicialismos.</span><span class="sxs-lookup"><span data-stu-id="13891-214">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="13891-215">Use `CamelCase` para acrônimos mais longos (três ou mais letras) e inicialismos.</span><span class="sxs-lookup"><span data-stu-id="13891-215">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-216">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-216">Examples</span></span>](#tab/examples)

| &nbsp;   | <span data-ttu-id="13891-217">Name</span><span class="sxs-lookup"><span data-stu-id="13891-217">Name</span></span> | <span data-ttu-id="13891-218">Descrição</span><span class="sxs-lookup"><span data-stu-id="13891-218">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="13891-219">☑</span><span class="sxs-lookup"><span data-stu-id="13891-219">☑</span></span> | `X` | <span data-ttu-id="13891-220">Atalho bem compreendido para "aplicar uma transformação de $X $"</span><span class="sxs-lookup"><span data-stu-id="13891-220">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="13891-221">☑</span><span class="sxs-lookup"><span data-stu-id="13891-221">☑</span></span> | `CNOT` | <span data-ttu-id="13891-222">Atalho bem compreendido para "controlado-não"</span><span class="sxs-lookup"><span data-stu-id="13891-222">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="13891-223">☒</span><span class="sxs-lookup"><span data-stu-id="13891-223">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="13891-224">A abreviação não deve estar em `CamelCase` .</span><span class="sxs-lookup"><span data-stu-id="13891-224">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="13891-225">☑</span><span class="sxs-lookup"><span data-stu-id="13891-225">☑</span></span> | `ApplyQft` | <span data-ttu-id="13891-226">O início comum "QFT" aparece como parte de um nome de formato longo.</span><span class="sxs-lookup"><span data-stu-id="13891-226">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="13891-227">☑</span><span class="sxs-lookup"><span data-stu-id="13891-227">☑</span></span> | `QFT` | <span data-ttu-id="13891-228">O inicial comum "QFT" aparece como parte de um nome abreviado.</span><span class="sxs-lookup"><span data-stu-id="13891-228">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



***


### <a name="proper-nouns-in-names"></a><span data-ttu-id="13891-229">Substantivos próprios em nomes</span><span class="sxs-lookup"><span data-stu-id="13891-229">Proper Nouns in Names</span></span> ###

<span data-ttu-id="13891-230">Embora na física seja comum nomear coisas depois da primeira pessoa a publicar sobre elas, a maioria das não physicistss não está familiarizada com os nomes de todos e todo o histórico.</span><span class="sxs-lookup"><span data-stu-id="13891-230">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="13891-231">Depender muito muito nas convenções de nomenclatura da física pode, portanto, criar uma barreira substancial para a entrada, pois os usuários de outros planos de fundo devem aprender um grande número de nomes aparentemente opacos para usar operações e conceitos comuns.</span><span class="sxs-lookup"><span data-stu-id="13891-231">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="13891-232">Portanto, é recomendável que, sempre que for razoável, os substantivos comuns que descrevem um conceito seja adotado em preferência forte a nomes próprios incorretos que descrevem o histórico de publicação de um conceito.</span><span class="sxs-lookup"><span data-stu-id="13891-232">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="13891-233">Como um exemplo específico, a permuta controlada individualmente e as operações não controladas duplamente não são chamadas de operações "Fredkin" e "Toffoli" em literatura acadêmica, mas são identificadas Q# principalmente como `CSWAP` e `CCNOT` .</span><span class="sxs-lookup"><span data-stu-id="13891-233">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in Q# primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="13891-234">Em ambos os casos, os comentários de documentação da API fornecem nomes sinônimos com base em substantivos apropriados, juntamente com todas as citações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="13891-234">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="13891-235">Essa preferência é especialmente importante, uma vez que algum uso dos nomes apropriados sempre será necessário — Q# segue a tradição definida por muitas linguagens clássicas, por exemplo, e refere-se a `Bool` tipos em referência à lógica booliana, que, por sua vez, é nomeado em honrar a George bool.</span><span class="sxs-lookup"><span data-stu-id="13891-235">This preference is especially important given that some usage of proper nouns will always be necessary — Q# follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="13891-236">Alguns conceitos de Quantum da mesma forma são nomeados de maneira semelhante, incluindo o `Pauli` tipo interno à Q# linguagem.</span><span class="sxs-lookup"><span data-stu-id="13891-236">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the Q# language.</span></span>
<span data-ttu-id="13891-237">Ao minimizar o uso de substantivos apropriados em que esse uso não é essencial, reduzimos o impacto em que os nomes próprios não podem ser evitados de forma razoável.</span><span class="sxs-lookup"><span data-stu-id="13891-237">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="13891-238">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-238">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="13891-239">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-239">We suggest:</span></span>

- <span data-ttu-id="13891-240">Evite o uso de substantivos apropriados em nomes.</span><span class="sxs-lookup"><span data-stu-id="13891-240">Avoid the use of proper nouns in names.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-241">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-241">Examples</span></span>](#tab/examples)

***

### <a name="type-conversions"></a><span data-ttu-id="13891-242">Conversões de tipo</span><span class="sxs-lookup"><span data-stu-id="13891-242">Type Conversions</span></span> ###

<span data-ttu-id="13891-243">Como Q# é um idioma fortemente e com rigidez de tipos, um valor de um tipo só pode ser usado como um valor de outro tipo usando uma chamada explícita para uma função de conversão de tipo.</span><span class="sxs-lookup"><span data-stu-id="13891-243">Since Q# is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="13891-244">Isso é diferente de linguagens que permitem valores para alterar tipos implicitamente (por exemplo: promoção de tipos) ou por meio de conversão.</span><span class="sxs-lookup"><span data-stu-id="13891-244">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="13891-245">Como resultado, as funções de conversão de tipo desempenham um papel importante no Q# desenvolvimento da biblioteca e compõem uma das decisões mais comumente encontradas sobre a nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="13891-245">As a result, type conversion functions play an important role in Q# library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="13891-246">No entanto, observamos que, como as conversões de tipo são sempre _determinísticas_, elas podem ser escritas como funções e, portanto, se enquadram no Conselho acima.</span><span class="sxs-lookup"><span data-stu-id="13891-246">We note, however, that since type conversions are always _deterministic_, they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="13891-247">Em particular, sugerimos que as funções de conversão de tipo nunca devem ser nomeadas como verbos (por exemplo: `ConvertToX` ) ou advérbio frases preposicionais ( `ToX` ), mas devem ser nomeadas como frases preposicionais de adjetivo que indicam os tipos de origem e de destino ( `XAsY` ).</span><span class="sxs-lookup"><span data-stu-id="13891-247">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="13891-248">Ao listar tipos de matriz em nomes de função de conversão de tipo, recomendamos a abreviação `Arr` .</span><span class="sxs-lookup"><span data-stu-id="13891-248">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="13891-249">Ao bloquear circunstâncias excepcionais, recomendamos que todas as funções de conversão de tipo sejam nomeadas usando `As` para que possam ser identificadas rapidamente.</span><span class="sxs-lookup"><span data-stu-id="13891-249">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="13891-250">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-250">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-251">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-251">We suggest:</span></span>

- <span data-ttu-id="13891-252">Se uma função converter um valor do tipo `X` para um valor do tipo `Y` , use o nome `AsY` ou `XAsY` .</span><span class="sxs-lookup"><span data-stu-id="13891-252">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-253">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-253">Examples</span></span>](#tab/examples)

| &nbsp;   | <span data-ttu-id="13891-254">Name</span><span class="sxs-lookup"><span data-stu-id="13891-254">Name</span></span> | <span data-ttu-id="13891-255">Descrição</span><span class="sxs-lookup"><span data-stu-id="13891-255">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="13891-256">☒</span><span class="sxs-lookup"><span data-stu-id="13891-256">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="13891-257">A preposição "to" resulta em uma frase verbal, indicando uma operação e não uma função.</span><span class="sxs-lookup"><span data-stu-id="13891-257">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="13891-258">☒</span><span class="sxs-lookup"><span data-stu-id="13891-258">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="13891-259">O tipo de entrada não é claro do nome da função.</span><span class="sxs-lookup"><span data-stu-id="13891-259">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="13891-260">☒</span><span class="sxs-lookup"><span data-stu-id="13891-260">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="13891-261">Os tipos de entrada e saída aparecem na ordem errada.</span><span class="sxs-lookup"><span data-stu-id="13891-261">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="13891-262">☑</span><span class="sxs-lookup"><span data-stu-id="13891-262">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="13891-263">Os tipos de entrada e de saída são claros.</span><span class="sxs-lookup"><span data-stu-id="13891-263">Both the input types and output types are clear.</span></span> |

***

### <a name="private-or-internal-names"></a><span data-ttu-id="13891-264">Nomes privados ou internos</span><span class="sxs-lookup"><span data-stu-id="13891-264">Private or Internal Names</span></span> ###

<span data-ttu-id="13891-265">Em muitos casos, um nome destina-se estritamente ao uso interno de uma biblioteca ou projeto e não é uma parte garantida da API oferecida por uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="13891-265">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="13891-266">É útil indicar claramente que esse é o caso ao nomear funções e operações para que dependências acidentais em código somente interno sejam tornadas óbvias.</span><span class="sxs-lookup"><span data-stu-id="13891-266">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="13891-267">Se uma operação ou função não for destinada ao uso direto, mas, em vez disso, deve ser usada por um callable chamado que age por aplicativo parcial, considere usar um nome começando com a `internal` palavra-chave para o callable que é parcialmente aplicado.</span><span class="sxs-lookup"><span data-stu-id="13891-267">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with the `internal` keyword for the callable that is partially applied.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="13891-268">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-268">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-269">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-269">We suggest:</span></span>

- <span data-ttu-id="13891-270">Quando uma função, uma operação ou um tipo definido pelo usuário não faz parte da API pública para uma Q# biblioteca ou programa, verifique se ele está marcado como interno colocando a `internal` palavra-chave antes da `function` `operation` declaração, ou `newtype` .</span><span class="sxs-lookup"><span data-stu-id="13891-270">When a function, operation, or user-defined type is not a part of the public API for a Q# library or program, ensure that it is marked as internal by placing the `internal` keyword before the `function`, `operation`, or `newtype` declaration.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-271">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-271">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="13891-272">Name</span><span class="sxs-lookup"><span data-stu-id="13891-272">Name</span></span> | <span data-ttu-id="13891-273">Descrição</span><span class="sxs-lookup"><span data-stu-id="13891-273">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="13891-274">☒</span><span class="sxs-lookup"><span data-stu-id="13891-274">☒</span></span> | <s>`operation _ApplyDecomposedOperation`</s> | <span data-ttu-id="13891-275">Não use um sublinhado `_` para indicar que esta operação é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="13891-275">Do not use an underscore `_` to indicate that this operation is for internal use only.</span></span> |
| <span data-ttu-id="13891-276">☑</span><span class="sxs-lookup"><span data-stu-id="13891-276">☑</span></span> | `internal operation ApplyDecomposedOperation` | <span data-ttu-id="13891-277">A `internal` palavra-chave no início indica claramente que esta operação é apenas para uso interno.</span><span class="sxs-lookup"><span data-stu-id="13891-277">The `internal` keyword at the beginning clearly indicates that this operation is for internal use only.</span></span> |

***
### <a name="variants"></a><span data-ttu-id="13891-278">Variantes</span><span class="sxs-lookup"><span data-stu-id="13891-278">Variants</span></span> ###

<span data-ttu-id="13891-279">Embora essa limitação possa não persistir em versões futuras do Q# , ela é apresentada no momento em que, em geral, haverá grupos de operações ou funções relacionadas que são diferenciadas pelo qual transmissão functors suas entradas dão suporte ou pelos tipos concretos de seus argumentos.</span><span class="sxs-lookup"><span data-stu-id="13891-279">Though this limitation may not persist in future versions of Q#, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="13891-280">Esses grupos podem ser diferenciados usando o mesmo nome de raiz, seguidos por uma ou duas letras que indicam sua variante.</span><span class="sxs-lookup"><span data-stu-id="13891-280">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="13891-281">Sufixo</span><span class="sxs-lookup"><span data-stu-id="13891-281">Suffix</span></span> | <span data-ttu-id="13891-282">Significado</span><span class="sxs-lookup"><span data-stu-id="13891-282">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="13891-283">Entrada esperada para suporte `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="13891-283">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="13891-284">Entrada esperada para suporte `Controlled`</span><span class="sxs-lookup"><span data-stu-id="13891-284">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="13891-285">Entrada esperada para dar suporte `Controlled` e `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="13891-285">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="13891-286">Entradas ou entradas são do tipo `Int`</span><span class="sxs-lookup"><span data-stu-id="13891-286">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="13891-287">Entradas ou entradas são do tipo `Double`</span><span class="sxs-lookup"><span data-stu-id="13891-287">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="13891-288">Entradas ou entradas são do tipo `BigInt`</span><span class="sxs-lookup"><span data-stu-id="13891-288">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidance"></a>[<span data-ttu-id="13891-289">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-289">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-290">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-290">We suggest:</span></span>

- <span data-ttu-id="13891-291">Se uma função ou operação não estiver relacionada a quaisquer funções ou operações semelhantes pelos tipos e suporte functor de suas entradas, não use um sufixo.</span><span class="sxs-lookup"><span data-stu-id="13891-291">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="13891-292">Se uma função ou operação estiver relacionada a quaisquer funções ou operações semelhantes pelos tipos e suporte functor de suas entradas, use sufixos como na tabela acima para distinguir variantes.</span><span class="sxs-lookup"><span data-stu-id="13891-292">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-293">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-293">Examples</span></span>](#tab/examples)

***

### <a name="arguments-and-variables"></a><span data-ttu-id="13891-294">Argumentos e variáveis</span><span class="sxs-lookup"><span data-stu-id="13891-294">Arguments and Variables</span></span> ###

<span data-ttu-id="13891-295">Uma meta-chave do Q# código para uma função ou operação é que ela seja facilmente lida e compreendida.</span><span class="sxs-lookup"><span data-stu-id="13891-295">A key goal of the Q# code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="13891-296">Da mesma forma, os nomes de entradas e argumentos de tipo devem comunicar como uma função ou um argumento será usado uma vez fornecido.</span><span class="sxs-lookup"><span data-stu-id="13891-296">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="13891-297">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-297">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-298">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-298">We suggest:</span></span>

- <span data-ttu-id="13891-299">Para todos os nomes de variáveis e de entrada, use `pascalCase` de preferência forte para `CamelCase` , `snake_case` ou `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="13891-299">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="13891-300">Os nomes de entrada devem ser descritivos; Evite um ou dois nomes de letra sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="13891-300">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="13891-301">Operações e funções que aceitam exatamente um argumento de tipo devem indicar esse argumento de tipo por `T` quando sua função é óbvia.</span><span class="sxs-lookup"><span data-stu-id="13891-301">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="13891-302">Se uma função ou operação usar vários argumentos de tipo, ou se a função de um argumento de tipo único não for óbvia, considere usar uma palavra em maiúscula curta precedida por `T` (por exemplo: `TOutput` ) para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="13891-302">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="13891-303">Não incluir nomes de tipos em nomes de argumentos e variáveis; essas informações podem e devem ser fornecidas pelo seu ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="13891-303">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="13891-304">Denotar tipos escalares por seus nomes literais ( `flagQubit` ) e tipos de matriz por um plural ( `measResults` ).</span><span class="sxs-lookup"><span data-stu-id="13891-304">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="13891-305">Para matrizes de qubits em particular, considere a possibilidade de indicar tais tipos por `Register` onde o nome se refere a uma sequência de qubits que estão fortemente relacionadas de alguma maneira.</span><span class="sxs-lookup"><span data-stu-id="13891-305">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="13891-306">As variáveis usadas como índices em matrizes devem começar com `idx` e devem ser singulares (por exemplo: `things[idxThing]` ).</span><span class="sxs-lookup"><span data-stu-id="13891-306">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="13891-307">Particularmente, evite usar nomes de variáveis de letra única como índices; Considere o uso de `idx` no mínimo.</span><span class="sxs-lookup"><span data-stu-id="13891-307">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="13891-308">As variáveis usadas para conter comprimentos de matrizes devem começar com `n` e devem ser pluraled (por exemplo: `nThings` ).</span><span class="sxs-lookup"><span data-stu-id="13891-308">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-309">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-309">Examples</span></span>](#tab/examples)

***

### <a name="user-defined-type-named-items"></a><span data-ttu-id="13891-310">Itens nomeados do tipo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="13891-310">User-Defined Type Named Items</span></span> ###

<span data-ttu-id="13891-311">Os itens nomeados em tipos definidos pelo usuário devem ser nomeados como `CamelCase` , mesmo em entrada para construtores UDT.</span><span class="sxs-lookup"><span data-stu-id="13891-311">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="13891-312">Isso ajuda a fazer com que os itens nomeados sejam claramente separados de referências a variáveis com escopo local ao usar a notação de acessador (por exemplo: `callable::Apply` ) ou a notação de copiar e atualizar ( `set arr w/= Data <- newData` ).</span><span class="sxs-lookup"><span data-stu-id="13891-312">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidance"></a>[<span data-ttu-id="13891-313">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-313">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-314">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-314">We suggest:</span></span>

- <span data-ttu-id="13891-315">Os itens nomeados nos construtores UDT devem ser nomeados como `CamelCase` ; ou seja, eles devem começar com uma letra maiúscula inicial.</span><span class="sxs-lookup"><span data-stu-id="13891-315">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="13891-316">Os itens nomeados que são resolvidos para as operações devem ser nomeados como fases de verbo.</span><span class="sxs-lookup"><span data-stu-id="13891-316">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="13891-317">Os itens nomeados que não são resolvidos para as operações devem ser nomeados como frases de substantivo.</span><span class="sxs-lookup"><span data-stu-id="13891-317">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="13891-318">Para UDTs que encapsulam as operações, um único item nomeado chamado `Apply` deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="13891-318">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-319">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-319">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="13891-320">Snippet</span><span class="sxs-lookup"><span data-stu-id="13891-320">Snippet</span></span> | <span data-ttu-id="13891-321">Descrição</span><span class="sxs-lookup"><span data-stu-id="13891-321">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="13891-322">☑</span><span class="sxs-lookup"><span data-stu-id="13891-322">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="13891-323">O nome `Apply` é uma `CamelCase` frase verbal formatada, sugerindo que o item nomeado é uma operação.</span><span class="sxs-lookup"><span data-stu-id="13891-323">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="13891-324">☒</span><span class="sxs-lookup"><span data-stu-id="13891-324">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="13891-325">Itens nomeados devem começar com uma letra maiúscula inicial.</span><span class="sxs-lookup"><span data-stu-id="13891-325">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="13891-326">☒</span><span class="sxs-lookup"><span data-stu-id="13891-326">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="13891-327">Itens nomeados que resolvem para funções devem ser nomeados como frases de substantivo, não como frases de verbo.</span><span class="sxs-lookup"><span data-stu-id="13891-327">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

***

## <a name="input-conventions"></a><span data-ttu-id="13891-328">Convenções de entrada</span><span class="sxs-lookup"><span data-stu-id="13891-328">Input Conventions</span></span> ##

<span data-ttu-id="13891-329">Quando um desenvolvedor chama uma operação ou função, as várias entradas para essa operação ou função devem ser especificadas em uma determinada ordem, aumentando a carga cognitiva que um desenvolvedor enfrenta para fazer uso de uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="13891-329">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="13891-330">Em particular, a tarefa de memorizar as ordens de entrada é, muitas vezes, uma distração da tarefa em questão: programando uma implementação de um algoritmo Quantum.</span><span class="sxs-lookup"><span data-stu-id="13891-330">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="13891-331">Embora o suporte a IDE avançado possa reduzir isso para uma grande extensão, o bom design e a adesão a Convenções comuns também podem ajudar a minimizar a carga cognitiva imposta por uma API.</span><span class="sxs-lookup"><span data-stu-id="13891-331">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="13891-332">Sempre que possível, pode ser útil reduzir o número de entradas esperado por uma operação ou função, de modo que a função de cada entrada seja mais óbvia imediatamente para os desenvolvedores que chamam essa operação ou função e para os desenvolvedores que lêem esse código mais tarde.</span><span class="sxs-lookup"><span data-stu-id="13891-332">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="13891-333">Especialmente quando não é possível ou razoável reduzir o número de argumentos para uma operação ou função, é importante ter uma ordenação consistente que minimize a surpresa que um usuário enfrenta ao prever a ordem das entradas.</span><span class="sxs-lookup"><span data-stu-id="13891-333">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="13891-334">Recomendamos que as convenções de ordenação de entrada derivem amplamente da reflexão do aplicativo parcial como uma generalização de currying f (x, y) ≡ f (x) (y).</span><span class="sxs-lookup"><span data-stu-id="13891-334">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="13891-335">Portanto, a aplicação parcial dos primeiros argumentos deve resultar em um callable que seja útil por si só, sempre que for razoável.</span><span class="sxs-lookup"><span data-stu-id="13891-335">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="13891-336">Seguindo esse princípio, considere o uso da seguinte ordem de argumentos:</span><span class="sxs-lookup"><span data-stu-id="13891-336">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="13891-337">Argumentos clássicos não chamáveis, como ângulos, vetores de potências, etc.</span><span class="sxs-lookup"><span data-stu-id="13891-337">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="13891-338">Argumentos que podem ser chamados (funções e argumentos).</span><span class="sxs-lookup"><span data-stu-id="13891-338">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="13891-339">Se as funções e as operações forem executadas como argumentos, considere colocar operações após funções.</span><span class="sxs-lookup"><span data-stu-id="13891-339">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="13891-340">As coleções foram acionadas por argumentos que podem ser chamados de uma maneira semelhante para `Map` , `Iter` , `Enumerate` e `Fold` .</span><span class="sxs-lookup"><span data-stu-id="13891-340">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="13891-341">Argumentos qubit usados como controles.</span><span class="sxs-lookup"><span data-stu-id="13891-341">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="13891-342">Argumentos qubit usados como destinos.</span><span class="sxs-lookup"><span data-stu-id="13891-342">Qubit arguments used as targets.</span></span>

<span data-ttu-id="13891-343">Considere uma operação `ApplyPhaseEstimationIteration` para uso na estimativa de fase que usa um ângulo e um Oracle, passa o ângulo para ser `Rz` modificado por uma matriz de fatores de dimensionamento diferentes e, em seguida, controla os aplicativos da Oracle.</span><span class="sxs-lookup"><span data-stu-id="13891-343">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="13891-344">Ordenamos as entradas da `ApplyPhaseEstimationIteration` seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="13891-344">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

```qsharp
operation ApplyPhaseEstimationIteration(
    angle : Double,
    callable : (Qubit => () is Ctl),
    scaleFactors : Double[],
    controlQubit : Qubit,
    targetQubits : Qubit[]
)
: Unit
...
```
<span data-ttu-id="13891-345">Como um caso especial de minimizar a surpresa, algumas funções e operações imitam o comportamento do transmissão functors interno `Adjoint` e `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="13891-345">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="13891-346">Por exemplo, `ControlledOnInt<'T>` tem tipo `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` , que `ControlledOnInt<Qubit[]>(5, _)` funciona como o `Controlled` functor, mas na condição que o registro de controle representa o estado $ \ket {5} = \ket {101} $.</span><span class="sxs-lookup"><span data-stu-id="13891-346">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="13891-347">Portanto, um desenvolvedor espera que as entradas `ControlledOnInt` coloquem o callable que está sendo transformado por último e que a operação resultante leve como sua entrada `(Qubit[], 'T)` ---mesma ordem, conforme seguido pela saída do `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="13891-347">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="13891-348">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-348">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-349">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-349">We suggest:</span></span>

- <span data-ttu-id="13891-350">Use ordenações de entrada consistentes com o uso de aplicativo parcial.</span><span class="sxs-lookup"><span data-stu-id="13891-350">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="13891-351">Use ordenações de entrada consistentes com transmissão functors internas.</span><span class="sxs-lookup"><span data-stu-id="13891-351">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="13891-352">Coloque todas as entradas clássicas antes de qualquer entrada de Quantum.</span><span class="sxs-lookup"><span data-stu-id="13891-352">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-353">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-353">Examples</span></span>](#tab/examples)

***

## <a name="documentation-conventions"></a><span data-ttu-id="13891-354">Convenções de documentação</span><span class="sxs-lookup"><span data-stu-id="13891-354">Documentation Conventions</span></span> ##

<span data-ttu-id="13891-355">O Q# idioma permite anexar documentação a operações, funções e tipos definidos pelo usuário por meio do uso de comentários de documentação especialmente formatados.</span><span class="sxs-lookup"><span data-stu-id="13891-355">The Q# language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="13891-356">Indicado por barras triplas ( `///` ), esses comentários de documentação são documentos [de redução DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) pequeno, que podem ser usados para descrever a finalidade de cada operação, função e tipo definido pelo usuário, quais entradas cada espera e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="13891-356">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="13891-357">O compilador fornecido com o kit de desenvolvimento Quantum extrai esses comentários e os utiliza para ajudar a documentar typeset de forma semelhante a https://docs.microsoft.com/quantum .</span><span class="sxs-lookup"><span data-stu-id="13891-357">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="13891-358">Da mesma forma, o servidor de linguagem fornecido com o kit de desenvolvimento Quantum usa esses comentários para fornecer ajuda aos usuários quando eles passam o mouse sobre símbolos em seu Q# código.</span><span class="sxs-lookup"><span data-stu-id="13891-358">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their Q# code.</span></span>
<span data-ttu-id="13891-359">Fazer uso de comentários de documentação pode ajudar os usuários a fazer sentido de código fornecendo uma referência útil para os detalhes que não são facilmente expressos usando as outras convenções deste documento.</span><span class="sxs-lookup"><span data-stu-id="13891-359">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

> [!div class="nextstepaction"]
> <span data-ttu-id="13891-360">[Referência de sintaxe de comentário da documentação](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span><span class="sxs-lookup"><span data-stu-id="13891-360">[Documentation comment syntax reference](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span></span>

<span data-ttu-id="13891-361">Para usar efetivamente essa funcionalidade para ajudar os usuários, é recomendável manter algumas coisas em mente ao escrever comentários de documentação.</span><span class="sxs-lookup"><span data-stu-id="13891-361">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="13891-362">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-362">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="13891-363">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-363">We suggest:</span></span>

- <span data-ttu-id="13891-364">Cada função pública, operação e tipo definido pelo usuário deve ser imediatamente precedido por um comentário de documentação.</span><span class="sxs-lookup"><span data-stu-id="13891-364">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="13891-365">No mínimo, cada comentário da documentação deve incluir as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="13891-365">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="13891-366">Resumo</span><span class="sxs-lookup"><span data-stu-id="13891-366">Summary</span></span>
    - <span data-ttu-id="13891-367">Entrada</span><span class="sxs-lookup"><span data-stu-id="13891-367">Input</span></span>
    - <span data-ttu-id="13891-368">Saída (se aplicável)</span><span class="sxs-lookup"><span data-stu-id="13891-368">Output (if applicable)</span></span>
- <span data-ttu-id="13891-369">Verifique se todos os resumos têm duas frases ou menos.</span><span class="sxs-lookup"><span data-stu-id="13891-369">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="13891-370">Se mais espaço for necessário, forneça uma `# Description` seção imediatamente após os `# Summary` detalhes completos.</span><span class="sxs-lookup"><span data-stu-id="13891-370">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="13891-371">Quando for razoável, não inclua Math em resumos, pois nem todos os clientes dão suporte à notação TeX em resumos.</span><span class="sxs-lookup"><span data-stu-id="13891-371">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="13891-372">Observe que, ao escrever documentos da Proseware (por exemplo, TeX ou de redução), pode ser preferível usar comprimentos de linha mais longos.</span><span class="sxs-lookup"><span data-stu-id="13891-372">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="13891-373">Forneça todas as expressões matemáticas relevantes na `# Description` seção.</span><span class="sxs-lookup"><span data-stu-id="13891-373">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="13891-374">Ao descrever as entradas, não repita os tipos de cada entrada, pois elas podem ser inferidas pelo compilador e risco para introduzir inconsistência.</span><span class="sxs-lookup"><span data-stu-id="13891-374">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="13891-375">Forneça exemplos, conforme apropriado, cada um em sua própria `# Example` seção.</span><span class="sxs-lookup"><span data-stu-id="13891-375">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="13891-376">Descreva brevemente cada exemplo antes de listar o código.</span><span class="sxs-lookup"><span data-stu-id="13891-376">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="13891-377">Cite todas as publicações acadêmicas relevantes (por exemplo: papéis, procedimentos, Postagens de blog e implementações alternativas) em uma `# References` seção como uma lista com marcadores de links.</span><span class="sxs-lookup"><span data-stu-id="13891-377">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="13891-378">Verifique se, quando possível, todos os links de citação são de identificadores permanentes e imutáveis (DOIs ou números de arXiv com controle de versão).</span><span class="sxs-lookup"><span data-stu-id="13891-378">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="13891-379">Quando uma operação ou função está relacionada a outras operações ou funções por variantes functor, liste outras variantes como marcadores na `# See Also` seção.</span><span class="sxs-lookup"><span data-stu-id="13891-379">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="13891-380">Deixe uma linha de comentário em branco entre as seções de nível 1 ( `/// #` ), mas não deixe uma linha em branco entre as seções de nível 2 ( `/// ##` ).</span><span class="sxs-lookup"><span data-stu-id="13891-380">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-381">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-381">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="13891-382">☑</span><span class="sxs-lookup"><span data-stu-id="13891-382">☑</span></span> ####

```
/// # Summary
/// Applies a rotation about the X-axis by a given angle.
///
///
/// # Description
/// This operation rotates a single qubit by the unitary operation
/// \begin{align}
///     R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2}.
/// \end{align}
///
/// # Input
/// ## theta
/// Angle about which the qubit is to be rotated.
/// ## qubit
/// Qubit to which the gate should be applied.
///
/// # Remarks
/// Equivalent to:
/// ```qsharp
/// R(PauliX, theta, qubit);
/// ```
///
/// # See Also
/// - Ry
/// - Rz
operation Rx(theta : Double, qubit : Qubit) : Unit
is Adj + Ctl {
    body (...) { R(PauliX, theta, qubit); }
    adjoint (...) { R(PauliX, -theta, qubit); }
}
```

***

## <a name="formatting-conventions"></a><span data-ttu-id="13891-383">Convenções de formatação</span><span class="sxs-lookup"><span data-stu-id="13891-383">Formatting Conventions</span></span> ##

<span data-ttu-id="13891-384">Além das sugestões anteriores, é útil ajudar a tornar o código mais legível possível para usar regras de formatação consistentes.</span><span class="sxs-lookup"><span data-stu-id="13891-384">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="13891-385">Essas regras de formatação por natureza tendem a ser, de certa forma, arbitrárias e com rigidez de estética pessoais.</span><span class="sxs-lookup"><span data-stu-id="13891-385">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="13891-386">No entanto, é recomendável manter um conjunto consistente de convenções de formatação dentro de um grupo de colaboradores e, especialmente, para projetos grandes, como Q# o próprio kit de desenvolvimento do Quantum.</span><span class="sxs-lookup"><span data-stu-id="13891-386">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large Q# projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="13891-387">Essas regras podem ser aplicadas automaticamente usando a ferramenta de formatação integrada ao Q# compilador.</span><span class="sxs-lookup"><span data-stu-id="13891-387">These rules can be automatically applied by using the formatting tool integrated with the Q# compiler.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="13891-388">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="13891-388">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="13891-389">Sugerimos:</span><span class="sxs-lookup"><span data-stu-id="13891-389">We suggest:</span></span>

- <span data-ttu-id="13891-390">Use quatro espaços em vez de guias para portabilidade.</span><span class="sxs-lookup"><span data-stu-id="13891-390">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="13891-391">Por exemplo, no VS Code:</span><span class="sxs-lookup"><span data-stu-id="13891-391">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="13891-392">Quebra de linha a 79 caracteres em que é razoável.</span><span class="sxs-lookup"><span data-stu-id="13891-392">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="13891-393">Use espaços em volta de operadores binários.</span><span class="sxs-lookup"><span data-stu-id="13891-393">Use spaces around binary operators.</span></span>
- <span data-ttu-id="13891-394">Use espaços em qualquer lado dos dois-pontos usados para anotações de tipo.</span><span class="sxs-lookup"><span data-stu-id="13891-394">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="13891-395">Use um único espaço após as vírgulas usadas em literais de matriz e de tupla (por exemplo: em entradas para funções e operações).</span><span class="sxs-lookup"><span data-stu-id="13891-395">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="13891-396">Não use espaços após a função, a operação ou os nomes UDT ou depois das `@` declarações de atributo in.</span><span class="sxs-lookup"><span data-stu-id="13891-396">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="13891-397">Cada declaração de atributo deve estar em sua própria linha.</span><span class="sxs-lookup"><span data-stu-id="13891-397">Each attribute declaration should be on its own line.</span></span>

# <a name="examples"></a>[<span data-ttu-id="13891-398">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13891-398">Examples</span></span>](#tab/examples)

| &nbsp; | <span data-ttu-id="13891-399">Snippet</span><span class="sxs-lookup"><span data-stu-id="13891-399">Snippet</span></span> | <span data-ttu-id="13891-400">Descrição</span><span class="sxs-lookup"><span data-stu-id="13891-400">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="13891-401">☒</span><span class="sxs-lookup"><span data-stu-id="13891-401">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="13891-402">Use espaços em volta de operadores binários.</span><span class="sxs-lookup"><span data-stu-id="13891-402">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="13891-403">☒</span><span class="sxs-lookup"><span data-stu-id="13891-403">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="13891-404">Use espaços em volta de dois-pontos de anotação de tipo.</span><span class="sxs-lookup"><span data-stu-id="13891-404">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="13891-405">☑</span><span class="sxs-lookup"><span data-stu-id="13891-405">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="13891-406">Os itens na tupla de entrada têm o espaçamento correto para facilitar a leitura.</span><span class="sxs-lookup"><span data-stu-id="13891-406">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="13891-407">☒</span><span class="sxs-lookup"><span data-stu-id="13891-407">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="13891-408">Os espaços devem ser suprimidos após os nomes de função, operação ou UDT.</span><span class="sxs-lookup"><span data-stu-id="13891-408">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

***
