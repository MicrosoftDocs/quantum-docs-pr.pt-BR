---
title: Executar o algoritmo de pesquisa de Grover em Q# – Quantum development kit
description: Crie um projeto Q# que demonstra o algoritmo de Grover, um dos algoritmos quânticos canônicos.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 9e4c53b4d5159cf07f0654603c1d477ad09eb7c6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274221"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a>Tutorial: Implementar o algoritmo de pesquisa de Grover em Q\#

Neste tutorial, saiba como criar e executar a pesquisa de Grover para acelerar a pesquisa de dados não estruturados.  A pesquisa de Grover é um dos algoritmos de computação quântica mais populares e essa implementação do Q# relativamente pequena dá uma noção das vantagens da programação de soluções quânticas com uma linguagem de programação quântica Q# de alto nível para expressar algoritmos quânticos.  No final do guia, você verá que a saída de simulação demonstra com êxito a localização de uma cadeia de caracteres específica entre uma lista de entradas não ordenadas em uma fração do tempo que levaria para pesquisar a lista inteira em um computador clássico.

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

1. Usando o Quantum development kit, [crie um projeto Q# para o aplicativo de linha de comando](xref:microsoft.quantum.install.standalone). Nomeie o projeto de `Grover`.

1. Adicione o seguinte código ao arquivo `Program.qs` no novo projeto:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. Para definir a lista que estamos pesquisando, crie um arquivo `Reflections.qs` e cole o seguinte código:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    A operação `ReflectAboutMarked` define a entrada marcada que você está pesquisando: a cadeia de caracteres que alterna zeros e uns. Essa amostra embute a entrada marcada em código e pode ser estendida para pesquisar diferentes entradas ou generalizada para qualquer entrada.

1. Em seguida, execute o novo programa Q# para encontrar o item marcado por `ReflectAboutMarked`.

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>Aplicativos de linha de comando Q# com o Visual Studio ou com o Visual Studio Code

O executável executará a operação ou a função marcada com o atributo `@EntryPoint()` em um simulador ou em um avaliador de recurso, dependendo da configuração do projeto e das opções de linha de comando.

No Visual Studio, basta pressionar Ctrl + F5 para executar o script.

No VS Code, compile o `Program.qs` pela primeira vez digitando o seguinte no terminal:

```Command line
dotnet build
```

Para as próximas execuções, não é necessário compilá-lo novamente. Para executá-lo, digite o seguinte comando e pressione Enter:

```Command line
dotnet run --no-build
```

Você deveria ver a seguinte mensagem exibida no terminal:

```
operations.qs:
This operation applies Grover's algorithm to search all possible inputs to an operation to find a particular marked state.
Usage:
operations.qs [options] [command]

--n-qubits <n-qubits> (REQUIRED)
-s, --simulator <simulator>         The name of the simulator to use.
--version                           Show version information
-?, -h, --help                      Show help and usage information
Commands:
```

Isso ocorre porque você não especificou o número de qubits que desejava usar. Portanto, o terminal informa os comandos disponíveis para o executável. Se desejamos usar cinco qubits, devemos digitar:

```Command line
dotnet run --n-qubits 5
```

Ao pressionar Enter, você deveria ver a seguinte saída:

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a>Próximas etapas

Se você gostou deste tutorial, confira alguns dos recursos abaixo para saber mais sobre como usar o Q# para escrever aplicativos quânticos próprios:

- [Volte para o guia de Introdução ao QDK](xref:microsoft.quantum.welcome)
- Experimente uma [amostra](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) mais geral do algoritmo de pesquisa de Grover
- [Saiba mais sobre a pesquisa de Grover com o Quantum Katas](xref:microsoft.quantum.overview.katas)
- Leia mais sobre a [Amplificação de amplitude][amplitude-amplification], a técnica de computação quântica por trás do algoritmo de pesquisa de Grover
- [Conceitos da computação quântica](xref:microsoft.quantum.concepts.intro)
- [Amostras do Quantum development kit](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification