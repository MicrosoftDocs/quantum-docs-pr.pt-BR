---
title: Desenvolver com aplicativos de linha de comando do Q#
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 630dc7b8acf2dd8f258eb27dfbc367b812cd1c19
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867600"
---
# <a name="develop-with-no-locq-command-line-applications"></a>Desenvolver com aplicativos de linha de comando do Q#

Os programas Q# podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F# ou Python.

## <a name="prerequisites"></a>Pré-requisitos

- [SDK do .NET Core 3.1 ou posterior](https://www.microsoft.com/net/download)

## <a name="installation"></a>Instalação

Embora seja possível compilar aplicativos de linha de comando do Q# em qualquer IDE, é recomendável usar o VS Code (Visual Studio Code) ou o IDE do Visual Studio para desenvolver aplicativos Q# localmente. Para desenvolvimento na nuvem por meio do navegador da Web, recomendamos o Codespaces do Visual Studio. O desenvolvimento nesses ambientes inclui a funcionalidade sofisticada da extensão do QDK, que inclui avisos, realce de sintaxe, modelos de projeto e muito mais. 

Para configurar o VS Code:

1. Baixe e instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).
2. Instale o [Microsoft QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Para configurar o Visual Studio:

1. Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 ou superior, com a carga de trabalho de desenvolvimento multiplataforma do .NET Core habilitada.
2. Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).

Para configurar o Codespaces do Visual Studio:

1. Criar uma [conta do Azure](https://azure.microsoft.com/free/).
2. Crie um ambiente de Codespaces. Siga o [guia de início rápido](https://docs.microsoft.com/visualstudio/online/quickstarts/browser). Ao criar o espaço de código, é recomendável inserir `microsoft/Quantum` no campo "Repositório Git" para carregar configurações específicas do QDK.
3. Agora você pode iniciar o novo ambiente e começar a desenvolver no navegador por meio do [IDE de nuvem do Codespaces do VS](https://online.visualstudio.com/environments). Como alternativa, é possível usar a instalação local do VS Code e usar o Codespaces como um [ambiente remoto](https://docs.microsoft.com/visualstudio/online/how-to/vscode).


Para instalar o QDK para outro ambiente, digite na linha de comando:

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a>Desenvolver com Q#

Siga as instruções na guia correspondente ao seu ambiente.

### <a name="vs-code"></a>[Código do VS](#tab/tabid-vscode)

Para criar um projeto:

1. Clique em **Exibir** -> **Paleta de Comandos** e selecione **Q#: Criar Novo Projeto**.
2. Clique em **Aplicativo de console autônomo**.
3. Navegue até o local para salvar o projeto e clique em **Criar Projeto**.
4. Quando o projeto for criado com êxito, clique em **Abrir novo projeto...** no canto inferior direito.
        
Inspecione o projeto. Você verá um arquivo de origem chamado `Program.qs`, um programa Q# que define uma operação simples para imprimir uma mensagem no console.

Para executar o aplicativo:
1. Clique em **Terminal** -> **Novo Terminal**.
2. No prompt do terminal, insira `dotnet run`.
3. Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`


> [!NOTE]
> No momento, não há compatibilidade com workspaces com várias pastas raiz na extensão do Q# para VS Code. Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.

### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs)

Verifique sua instalação do Visual Studio criando um aplicativo Q# `Hello World`.

Para criar um novo aplicativo Q#:
1. Abra o Visual Studio e clique em **Arquivo** -> **Novo** -> **Projeto**.
2. Digite `Q#` na caixa de pesquisa, selecione **Aplicativo Q#** e clique em **Avançar**.
3. Insira um nome e um local para o aplicativo e clique em **Criar**.


Inspecione o projeto. Você verá um arquivo de origem chamado `Program.qs`, um programa Q# que define uma operação simples para imprimir uma mensagem no console.

Para executar o aplicativo:
1. Selecione **Depurar** -> **Iniciar Sem Depuração**.
2. Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.

> [!NOTE]
> Se você tiver vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas dela.  

### <a name="other-editors-with-the-command-line"></a>[Outros editores com a linha de comando](#tab/tabid-cmdline)

Verifique sua instalação criando um aplicativo Q# `Hello World`.

1. Instale os modelos de projeto.

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. Crie um aplicativo:
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. Navegue até o diretório do aplicativo:
    ```dotnetcli
    cd runSayHello
    ```

    Agora, esse diretório deve conter um arquivo `Program.qs`, que é um programa Q# que define uma operação simples para imprimir uma mensagem no console. Você pode modificar esse modelo com um editor de texto e substituí-lo por seus aplicativos quânticos. 

1. Execute o programa:
    ```dotnetcli
    dotnet run
    ```

1. Você verá o seguinte texto impresso: `Hello quantum world!`

***

## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
