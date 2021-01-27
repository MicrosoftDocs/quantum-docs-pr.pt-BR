---
title: Código colaborador para o Microsoft QDK
description: Saiba como contribuir com o código de exemplo e biblioteca para o Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: contributor-guide
uid: microsoft.quantum.contributing.code
no-loc:
- Q#
- $$v
ms.openlocfilehash: 54ef15db2b850e6a3bff38945c57129361517bfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856688"
---
# <a name="contributing-code"></a><span data-ttu-id="03057-103">Código de contribuição</span><span class="sxs-lookup"><span data-stu-id="03057-103">Contributing Code</span></span>

<span data-ttu-id="03057-104">Além de relatar problemas e aprimorar a documentação, o código que contribui para o kit de desenvolvimento Quantum pode ser uma maneira muito direta de ajudar seus colegas na Comunidade de programação Quantum.</span><span class="sxs-lookup"><span data-stu-id="03057-104">In addition to reporting issues and improving documentation, contributing code to the Quantum Development Kit can be a very direct way to help your peers in the quantum programming community.</span></span>
<span data-ttu-id="03057-105">Ao contribuir com código, você pode ajudar a corrigir problemas, fornecer novos exemplos, tornar as bibliotecas existentes mais fáceis de usar ou até mesmo adicionar recursos totalmente novos.</span><span class="sxs-lookup"><span data-stu-id="03057-105">By contributing code, you can help to fix issues, provide new examples, make existing libraries easier to use, or even add entirely new features.</span></span>

<span data-ttu-id="03057-106">Neste guia, detalharemos um pouco do que procuramos quando revisarmos as solicitações de pull para ajudar sua contribuição a fazer o mais bom.</span><span class="sxs-lookup"><span data-stu-id="03057-106">In this guide, we'll detail a bit of what we look for when we review pull requests to help your contribution do the most good.</span></span>

## <a name="what-we-look-for"></a><span data-ttu-id="03057-107">O que procuramos</span><span class="sxs-lookup"><span data-stu-id="03057-107">What We Look For</span></span>

<span data-ttu-id="03057-108">Uma contribuição de código ideal se baseia no trabalho existente em um repositório de kit de desenvolvimento Quantum para corrigir problemas, expandir os recursos existentes ou adicionar novos recursos que estão dentro do escopo de um repositório.</span><span class="sxs-lookup"><span data-stu-id="03057-108">An ideal code contribution builds on the existing work in a Quantum Development Kit repository to fix issues, expand existing features, or to add new features that are within the scope of a repository.</span></span>
<span data-ttu-id="03057-109">Quando aceitamos uma contribuição de código, ele se torna parte do próprio kit de desenvolvimento Quantum, de modo que novos recursos serão lançados, mantidos e desenvolvidos da mesma maneira que o restante do kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="03057-109">When we accept a code contribution, it becomes a part of the Quantum Development Kit itself, such that new features will be released, maintained, and developed in the same way as the rest of the Quantum Development Kit.</span></span>
<span data-ttu-id="03057-110">Portanto, é útil quando a funcionalidade adicionada por uma contribuição é bem testada e documentada.</span><span class="sxs-lookup"><span data-stu-id="03057-110">Thus, it is helpful when functionality added by a contribution is well-tested and is documented.</span></span>

### <a name="unit-tests"></a><span data-ttu-id="03057-111">Testes de Unidade</span><span class="sxs-lookup"><span data-stu-id="03057-111">Unit Tests</span></span>

