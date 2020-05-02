---
title: 'Executar programas de Q # sem um driver e um idioma de host'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706794"
---
# <a name="q-command-line-applications"></a>Q # aplicativos de linha de comando

Os programas da Q # podem ser executados por conta própria, sem um driver em uma linguagem de host como C#, F # ou Python.

## <a name="pre-requisites"></a>Pré-requisitos

- [SDK do .NET Core 3,1 ou posterior](https://www.microsoft.com/net/download)

## <a name="installation"></a>Instalação

Embora você possa criar aplicativos de linha de comando Q # em qualquer IDE, é altamente recomendável usar Visual Studio Code (VS Code) ou IDE do Visual Studio para seus aplicativos do Q #. Usando VS Code ou o Visual Studio e a extensão de Visual Studio Code QDK, você obterá acesso à funcionalidade mais rica.

- Instalar o [vs Code](https://code.visualstudio.com/download) (Windows, Linux e Mac)
- Instalar a [extensão QDK para vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) ou
- [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, com a carga de trabalho de desenvolvimento multiplataforma com .NET Core habilitada
- Baixar e instalar a [extensão do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)


## <a name="develop-with-q-using-vs-code"></a>Desenvolver com Q # usando VS Code

Instale os modelos de projeto do Quantum:

- Ir para **Exibir** -> **paleta de comandos**
- Selecione **Q #: instalar modelos de projeto**

Agora você tem o Quantum development kit instalado e pronto para uso em seus próprios aplicativos e suas bibliotecas.
- Crie um novo projeto:
  - Ir para **Exibir** -> **paleta de comandos**
  - Selecione **Q #: criar novo projeto**
  - Selecionar **aplicativo de console autônomo**
  - Navegue até a localização no sistema de arquivos em que deseja criar o aplicativo
  - Clique no botão **Abrir novo projeto...** após a criação do projeto
        
- Inspecionar o projeto
  - Você deve ver que um arquivo chamado `Program.qs` criado, que é um programa Q # que define uma operação simples para imprimir uma mensagem no console.

- Executar o aplicativo:
  - Ir para **terminal** -> **novo terminal**
  - Inserir `dotnet run`
  - Você deverá ver o seguinte texto na Janela de Saída `Hello quantum world!`


> [!NOTE]
> * No momento, não há suporte para workspaces com várias pastas raiz na extensão do Visual Studio Code. Caso você tenha vários projetos em um workspace do VS Code, todos os projetos precisarão estar contidos na mesma pasta raiz.

## <a name="develop-with-q-using-visual-studio"></a>Desenvolver com Q # usando o Visual Studio

Verificar a instalação criando um aplicativo `Hello World`

- Criar um aplicativo Q#
  - Ir para **arquivo** -> **novo** -> **projeto**
  - Digite `Q#` na caixa de pesquisa
  - Selecione **Aplicativo Q#**
  - Selecione **Avançar**.
  - Escolha um nome e uma localização para seu aplicativo
  - Selecione **criar**

- Inspecionar o projeto
  - Você verá que um arquivo chamado `Program.qs` foi criado, que é um programa Q # que define uma operação simples para imprimir uma mensagem no console.

- Executar o aplicativo
  - Selecione **depurar** -> **Iniciar sem depuração**
  - Você deverá ver o texto `Hello quantum world!` impresso em uma janela do console.

> [!NOTE]
> * Caso você tenha vários projetos em uma só solução do Visual Studio, todos os projetos contidos na solução precisarão estar na mesma pasta da solução ou em uma das subpastas.  


## <a name="whats-next"></a>O que vem a seguir?

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.write-program).
