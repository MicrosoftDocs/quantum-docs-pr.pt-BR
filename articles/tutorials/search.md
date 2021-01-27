---
title: Executar o algoritmo de pesquisa do Grover no Q# Kit de desenvolvimento do Quantum
description: Crie um Q# projeto que demonstre o algoritmo de Grover, um dos algoritmos de Quantum canônicos.
author: cgranade
ms.author: chgranad
ms.date: 10/19/2019
ms.topic: tutorial
uid: microsoft.quantum.quickstarts.search
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5e0398338ff710decc0f3038c07c9b7d39514195
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856627"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a>Tutorial: Implementar o algoritmo de pesquisa de Grover em Q\#

Neste tutorial, saiba como criar e executar a pesquisa de Grover para acelerar a pesquisa de dados não estruturados.  A pesquisa do Grover é um dos mais populares algoritmos de computação Quantum, e essa Q# implementação relativamente pequena dá a você uma noção de algumas das vantagens da programação de soluções Quantum com uma Q# linguagem de programação Quantum de alto nível para expressar os algoritmos Quantum.  No final do guia, você verá que a saída de simulação demonstra com êxito a localização de uma cadeia de caracteres específica entre uma lista de entradas não ordenadas em uma fração do tempo que levaria para pesquisar a lista inteira em um computador clássico.

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

1. Usando o kit de desenvolvimento Quantum, [crie um novo Q# projeto para o aplicativo](xref:microsoft.quantum.install.standalone). Nomeie o projeto de `Grover`.

1. Adicione o seguinte código ao arquivo `Program.qs` no novo projeto:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. Para definir a lista que estamos pesquisando, crie um arquivo `Reflections.qs` e cole o seguinte código:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    A operação `ReflectAboutMarked` define a entrada marcada que você está pesquisando: a cadeia de caracteres que alterna zeros e uns. Essa amostra embute a entrada marcada em código e pode ser estendida para pesquisar diferentes entradas ou generalizada para qualquer entrada.

1. Em seguida, execute o novo Q# programa para localizar o item marcado por `ReflectAboutMarked` .

### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a>Q# aplicativos com Visual Studio ou Visual Studio Code

O programa executará a operação ou função marcada com o `@EntryPoint()` atributo em um simulador ou avaliador de recurso, dependendo da configuração do projeto e das opções de linha de comando.

No Visual Studio, basta pressionar CTRL + F5 para executar o script.

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

Isso ocorre porque você não especificou o número de qubits que desejava usar, de modo que o terminal mostra os comandos disponíveis para o programa executável. Se quisermos usar 5 qubits, devemos digitar:

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

Se você gostou deste tutorial, confira alguns dos recursos abaixo para saber mais sobre como você pode usar Q# o para escrever seus próprios aplicativos Quantum:

- [Volte para o guia de Introdução ao QDK](xref:microsoft.quantum.welcome)
- Experimente uma [amostra](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/database-search) mais geral do algoritmo de pesquisa de Grover
- [Saiba mais sobre a pesquisa de Grover com o Quantum Katas](xref:microsoft.quantum.overview.katas)
- Leia mais sobre a [Amplificação de amplitude][amplitude-amplification], a técnica de computação quântica por trás do algoritmo de pesquisa de Grover
- [Conceitos da computação quântica](xref:microsoft.quantum.concepts.intro)
- [Amostras do Quantum development kit](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
