---
title: Desenvolver com Jupyter Notebooks do Q#
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274017"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Desenvolver com Jupyter Notebooks do Q#

Instale o QDK para desenvolver operações Q# em Jupyter Notebooks do Q#.

Os Jupyter Notebooks permitem a execução de código in-loco juntamente com instruções, observações e outros tipos de conteúdo. Esse ambiente é ideal para a escrita de código Q# com explicações inseridas ou tutoriais interativos de computação quântica. Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.

IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.

> [!NOTE]
> * Em Jupyter Notebooks do Q#, você só pode executar o código Q#, e as operações não podem ser chamadas em programas de host externos (por exemplo, arquivos do Python ou C#). Esse ambiente não será apropriado se sua meta for combinar um programa de host clássico externo com o programa quântico.

1. Pré-requisitos

    - [Python](https://www.python.org/downloads/) 3.6 ou posterior
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [SDK do .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Instalar o pacote `iqsharp`

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Se você receber um erro durante a etapa `dotnet iqsharp install`, abra uma nova janela de terminal e tente novamente.
    > Se isso ainda não funcionar, tente localizar a ferramenta `dotnet-iqsharp` instalada (no Windows, `dotnet-iqsharp.exe`) e executar:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > em que `/path/to/dotnet-iqsharp` deverá ser substituída pelo caminho absoluto para a ferramenta `dotnet-iqsharp` no sistema de arquivos.
    > Normalmente, isso estará em `.dotnet/tools` na pasta de perfil do usuário.

1. Verificar a instalação criando um aplicativo `Hello World`

    - Execute o seguinte comando para iniciar o servidor de notebook:

        ```
        jupyter notebook
        ```

    - Para abrir o Jupyter Notebook, copie e cole a URL fornecida pela linha de comando no navegador.

    - Crie um Jupyter Notebook com um kernel do Q# e adicione o seguinte código à primeira célula do notebook:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Execute esta célula do notebook:

        ![Célula do Jupyter Notebook com o código Q#](~/media/install-guide-jupyter.png)

        Você deverá ver `SayHello` na saída da célula. Durante a execução no Jupyter Notebook, o código Q# é compilado e o notebook gera o nome das operações encontradas.


    - Em uma nova célula, execute a operação recém-criada (em um simulador) usando o comando `%simulate`:

        ![Célula do Jupyter Notebook com o magic %simulate](~/media/install-guide-jupyter-simulate.png)

        Você verá a mensagem impressa na tela junto com o resultado da operação invocada (aqui, vemos a tupla vazia `()` porque nossa operação apenas retorna um tipo `Unit`).

## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o QDK para Jupyter Notebooks do Q#, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng) escrevendo o código Q# diretamente no ambiente do Jupyter Notebook.

Para obter mais exemplos do que você pode fazer com Jupyter Notebooks do Q#, confira:
- [Introdução ao Q# e ao Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Nesse artigo, você encontrará um Jupyter Notebook do Q# que mostra como usar o Q# nesse ambiente.
- [Quantum Katas](xref:microsoft.quantum.overview.katas), uma coleção de software livre de tutoriais individuais e conjuntos de exercícios de programação na forma de Jupyter Notebooks do Q#. Os [notebooks do tutorial do Quantum Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) são um bom ponto de partida. O Quantum Katas tem como objetivo ensinar elementos da computação quântica e programação com o Q# simultaneamente. Eles são um excelente exemplo do tipo de conteúdo que você pode criar com Jupyter Notebooks do Q#.
