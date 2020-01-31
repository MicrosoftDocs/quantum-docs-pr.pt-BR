---
title: 'Desenvolver com Q # +C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 1fd829c684502092bb7491b0f46b5f690320c941
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831011"
---
# <a name="develop-with-q--c"></a>Desenvolver com Q # +C#

Instale o QDK para desenvolver C# programas de host para chamar Q # operações.

O Q # foi criado para brincar bem com linguagens .NET – C#especificamente. Você pode trabalhar com esse emparelhamento dentro de diferentes ambientes de desenvolvimento:

- [Q # + C# usando o Visual Studio (Windows)](#VS)
- [Q # + C# usando Visual Studio Code (Windows, Linux e Mac)](#VSC)
- [Q # + C# usando a ferramenta de linha de comando `dotnet`](#command)

## Desenvolver com Q # + C# usando o Visual Studio<a name="VS"></a>

O Visual Studio oferece um ambiente avançado para o desenvolvimento de programas em Q #. A extensão do Visual Studio para Q # contém modelos para arquivos e projetos do Q #, bem como realce de sintaxe, conclusão de código e suporte IntelliSense.


1. Pré-requisitos

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, com a carga de trabalho de desenvolvimento multiplataforma com .NET Core habilitada

1. Instalar a extensão do Visual Studio para Q#

    - Baixar e instalar a [extensão do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)

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

## Desenvolver com Q # + C# usando Visual Studio Code<a name="VSC"></a>

O Visual Studio Code (VS Code) oferece um ambiente avançado para o desenvolvimento de programas em Q # no Windows, Linux e Mac.  A extensão Q # VS Code inclui suporte para realce de sintaxe Q #, conclusão de código e trechos de código Q #.

1. Pré-requisitos

   - [Código do VS](https://code.visualstudio.com/download)
   - [SDK do .NET Core 3,1 ou posterior](https://www.microsoft.com/net/download)

1. Instalar a extensão do VS Code para Quantum

    - Instalar a [extensão do VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)

1. Instale os modelos de projeto do Quantum:

   - Acesse **Exibir** -> **Paleta de Comandos**
   - Selecione **Q #: instalar modelos de projeto**

    Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.

1. Verificar a instalação criando um aplicativo `Hello World`

    - Crie um novo projeto:

        - Acesse **Exibir** -> **Paleta de Comandos**
        - Selecione **Q #: criar novo projeto**
        - Selecionar **aplicativo de console autônomo**
        - Navegue até a localização no sistema de arquivos em que deseja criar o aplicativo
        - Clique no botão **Abrir novo projeto...** após a criação do projeto

    - Se você ainda não tiver a C# extensão para vs Code instalada, um pop-up será exibido. Instale a extensão. 

    - Executar o aplicativo:

        - Ir para **terminal** -> **novo terminal**
        - Inserir `dotnet run`
        - Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`


> [!NOTE]
> * No momento, não há suporte para workspaces com várias pastas raiz na extensão do Visual Studio Code. Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.

## Desenvolver com Q # + C# usando a ferramenta de linha de comando `dotnet`<a name="command"></a>

É claro que você também pode criar e executar os programas de Q# na linha de comando, simplesmente instalando o SDK do .NET Core e os modelos de projeto do QDK. 

1. Pré-requisitos

    - [SDK do .NET Core 3,1 ou posterior](https://www.microsoft.com/net/download)

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
