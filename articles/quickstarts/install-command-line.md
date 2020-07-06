---
title: Desenvolver com aplicativos de linha de comando do Q#
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 15015d1673f47faf5a13dde516f834916b4319d6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884278"
---
# <a name="develop-with-q-command-line-applications"></a>Desenvolver com aplicativos de linha de comando do Q#

Os programas Q# podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F# ou Python.

## <a name="prerequisites"></a>Pré-requisitos

- [SDK do .NET Core 3.1 ou posterior](https://www.microsoft.com/net/download)

## <a name="installation"></a>Instalação

Embora você possa compilar aplicativos de linha de comando do Q# em qualquer IDE, recomendamos usar o VS Code (Visual Studio Code) ou o IDE do Visual Studio para seus aplicativos Q#. O desenvolvimento nesses ambientes inclui a funcionalidade sofisticada da extensão do QDK, que inclui avisos, realce de sintaxe, modelos de projeto e muito mais.

Para configurar o VS Code:

1. Baixe e instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).
2. Instale o [Microsoft QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Para configurar o Visual Studio:

1. Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 ou superior, com a carga de trabalho de desenvolvimento multiplataforma do .NET Core habilitada.
2. Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).

Para instalar o QDK para outro ambiente, digite na linha de comando:

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-q"></a>Desenvolver com Q #

Siga as instruções na guia correspondente ao seu ambiente.

### <a name="vs-code"></a>[Código do VS](#tab/tabid-vscode)

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

### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs)

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

### <a name="other-editors-with-the-command-line"></a>[Outros editores com a linha de comando](#tab/tabid-cmdline)

Verifique sua instalação criando um aplicativo Q# `Hello World`.

1. Crie um aplicativo:
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

2. Navegue até o diretório do aplicativo:
    ```dotnetcli
    cd runSayHello
    ```

    Agora, esse diretório deve conter um arquivo `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console. Você pode modificar esse modelo com um editor de texto e substituí-lo por seus aplicativos quânticos. 

3. Execute o programa:
    ```dotnetcli
    dotnet run
    ```

4. Você verá o seguinte texto impresso: `Hello quantum world!`

***

## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
