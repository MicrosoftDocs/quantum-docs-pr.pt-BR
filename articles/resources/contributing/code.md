---
title: Código colaborador para o Microsoft QDK
description: Saiba como contribuir com o código de exemplo e biblioteca para o Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.code
no-loc:
- Q#
- $$v
ms.openlocfilehash: 956b0957a5261b8a77bf18d776fbcc2853bfbfe7
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866901"
---
# <a name="contributing-code"></a>Código de contribuição

Além de relatar problemas e aprimorar a documentação, o código que contribui para o kit de desenvolvimento Quantum pode ser uma maneira muito direta de ajudar seus colegas na Comunidade de programação Quantum.
Ao contribuir com código, você pode ajudar a corrigir problemas, fornecer novos exemplos, tornar as bibliotecas existentes mais fáceis de usar ou até mesmo adicionar recursos totalmente novos.

Neste guia, detalharemos um pouco do que procuramos quando revisarmos as solicitações de pull para ajudar sua contribuição a fazer o mais bom.

## <a name="what-we-look-for"></a>O que procuramos

Uma contribuição de código ideal se baseia no trabalho existente em um repositório de kit de desenvolvimento Quantum para corrigir problemas, expandir os recursos existentes ou adicionar novos recursos que estão dentro do escopo de um repositório.
Quando aceitamos uma contribuição de código, ele se torna parte do próprio kit de desenvolvimento Quantum, de modo que novos recursos serão lançados, mantidos e desenvolvidos da mesma maneira que o restante do kit de desenvolvimento Quantum.
Portanto, é útil quando a funcionalidade adicionada por uma contribuição é bem testada e documentada.

### <a name="unit-tests"></a>Testes de Unidade

As Q# funções, as operações e os tipos definidos pelo usuário que compõem bibliotecas como a Canon são testados automaticamente como parte do desenvolvimento no repositório [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) .
Quando uma nova solicitação pull é aberta, por exemplo, nossa configuração de [Azure pipelines](https://azure.microsoft.com/services/devops/pipelines/) verificará se as alterações na solicitação pull não interrompem nenhuma funcionalidade existente da qual a comunidade de programação Quantum dependa.

Com a versão mais recente Q# , o teste de unidade é definido usando o `@Test("QuantumSimulator")` atributo. O argumento pode ser "QuantumSimulator", "ToffoliSimulator", "TraceSimulator" ou qualquer nome totalmente qualificado especificando o destino de execução. Vários atributos que definem destinos de execução diferentes podem ser anexados ao mesmo callable. Alguns de nossos testes ainda usam o pacote [Microsoft. Quantum. xUnit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) preterido que expõe todas as Q# funções e operações que terminam `Test` com a estrutura [xUnit](https://xunit.github.io/) . Este pacote não é mais necessário para definir testes de unidade. 

A função a seguir é usada para garantir que <xref:microsoft.quantum.canon.fst> as <xref:microsoft.quantum.canon.snd> funções e retornam as saídas corretas em um exemplo representativo.
Se a saída de `Fst` ou `Snd` estiver incorreta, a `fail` instrução será usada para fazer com que o teste falhe.

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

Condições mais complicadas podem ser verificadas usando as técnicas na [seção de teste](xref:microsoft.quantum.libraries.diagnostics) do guia de bibliotecas padrão.
Por exemplo, o teste a seguir verifica se, `H(q); X(q); H(q);` como chamado pelo, <xref:microsoft.quantum.canon.applywith> faz a mesma coisa que `Z(q)` .

```Q#
@Test("QuantumSimulator")
operation TestApplyWith() : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

Ao adicionar novos recursos, é uma boa ideia também adicionar novos testes para garantir que sua contribuição faça o que deveria.
Isso ajuda o restante da Comunidade a manter e desenvolver seu recurso e, em particular, ajuda outros desenvolvedores a saber que eles podem contar com seu recurso.

> [!NOTE]
> Isso também funciona da mesma forma!
> Se houver um recurso existente que não tem alguns testes, nos ajudando a adicionar cobertura de teste, isso fará uma grande contribuição para a Comunidade.

Localmente, os testes de unidade podem ser executados usando o Visual Studio Test Explorer ou o `dotnet test` comando, para que você possa verificar sua contribuição antes de abrir uma solicitação de pull.

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->


## <a name="when-well-reject-a-pull-request"></a>Quando rejeitarmos uma solicitação de pull

Às vezes, rejeitaremos a solicitação de pull para uma contribuição.
Se isso acontecer com você, não significa que ela é inadequada, pois há vários motivos para não poder aceitar uma contribuição específica.
Talvez, mais comumente, uma contribuição para a comunidade de programação Quantum seja realmente boa, mas os repositórios do kit de desenvolvimento do Quantum não são o lugar certo para desenvolvê-lo.
Nesses casos, é altamente recomendável que você faça seu próprio repositório---parte da força do kit de desenvolvimento Quantum é que é fácil fazer e distribuir suas próprias bibliotecas usando o GitHub e o NuGet.org, da mesma forma que distribuímos as bibliotecas Canon e química hoje em dia.

Em outras ocasiões, poderemos rejeitar uma boa contribuição simplesmente porque ainda não estamos prontos para mantê-la e desenvolvê-la.
Pode ser difícil fazer tudo, portanto, vamos planejar quais recursos podemos trabalhar melhor como um roteiro.
Isso pode ser outro caso em que a liberação de um recurso como uma biblioteca de terceiros pode fazer muito sentido.
Como alternativa, poderemos pedir ajuda para modificar um recurso para se ajustar melhor ao nosso roteiro, para que possamos fazer o melhor trabalho que possamos com ele.

Também solicitaremos alterações a uma solicitação de pull se precisar de mais testes de unidade ou de documentação para nos ajudar a usá-lo, ou se ele for diferente no estilo do restante das Q# bibliotecas que tornará mais difícil para os usuários encontrarem seu recurso.
Nesses casos, tentaremos oferecer conselhos sobre as revisões de código sobre o que pode ser adicionado ou alterado para facilitar a inclusão da sua contribuição.

Por fim, não podemos aceitar contribuições que causam danos à comunidade de computação Quantum, conforme descrito no [código de conduta da Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/).
Queremos garantir que as contribuições atendam a toda a comunidade de computação Quantum, tanto em sua diversidade maravilhosa atual quanto no futuro, à medida que ela cresce para se tornar ainda mais inclusiva.
Agradecemos sua ajuda em concretizar essa meta.

## <a name="next-steps"></a>Próximas etapas

Obrigado por ajudar a tornar o kit de desenvolvimento Quantum um excelente recurso para toda a comunidade de programação Quantum!
Para saber mais, continue com o seguinte guia sobre Q# estilo.

> [!div class="nextstepaction"]
> [Saiba mais sobre as Q# diretrizes de estilo](xref:microsoft.quantum.contributing.style)

Dependendo do tipo de código que você está contribuindo, pode haver coisas adicionais para ter em mente que podem ajudá-lo a fazer sua contribuição fazer o máximo possível para a Comunidade.

> [!div class="nextstepaction"]
> [Saiba mais sobre exemplos de colaboração](xref:microsoft.quantum.contributing.samples)
