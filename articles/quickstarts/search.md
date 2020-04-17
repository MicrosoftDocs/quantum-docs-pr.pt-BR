---
title: Executar o algoritmo de pesquisa de Grover em Q# – Quantum development kit
description: Crie um projeto Q# que demonstra o algoritmo de Grover, um dos algoritmos quânticos canônicos.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 0e64fcd56929fa33397c45bf1b2e99bf687eca6f
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "77906943"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a>Início Rápido: Implementar o algoritmo de pesquisa de Grover em Q#

Neste Início Rápido, você pode aprender a criar e executar a pesquisa de Grover para acelerar a pesquisa de dados não estruturados.  A pesquisa de Grover é um dos algoritmos de computação quântica mais populares e essa implementação do Q# relativamente pequena dá uma noção das vantagens da programação de soluções quânticas com uma linguagem de programação quântica Q# de alto nível para expressar algoritmos quânticos.  No fim do guia, você verá que a saída da simulação demonstra com êxito a localização de uma cadeia de caracteres específica entre uma lista de entradas não ordenadas em uma fração do tempo que levaria para pesquisar toda a lista em um computador clássico.

O algoritmo de Grover pesquisa itens específicos em uma lista de dados não estruturados. Por exemplo, ele pode responder à pergunta: Esta carta retirada de um baralho é um ás de copas? A rotulagem do item específico é chamada _entrada marcada_.

Usando o algoritmo de pesquisa de Grover, é garantido que um computador quântico execute essa pesquisa em menos etapas do que o número de itens na lista que você está pesquisando – algo que nenhum algoritmo clássico pode fazer. A maior velocidade no caso de um baralho é insignificante; no entanto, em listas que contêm milhões ou bilhões de itens, ela se torna significativa.

Você pode criar o algoritmo de pesquisa de Grover com apenas algumas linhas de código.

## <a name="prerequisites"></a>Pré-requisitos

- O Microsoft [Quantum development kit][install].

## <a name="what-does-grovers-search-algorithm-do"></a>O que o algoritmo de pesquisa de Grover faz?

O algoritmo de Grover pergunta se um item de uma lista é aquele que estamos procurando. Ele faz isso construindo uma superposição quântica dos índices da lista com cada coeficiente, ou amplitude de probabilidade, representando a probabilidade desse índice específico ser aquele que você está procurando.

No centro do algoritmo há duas etapas que aumentam de maneira incremental o coeficiente do índice que estamos procurando, até a amplitude da probabilidade desse coeficiente se aproximar de um.

O número de aumentos incrementais é menor que o número de itens na lista. É por isso que o algoritmo de pesquisa de Grover executa a pesquisa em menos etapas do que qualquer algoritmo clássico.

![Diagrama funcional do algoritmo de pesquisa de Grover](~/media/grover.png)

## <a name="write-the-code"></a>Escreva o código

1. Usando o Quantum development kit, [crie um projeto Q#](xref:microsoft.quantum.howto.createproject) chamado `Grover` no ambiente de desenvolvimento de sua escolha.

1. Adicione o seguinte código ao arquivo `Operations.qs` no novo projeto:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-40":::

1. Para definir a lista que estamos pesquisando, crie um arquivo `Reflections.qs` e cole o seguinte código:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    A operação `ReflectAboutMarked` define a entrada marcada que você está pesquisando: a cadeia de caracteres que alterna zeros e uns. Essa amostra embute a entrada marcada em código e pode ser estendida para pesquisar diferentes entradas ou generalizada para qualquer entrada.

1. Em seguida, execute o novo programa Q# para encontrar o item marcado por `ReflectAboutMarked`.

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python com Visual Studio Code ou a linha de comando](#tab/tabid-python)

    Para executar o novo programa Q# no Python, salve o seguinte código como `host.py`:

    :::code language="python" source="~/quantum/samples/algorithms/simple-grover/host.py" range="9-14":::

    Em seguida, execute o programa host do Python na linha de comando:

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# com Visual Studio Code ou a linha de comando](#tab/tabid-csharp)

    Para executar o novo programa Q# no C#, modifique `Driver.cs` para incluir o seguinte código C#:

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    Em seguida, execute o programa host do C# na linha de comando:

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019"></a>[C# com Visual Studio 2019](#tab/tabid-vs2019)

    Para executar seu novo programa em Q# no C# no Visual Studio, modifique `Driver.cs` para incluir o seguinte código C#:

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    Em seguida, pressione F5. O programa iniciará a execução e uma nova janela será exibida com os seguintes resultados: 

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```
    ***

    A operação `ReflectAboutMarked` é chamada apenas quatro vezes, mas o programa Q# conseguiu encontrar a entrada "01010" entre $2^{5} = 32$ entradas possíveis.

## <a name="next-steps"></a>Próximas etapas

Se você gostou deste início rápido, confira alguns dos recursos abaixo para saber mais sobre como usar o Q# para escrever seus próprios aplicativos quânticos:

- [Volte para o guia de Introdução ao QDK](xref:microsoft.quantum.welcome)
- Experimente uma [amostra](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) mais geral do algoritmo de pesquisa de Grover
- [Saiba mais sobre a pesquisa de Grover com o Quantum Katas](xref:microsoft.quantum.overview.katas)
- Leia mais sobre a [Amplificação de amplitude](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), a técnica de computação quântica por trás do algoritmo de pesquisa de Grover
- [Conceitos da computação quântica](xref:microsoft.quantum.concepts.intro)
- [Amostras do Quantum development kit](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
