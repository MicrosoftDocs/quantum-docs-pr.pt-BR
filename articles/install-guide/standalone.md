---
title: 'Desenvolver com aplicativos de linha de comando Q #'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e829862521951c50cb42eebf261c803071a95275
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426432"
---
# <a name="develop-with-q-command-line-applications"></a>Desenvolver com aplicativos de linha de comando Q #

Os programas da Q # podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F # ou Python.

## <a name="pre-requisites"></a>Pré-requisitos

- [SDK do .NET Core 3,1 ou posterior](https://www.microsoft.com/net/download)

## <a name="installation"></a>Instalação

Embora você possa criar aplicativos de linha de comando Q # em qualquer IDE, é recomendável usar Visual Studio Code (VS Code) ou IDE do Visual Studio para seus aplicativos do Q #. O desenvolvimento nessas ferramentas fornece acesso a funcionalidades avançadas.

Para configurar VS Code:

1. Baixe e instale o [vs Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).
2. Instale o [Microsoft QDK para vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Para configurar o Visual Studio:

1. Baixe e instale o [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16,3 ou superior, com a carga de trabalho de desenvolvimento de plataforma cruzada do .NET Core habilitada.
2. Baixe e instale o [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).


## <a name="develop-with-q-using-vs-code"></a>Desenvolver com Q # usando VS Code

Instale os modelos de projeto do Q #:

1. Abra o VS Code.
2. Clique em **Exibir**  ->  **paleta de comandos**.
3. Selecione **Q #: instalar modelos de projeto**.

Quando os **modelos de projeto forem instalados com êxito** , o QDK estará pronto para uso com seus próprios aplicativos e bibliotecas.

Para criar um novo projeto:

1. Clique em **Exibir**  ->  **paleta de comandos** e selecione **Q #: criar novo projeto**.
2. Clique em **aplicativo de console autônomo**.
3. Navegue até o local para salvar o projeto e clique em **criar projeto**.
4. Quando o projeto for criado com êxito, clique em **abrir novo projeto...** no canto inferior direito.
        
Inspecione o projeto. Você deve ver um arquivo de origem chamado `Program.qs` , que é um programa Q # que define uma operação simples para imprimir uma mensagem no console.

Para executar o aplicativo:
1. Clique em **terminal**  ->  **novo terminal**.
2. No prompt do terminal, digite `dotnet run` .
3. Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`


> [!NOTE]
> Os espaços de trabalho com várias pastas raiz não têm suporte atualmente pela extensão VS Code Q #. Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.

## <a name="develop-with-q-using-visual-studio"></a>Desenvolver com Q # usando o Visual Studio

Verifique sua instalação do Visual Studio criando um aplicativo Q # `Hello World` .

Para criar um novo aplicativo Q #:
1. Abra o Visual Studio e clique em **arquivo**  ->  **novo**  ->  **projeto**.
2. Digite `Q#` na caixa de pesquisa, selecione **aplicativo Q #** e clique em **Avançar**.
3. Insira um nome e um local para seu aplicativo e clique em **criar**.


Inspecione o projeto. Você deve ver um arquivo de origem chamado `Program.qs` , que é um programa Q # que define uma operação simples para imprimir uma mensagem no console.

Para executar o aplicativo:
1. Selecione **depurar**  ->  **Iniciar sem depuração**.
2. Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.

> [!NOTE]
> Se você tiver vários projetos dentro de uma solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta que a solução, ou em uma de suas subpastas.  


## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