<span data-ttu-id="03057-112">As Q# funções, as operações e os tipos definidos pelo usuário que compõem bibliotecas como a Canon são testados automaticamente como parte do desenvolvimento no repositório [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) .</span><span class="sxs-lookup"><span data-stu-id="03057-112">The Q# functions, operations, and user-defined types that make up libraries such as the canon are automatically tested as a part of development on the [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) repository.</span></span>
<span data-ttu-id="03057-113">Quando uma nova solicitação pull é aberta, por exemplo, nossa configuração de [Azure pipelines](https://azure.microsoft.com/services/devops/pipelines/) verificará se as alterações na solicitação pull não interrompem nenhuma funcionalidade existente da qual a comunidade de programação Quantum dependa.</span><span class="sxs-lookup"><span data-stu-id="03057-113">When a new pull request is opened, for instance, our [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) configuration will check that the changes in the pull request do not break any existing functionality that the quantum programming community depends on.</span></span>

<span data-ttu-id="03057-114">Com a versão mais recente Q# , os testes de unidade são definidos usando o `@Test("QuantumSimulator")` atributo.</span><span class="sxs-lookup"><span data-stu-id="03057-114">With the latest Q# version, unit tests are defined using the `@Test("QuantumSimulator")` attribute.</span></span> <span data-ttu-id="03057-115">O argumento pode ser "QuantumSimulator", "ToffoliSimulator", "TraceSimulator" ou qualquer nome totalmente qualificado especificando o destino de execução.</span><span class="sxs-lookup"><span data-stu-id="03057-115">The argument may be either "QuantumSimulator", "ToffoliSimulator", "TraceSimulator", or any fully qualified name specifying the run target.</span></span> <span data-ttu-id="03057-116">Vários atributos que definem destinos de execução diferentes podem ser anexados ao mesmo callable.</span><span class="sxs-lookup"><span data-stu-id="03057-116">Several attributes defining different run targets may be attached to the same callable.</span></span> <span data-ttu-id="03057-117">Alguns de nossos testes ainda usam o pacote [Microsoft. Quantum. xUnit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) preterido que expõe todas as Q# funções e operações que terminam `Test` com a estrutura [xUnit](https://xunit.github.io/) .</span><span class="sxs-lookup"><span data-stu-id="03057-117">Some of our tests still use the deprecated [Microsoft.Quantum.Xunit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) package that exposes all Q# functions and operations ending in `Test` to the [xUnit](https://xunit.github.io/) framework.</span></span> <span data-ttu-id="03057-118">Este pacote não é mais necessário para definir testes de unidade.</span><span class="sxs-lookup"><span data-stu-id="03057-118">This package is no longer needed for defining unit tests.</span></span> 

<span data-ttu-id="03057-119">A função a seguir é usada para garantir que <xref:Microsoft.Quantum.Canon.Fst> as <xref:Microsoft.Quantum.Canon.Snd> funções e retornam as saídas corretas em um exemplo representativo.</span><span class="sxs-lookup"><span data-stu-id="03057-119">The following function is used to ensure that the <xref:Microsoft.Quantum.Canon.Fst> and <xref:Microsoft.Quantum.Canon.Snd> functions both return the right outputs in a representative example.</span></span>
<span data-ttu-id="03057-120">Se a saída de `Fst` ou `Snd` estiver incorreta, a `fail` instrução será usada para fazer com que o teste falhe.</span><span class="sxs-lookup"><span data-stu-id="03057-120">If the output of `Fst` or `Snd` is incorrect, the `fail` statement is used to cause the test to fail.</span></span>

```qsharp
@Test("QuantumSimulator")
function PairTest () : Unit {
    let pair = (12, PauliZ);

    if (Fst(pair) != 12) {
        let actual = Fst(pair);
        fail $"Expected 12, actual {actual}.";
    }

    if (Snd(pair) != PauliZ) {
        let actual = Snd(pair);
        fail $"Expected PauliZ, actual {actual}.";
    }
}
```

<span data-ttu-id="03057-121">Condições mais complicadas podem ser verificadas usando as técnicas na [seção de teste](xref:microsoft.quantum.libraries.diagnostics) do guia de bibliotecas padrão.</span><span class="sxs-lookup"><span data-stu-id="03057-121">More complicated conditions can be checked using the techniques in the [testing section](xref:microsoft.quantum.libraries.diagnostics) of the standard libraries guide.</span></span>
<span data-ttu-id="03057-122">Por exemplo, o teste a seguir verifica se, `H(q); X(q); H(q);` como chamado pelo, <xref:Microsoft.Quantum.Canon.ApplyWith> faz a mesma coisa que `Z(q)` .</span><span class="sxs-lookup"><span data-stu-id="03057-122">For instance, the following test checks that `H(q); X(q); H(q);` as called by <xref:Microsoft.Quantum.Canon.ApplyWith> does the same thing as `Z(q)`.</span></span>

```qsharp
@Test("QuantumSimulator")
operation TestApplyWith() : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

<span data-ttu-id="03057-123">Ao adicionar novos recursos, é uma boa ideia também adicionar novos testes para garantir que sua contribuição faça o que deveria.</span><span class="sxs-lookup"><span data-stu-id="03057-123">When adding new features, it's a good idea to also add new tests to make sure that your contribution does what it's supposed to.</span></span>
<span data-ttu-id="03057-124">Isso ajuda o restante da Comunidade a manter e desenvolver seu recurso e, em particular, ajuda outros desenvolvedores a saber que eles podem contar com seu recurso.</span><span class="sxs-lookup"><span data-stu-id="03057-124">This helps the rest of the community to maintain and develop your feature, and in particular helps other developers know that they can rely on your feature.</span></span>

> [!NOTE]
> <span data-ttu-id="03057-125">Isso também funciona da mesma forma!</span><span class="sxs-lookup"><span data-stu-id="03057-125">This works the other way around, too!</span></span>
> <span data-ttu-id="03057-126">Se houver um recurso existente que não tem alguns testes, nos ajudando a adicionar cobertura de teste, isso fará uma grande contribuição para a Comunidade.</span><span class="sxs-lookup"><span data-stu-id="03057-126">If there's an existing feature that's missing some tests, helping us add test coverage would make a great contribution to the community.</span></span>

<span data-ttu-id="03057-127">Localmente, os testes de unidade podem ser executados usando o Visual Studio Test Explorer ou o `dotnet test` comando, para que você possa verificar sua contribuição antes de abrir uma solicitação de pull.</span><span class="sxs-lookup"><span data-stu-id="03057-127">Locally, unit tests can be run using the Visual Studio Test Explorer or the `dotnet test` command, so that you can check your contribution before opening up a pull request.</span></span>

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->

## <a name="pull-requests"></a><span data-ttu-id="03057-128">Solicitações de pull</span><span class="sxs-lookup"><span data-stu-id="03057-128">Pull Requests</span></span>

<span data-ttu-id="03057-129">Quando estiver pronto para contribuir com seu trabalho, envie uma solicitação de pull por meio do GitHub para o repositório correspondente.</span><span class="sxs-lookup"><span data-stu-id="03057-129">When you are ready to contribute your work, please send a Pull Request via GitHub to the corresponding repository.</span></span>
<span data-ttu-id="03057-130">A equipe irá revisar e fornecer comentários.</span><span class="sxs-lookup"><span data-stu-id="03057-130">The team will review and provide feedback.</span></span> <span data-ttu-id="03057-131">Todos os comentários precisam ser respondidos e resolvidos e todas as verificações precisam passar antes que o código seja mesclado para a `main` ramificação.</span><span class="sxs-lookup"><span data-stu-id="03057-131">All comments need to be answered and resolved and all checks need to pass before the code is merged to the `main` branch.</span></span>

## <a name="when-well-reject-a-pull-request"></a><span data-ttu-id="03057-132">Quando rejeitarmos uma solicitação de pull</span><span class="sxs-lookup"><span data-stu-id="03057-132">When We'll Reject a Pull Request</span></span>

<span data-ttu-id="03057-133">Às vezes, rejeitaremos a solicitação de pull para uma contribuição.</span><span class="sxs-lookup"><span data-stu-id="03057-133">Sometimes, we'll reject the pull request for a contribution.</span></span>
<span data-ttu-id="03057-134">Se isso acontecer com você, não significa que ela é inadequada, pois há vários motivos para não poder aceitar uma contribuição específica.</span><span class="sxs-lookup"><span data-stu-id="03057-134">If this happens to you, it doesn't mean that it's bad, as there's a number of reasons why we might not be able to accept a particular contribution.</span></span>
<span data-ttu-id="03057-135">Talvez, mais comumente, uma contribuição para a comunidade de programação Quantum seja realmente boa, mas os repositórios do kit de desenvolvimento do Quantum não são o lugar certo para desenvolvê-lo.</span><span class="sxs-lookup"><span data-stu-id="03057-135">Perhaps most commonly, a contribution to the quantum programming community is a really good one, but the Quantum Development Kit repositories aren't the right place to develop it.</span></span>
<span data-ttu-id="03057-136">Nesses casos, é altamente recomendável que você faça seu próprio repositório---parte da força do kit de desenvolvimento Quantum é que é fácil fazer e distribuir suas próprias bibliotecas usando o GitHub e o NuGet.org, da mesma forma que distribuímos as bibliotecas Canon e química hoje em dia.</span><span class="sxs-lookup"><span data-stu-id="03057-136">In such cases, we strongly encourage you to make your own repository --- part of the strength of the Quantum Development Kit is that it's easy to make and distribute your own libraries using GitHub and NuGet.org, the same way that we distribute the canon and chemistry libraries today.</span></span>

<span data-ttu-id="03057-137">Em outras ocasiões, poderemos rejeitar uma boa contribuição simplesmente porque ainda não estamos prontos para mantê-la e desenvolvê-la.</span><span class="sxs-lookup"><span data-stu-id="03057-137">At other times, we may reject a good contribution simply because we aren't yet ready to maintain and develop it.</span></span>
<span data-ttu-id="03057-138">Pode ser difícil fazer tudo, portanto, vamos planejar quais recursos podemos trabalhar melhor como um roteiro.</span><span class="sxs-lookup"><span data-stu-id="03057-138">It can be difficult to do everything, so we plan out what features we're best able to work on as a roadmap.</span></span>
<span data-ttu-id="03057-139">Isso pode ser outro caso em que a liberação de um recurso como uma biblioteca de terceiros pode fazer muito sentido.</span><span class="sxs-lookup"><span data-stu-id="03057-139">This can be another case where releasing a feature as a third-party library can make a lot of sense.</span></span>
<span data-ttu-id="03057-140">Como alternativa, poderemos pedir ajuda para modificar um recurso para se ajustar melhor ao nosso roteiro, para que possamos fazer o melhor trabalho que possamos com ele.</span><span class="sxs-lookup"><span data-stu-id="03057-140">Alternatively, we may ask for your help in modifying a feature to better fit into our roadmap so that we can do the best work we can with it.</span></span>

<span data-ttu-id="03057-141">Também solicitaremos alterações a uma solicitação de pull se precisar de mais testes de unidade ou de documentação para nos ajudar a usá-lo, ou se ele for diferente no estilo do restante das Q# bibliotecas que tornará mais difícil para os usuários encontrarem seu recurso.</span><span class="sxs-lookup"><span data-stu-id="03057-141">We'll also ask for changes to a pull request if it requires more documentation or unit tests to help us make use of it, or if it differs enough in style from the rest of the Q# libraries that it will make it harder for users to find your feature.</span></span>
<span data-ttu-id="03057-142">Nesses casos, tentaremos oferecer conselhos sobre as revisões de código sobre o que pode ser adicionado ou alterado para facilitar a inclusão da sua contribuição.</span><span class="sxs-lookup"><span data-stu-id="03057-142">In these cases, we'll try to offer some advice in code reviews about what can be added or changed to make your contribution easier for us to include.</span></span>

<span data-ttu-id="03057-143">Por fim, não podemos aceitar contribuições que causam danos à comunidade de computação Quantum, conforme descrito no [código de conduta da Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/).</span><span class="sxs-lookup"><span data-stu-id="03057-143">Finally, we cannot accept contributions that cause harm the quantum computing community, as outlined in the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).</span></span>
<span data-ttu-id="03057-144">Queremos garantir que as contribuições atendam a toda a comunidade de computação Quantum, tanto em sua diversidade maravilhosa atual quanto no futuro, à medida que ela cresce para se tornar ainda mais inclusiva.</span><span class="sxs-lookup"><span data-stu-id="03057-144">We want to ensure that contributions serve the entire quantum computing community, both in its current wonderful diversity, and in the future as it grows to become still more inclusive.</span></span>
<span data-ttu-id="03057-145">Agradecemos sua ajuda em concretizar essa meta.</span><span class="sxs-lookup"><span data-stu-id="03057-145">We appreciate your help in realizing this goal.</span></span>

## <a name="next-steps"></a><span data-ttu-id="03057-146">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="03057-146">Next steps</span></span>

<span data-ttu-id="03057-147">Obrigado por ajudar a tornar o kit de desenvolvimento Quantum um excelente recurso para toda a comunidade de programação Quantum!</span><span class="sxs-lookup"><span data-stu-id="03057-147">Thanks for helping to make the Quantum Development Kit a great resource for the entire quantum programming community!</span></span>
<span data-ttu-id="03057-148">Para saber mais, continue com o seguinte guia sobre Q# estilo.</span><span class="sxs-lookup"><span data-stu-id="03057-148">To learn more, please continue with the following guide on Q# style.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="03057-149">Saiba mais sobre as Q# diretrizes de estilo</span><span class="sxs-lookup"><span data-stu-id="03057-149">Learn about Q# style guidelines</span></span>](xref:microsoft.quantum.contributing.style)

<span data-ttu-id="03057-150">Dependendo do tipo de código que você está contribuindo, pode haver coisas adicionais para ter em mente que podem ajudá-lo a fazer sua contribuição fazer o máximo possível para a Comunidade.</span><span class="sxs-lookup"><span data-stu-id="03057-150">Depending on what kind of code you're contributing, there may be additional things to keep in mind that can help you make your contribution do as much good for the community as possible.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="03057-151">Saiba mais sobre exemplos de colaboração</span><span class="sxs-lookup"><span data-stu-id="03057-151">Learn about contributing samples</span></span>](xref:microsoft.quantum.contributing.samples)
