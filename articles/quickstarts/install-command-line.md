---
title: Desenvolver com aplicativos de linha de comando do Q#
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274024"
---
# <a name="develop-with-q-command-line-applications"></a>Desenvolver com aplicativos de linha de comando do Q#

Os programas Q# podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F# ou Python.

## <a name="prerequisites"></a>Pré-requisitos

- [SDK do .NET Core 3.1 ou posterior](https://www.microsoft.com/net/download)

## <a name="installation"></a>Instalação

Embora você possa compilar aplicativos de linha de comando do Q# em qualquer IDE, recomendamos usar o VS Code (Visual Studio Code) ou o IDE do Visual Studio para seus aplicativos Q#. O desenvolvimento nessas ferramentas fornece acesso a funcionalidades avançadas.

Para configurar o VS Code:

1. Baixe e instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).
2. Instale o [Microsoft QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Para configurar o Visual Studio:

1. Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 ou superior, com a carga de trabalho de desenvolvimento multiplataforma do .NET Core habilitada.
2. Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).


## <a name="develop-with-q-using-vs-code"></a>Desenvolver com o C# por meio do VS Code

Instale os modelos de projeto Q#:

1. Abra o VS Code.
2. Clique em **Exibir** -> **Paleta de Comandos**.
3. Selecione **Q#: Instalar modelos de projeto**.

Quando a mensagem **Modelos de projeto instalados com êxito** for exibida, o QDK estará pronto para uso com bibliotecas e aplicativos próprios.

Para criar um projeto:

1. Clique em **Exibir** -> **Paleta de Comandos** e selecione **Q#: Criar Novo Projeto**.
2. Clique em **Aplicativo de console autônomo**.
3. Navegue até o local para salvar o projeto e clique em **Criar Projeto**.
4. Quando o projeto for criado com êxito, clique em **Abrir novo projeto...** no canto inferior direito.
        
Inspecione o projeto. Você verá um arquivo de origem chamado `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.

Para executar o aplicativo:
1. Clique em **Terminal** -> **Novo Terminal**.
2. No prompt do terminal, insira `dotnet run`.
3. Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`


> [!NOTE]
> No momento, não há suporte para workspaces com várias pastas raiz na extensão do Q# para VS Code. Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.

## <a name="develop-with-q-using-visual-studio"></a>Desenvolver com o Q# por meio do Visual Studio

Verifique sua instalação do Visual Studio criando um aplicativo Q# `Hello World`.

Para criar um aplicativo Q#:
1. Abra o Visual Studio e clique em **Arquivo** -> **Novo** -> **Projeto**.
2. Digite `Q#` na caixa de pesquisa, selecione **Aplicativo Q#** e clique em **Avançar**.
3. Insira um nome e um local para o aplicativo e clique em **Criar**.


Inspecione o projeto. Você verá um arquivo de origem chamado `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console.

Para executar o aplicativo:
1. Selecione **Depurar** -> **Iniciar Sem Depuração**.
2. Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.

> [!NOTE]
> Se você tiver vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas dela.  


## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
