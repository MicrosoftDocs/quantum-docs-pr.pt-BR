---
title: Saiba como instalar o QDK (Microsoft Quantum development kit)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2a098d89f13278d7137bf182a184a74afb9393be
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462876"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Instalar o QDK (Microsoft Quantum development kit)

Saiba como instalar o QDK (Microsoft Quantum development kit) para começar a usar a programação quântica. O QDK consiste no seguinte:

- a linguagem de programação Q#
- um conjunto de bibliotecas que abstrai a funcionalidade complexa no Q#
- um aplicativo host (escrito em Python ou uma linguagem .NET) que executa operações quânticas escritas em Q#
- ferramentas para facilitar seu desenvolvimento

Dependendo do ambiente de desenvolvimento escolhido, há diferentes etapas de instalação. Escolha seu ambiente nas seções abaixo.

## <a name="develop-with-python"></a>Desenvolvimento com o Python

O pacote qsharp para Python facilita a simulação de operações e funções de Q# no Python. IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python que fornece a funcionalidade principal para compilar e simular operações Q#.

1. Pré-requisitos

    - [Python](https://www.python.org/downloads/) 3.6 ou posterior
    - O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [SDK do .NET Core 3.0 ou posterior](https://www.microsoft.com/net/download)

1. Instalar o pacote `iqsharp`

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Instalar o pacote `qsharp`

    ```bash
    pip install qsharp
    ```

1. Verificar a instalação criando um aplicativo `Hello World`

    - Crie uma operação Q# mínima criando um arquivo chamado `Operation.qs` e adicionando o seguinte código a ele:

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - Crie um programa Python chamado `hello_world.py` para chamar a operação Q# `SayHello()`:

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - Execute o programa:

        ```bash
        python hello_world.py
        ```

    - Verifique a saída. Seu programa deverá gerar as seguintes linhas:

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a>Desenvolvimento com Jupyter notebooks

Favoritos de configurações acadêmicas, laboratórios científicos e programação colaborativa baseada em uso online, os Jupyter Notebooks oferecem execução de código in-loco — agora incluindo código Q# — juntamente com instruções, anotações e outros conteúdos.  Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.

IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.


1. Pré-requisitos

    - [Python](https://www.python.org/downloads/) 3.6 ou posterior
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [SDK do .NET Core 3.0 ou posterior](https://www.microsoft.com/net/download)

1. Instalar o pacote `iqsharp`

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Verificar a instalação criando um aplicativo `Hello World`

    - Execute o seguinte comando para iniciar o servidor de notebook:

        ```bash
        jupyter notebook
        ```

    - Procure a URL mostrada na linha de comando. Por exemplo: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

    - Crie um Jupyter Notebook com um kernel do Q# e adicione o seguinte código à primeira célula do notebook:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Execute esta célula do notebook:

        ![Célula do Jupyter Notebook com código Q#](~/media/install-guide-jupyter.png)

        Você deverá ver `SayHello` na saída da célula. Durante a execução em Jupyter notebooks, o código Q# é compilado e o notebook gera o nome das operações encontradas.


    - Em uma nova célula, usando um computador quântico, simule a execução da operação que você acabou de criar usando a mágica `%simulate`:

        ![Célula do Jupyter Notebook com a mágica %simulate](~/media/install-guide-jupyter-simulate.png)

        Você deverá ver a mensagem impressa na tela, juntamente com o resultado da operação que você invocou (nesse caso, vazio).


## <a name="develop-with-c-on-windows-using-visual-studio"></a>Desenvolvimento com o C# no Windows usando o Visual Studio

O Visual Studio oferece um ambiente avançado para o desenvolvimento de programas de Q#, oferecendo ótimos recursos como conclusão de código e realce de sintaxe que orienta o desenvolvedor na criação de seus aplicativos.  A extensão do Visual Studio para Q# contém modelos para arquivos e projetos do Q#, bem como realce de sintaxe e suporte para IntelliSense.


1. Pré-requisitos

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, com a carga de trabalho de desenvolvimento multiplataforma com .NET Core habilitada

1. Instalar a extensão do Visual Studio para Q#

    - Baixar a [extensão do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Adicionar a extensão ao Visual Studio

1. Verificar a instalação criando um aplicativo `Hello World`

    - Criar um aplicativo Q#

        - Acesse **Arquivo** -> **Novo** -> **Projeto**
        - Digite `Q#` na caixa de pesquisa
        - Selecione **Aplicativo Q#**
        - Selecione **Avançar**
        - Escolha um nome e uma localização para seu aplicativo
        - Escolha **Criar**

    - Inspecionar o projeto

        Você deverá ver que dois arquivos foram criados: `Driver.cs`, que é o aplicativo host C#; e `Operation.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.

    - Executar o aplicativo

        - Selecione **Depurar** -> **Iniciar Sem Depuração**
        - Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.

> [!NOTE]
> * Caso você tenha vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas.  

## <a name="develop-with-c-using-visual-studio-code"></a>Desenvolver com C# usando o Visual Studio Code

O VS Code (Visual Studio Code) oferece um ambiente avançado para o desenvolvimento de programas de Q# entre vários ambientes de computadores, incluindo Windows, Linux e Mac e oferecendo ótimos recursos, tais como conclusão de código e realce de sintaxe, que orientam os desenvolvedores na criação dos respectivos aplicativos.  A extensão VS Code do Q# contém realce de sintaxe e trechos de código do Q#.

1. Pré-requisitos

   - [Código do VS](https://code.visualstudio.com/download)
   - [SDK do .NET Core 3.0 ou posterior](https://www.microsoft.com/net/download)

1. Instalar a extensão do VS Code para Quantum

    - Instalar a [extensão do VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)

1. Instale os modelos de projeto do Quantum:

   - Acesse **Exibir** -> **Paleta de Comandos**
   - Selecione **Q#: Instalar modelos de projeto**

    Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.

1. Verificar a instalação criando um aplicativo `Hello World`

    - Crie um novo projeto:

        - Acesse **Exibir** -> **Paleta de Comandos**
        - Selecione **Q#: Criar Projeto**
        - Navegue até a localização no sistema de arquivos em que deseja criar o aplicativo
        - Clique no botão **Abrir novo projeto...** após a criação do projeto

    - Executar o aplicativo:

        - Acesse **Depurar** -> **Iniciar Sem Depuração**
        - Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`

> [!NOTE]
> * > * No momento, não há suporte para workspaces com várias pastas raiz na extensão do Visual Studio Code. Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a>Desenvolvimento com o C# usando a ferramenta de linha de comando `dotnet`

É claro que você também pode criar e executar os programas de Q# na linha de comando, simplesmente instalando o SDK do .NET Core e os modelos de projeto do QDK. 

1. Pré-requisitos

    - [SDK do .NET Core 3.0 ou posterior](https://www.microsoft.com/net/download)

1. Instalar os modelos de projeto do Quantum para .NET

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.

1. Verificar a instalação criando um aplicativo `Hello World`

    - Crie um novo aplicativo

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - Navegue até o diretório do novo aplicativo

       ```bash
       cd runSayHello
       ```

    Você deverá ver que dois arquivos foram criados, juntamente com os arquivos de projeto do aplicativo: um arquivo Q# (`Operation.qs`) e um arquivo de host C# (`Driver.cs`).

    - Executar o aplicativo

        ```bash
        dotnet run
        ```

        Você deverá ver a seguinte saída: `Hello quantum world!`

## <a name="whats-next"></a>O que vem a seguir?

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.write-program).
