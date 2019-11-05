---
title: 'Saiba como criar um projeto do Q # com o kit de desenvolvimento Quantum (QDK)'
description: 'Inicialize um projeto para o desenvolvimento Quantum com o QDK e o Q # no ambiente de desenvolvimento de sua escolha'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: b4bec5e7a174b7e2d588331dd2093c7b23a728b0
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73444167"
---
# <a name="create-a-q-project-in-your-development-environment"></a>Criar um projeto do Q # em seu ambiente de desenvolvimento

Saiba como criar um projeto do Q # com o QDK.

Um projeto Q # contém os arquivos Q # contendo o código Quantum, bem como um programa de host para executar o programa Quantum. Você pode escrever o programa host em linguagens C#.net, como ou em Python. Você também pode executar o código Q # em um notebook Jupyter usando o kernel IQ #.

Escolha seu ambiente de desenvolvimento e idioma nas seções a seguir:

* [Python](#create-a-python-project)
* [Notebooks Jupyter](#create-a-jupyter-notebook-project)
* [C#com o Visual Studio](#create-a-c-project-on-windows-using-visual-studio)
* [C#com VS Code](#create-a-c-project-using-vs-code)
* [C#com a linha de comando](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a>Criar um projeto Python

1. Pré-requisitos

     * O [Kit de desenvolvimento Quantum para Python](xref:microsoft.quantum.install#develop-with-python)

1. Criar uma pasta para seu projeto e navegar até essa pasta

1. Crie um arquivo Q # chamado `Operation.qs`e adicione o código Q # a ele. Por exemplo:

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. Crie um arquivo de host Python chamado `host.py` para chamar a operação Q #. Por exemplo:

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. Execute o programa:

    ```bash
    python host.py
    ```

1. Verifique a saída. Seu programa deverá gerar as seguintes linhas:

    ```bash
    Hello from quantum world!
    0
    ```

Agora você pode continuar a desenvolver seu programa Quantum.

## <a name="create-a-jupyter-notebook-project"></a>Criar um projeto Jupyter Notebook

1. Pré-requisitos

    * O [Kit de desenvolvimento Quantum para notebooks Jupyter](xref:microsoft.quantum.install#develop-with-jupyter-notebooks)

1. Execute o seguinte comando para iniciar o servidor de notebook:

    ```bash
    jupyter notebook
    ```

1. Procure a URL mostrada na linha de comando. Por exemplo: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

1. Uma página Jupyter aparece no navegador. Na guia **arquivos** , selecione **novo** > **Q #** para criar um notebook Jupyter com um kernel Q #. Adicione o seguinte código à primeira célula do bloco de anotações:

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. Selecione a **célula** > **executar células** para executar o bloco de anotações. `SayHello` aparecerá em breve na saída da célula:

    ![Célula do notebook Jupyter com o código de Q #](~/media/install-guide-jupyter.png)

    Ao executar em notebooks Jupyter, o código Q # é compilado e o notebook gera o nome da (s) operação (ões) que encontrará.

1. Em uma nova célula, simule a execução em um computador Quantum da operação que você acabou de criar usando a mágica `%simulate`:

    ![Célula do notebook Jupyter com% simula mágica](~/media/install-guide-jupyter-simulate.png)

    Você deve ver a mensagem impressa na tela, juntamente com o resultado da operação que você chamou (nesse caso, vazio).

Agora você pode adicionar outras operações Q # para continuar o desenvolvimento do Quantum.

## <a name="create-a-c-project-on-windows-using-visual-studio"></a>Criar um C# projeto no Windows usando o Visual Studio

1. Pré-requisitos

    * O [Kit de desenvolvimento Quantum para Visual Studio](xref:microsoft.quantum.install#develop-with-c-on-windows-using-visual-studio)

1. Criar um aplicativo Q#

    * Acesse **Arquivo** -> **Novo** -> **Projeto**
    * Digite `Q#` na caixa de pesquisa
    * Selecione **Aplicativo Q#**
    * Selecione **Avançar**
    * Escolha um nome e uma localização para seu aplicativo
    * Escolha **Criar**

1. Inspecionar o projeto

    Você deverá ver que dois arquivos foram criados: `Driver.cs`, que é o aplicativo host C#; e `Operation.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.

1. Executar o aplicativo

    * Selecione **Depurar** -> **Iniciar Sem Depuração**
    * Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.

Agora você pode continuar o desenvolvimento do Quantum usando o Visual Studio

> [!NOTE]
> * Caso você tenha vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas.  

## <a name="create-a-c-project-using-vs-code"></a>Criar um C# projeto, usando vs Code

1. Pré-requisitos

    * O [Kit de desenvolvimento Quantum para vs Code](xref:microsoft.quantum.install#develop-with-c-using-visual-studio-code)

1. Crie um novo projeto:

    * Acesse **Exibir** -> **Paleta de Comandos**
    * Selecione **Q #: criar novo projeto**
    * Navegue até a localização no sistema de arquivos em que deseja criar o aplicativo
    * Clique no botão **Abrir novo projeto...** após a criação do projeto

1. Executar o aplicativo:

    * Acesse **Depurar** -> **Iniciar Sem Depuração**
    * Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`

Agora você pode continuar o desenvolvimento do Quantum usando Visual Studio Code.

> [!NOTE]
> * No momento, não há suporte para workspaces com várias pastas raiz na extensão do Visual Studio Code. Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a>Criar um C# projeto, usando a ferramenta de linha de comando `dotnet`

1. Pré-requisitos

    * O [Kit de desenvolvimento Quantum para a linha de comando](xref:microsoft.quantum.install#develop-with-c-using-the-dotnet-command-line-tool)

1. Crie um novo aplicativo

    ```bash
    dotnet new console -lang Q# -o <project name>
    ```

1. Navegue até o diretório do novo aplicativo

    ```bash
    cd <project name>
    ```

    Você deverá ver que dois arquivos foram criados, juntamente com os arquivos de projeto do aplicativo: um arquivo Q# (`Operation.qs`) e um arquivo de host C# (`Driver.cs`).

1. Executar o aplicativo

    ```bash
    dotnet run
    ```

    Você deverá ver a seguinte saída: `Hello quantum world!`

Agora você continua o desenvolvimento do Quantum, usando as ferramentas de linha de comando.

## <a name="whats-next"></a>O que vem a seguir?

Agora que você criou um projeto em seu ambiente preferido, você pode continuar o desenvolvimento do Quantum.
