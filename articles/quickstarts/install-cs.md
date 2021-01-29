---
title: Desenvolver com o Q# e o .NET
description: Saiba como criar um aplicativo Q# usando linguagens .NET.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: de79c361331766572f5608c341be766e071e01b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844300"
---
# <a name="develop-with-no-locq-and-net"></a>Desenvolver com o Q# e o .NET

O Q# foi criado visando a uma boa compatibilidade com as linguagens .NET, como C# e F#.
Neste guia, demonstramos como usar o Q# com um programa de host escrito em uma linguagem .NET.

Primeiro, criamos o aplicativo Q# e o host .NET, depois demonstramos como chamar Q# do host.

## <a name="prerequisites"></a>Pré-requisitos

- Instalar o Quantum Development Kit [para uso com projetos do Q#](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-no-locq-library-and-a-net-host"></a>Criar uma biblioteca do Q# e um host do .NET

A primeira etapa é criar projetos para a biblioteca do Q# e para o host do .NET que chamará as operações e as funções definidas na biblioteca do Q#.

Siga as instruções na guia correspondente ao seu ambiente de desenvolvimento.
Se estiver usando um editor diferente do Visual Studio ou do VS Code, basta seguir as etapas do prompt de comando.

### <a name="visual-studio-code-or-command-prompt"></a>[Visual Studio Code ou prompt de comando](#tab/tabid-cmdline)

- Criar uma nova biblioteca do Q#

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Criar um projeto de console C# ou F#

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Adicione a biblioteca do Q# como uma referência do programa de host

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- [Opcional] Crie uma solução para os dois projetos

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Criar uma nova biblioteca do Q#
  - Acesse **Arquivo** -> **Novo** -> **Projeto**
  - Digite "Q#" na caixa de pesquisa
  - Selecione **Biblioteca Q#**
  - Selecione **Avançar**
  - Escolha um nome e um local para a biblioteca
  - Verifique se a opção "Colocar projeto e solução no mesmo diretório" está **desmarcada**
  - Escolha **Criar**
- Criar um programa de host C# ou F#
  - Acesse **Arquivo** → **Novo** → **Projeto**
  - Selecione "Aplicativo de Console (.NET Core)" para C# ou F#
  - Selecione **Avançar**
  - Em *Solução*, selecione "Adicionar à solução"
  - Escolha um nome para o programa de host
  - Escolha **Criar**

**_

## <a name="calling-into-no-locq-from-net"></a>Chamar o Q# no .NET

Depois de configurar seus projetos seguindo as instruções acima, chame o Q# no aplicativo de console .NET.
O compilador Q# criará as classes .NET para cada operação e função Q# que permite executar seus programas quânticos em um simulador.

Por exemplo, a [amostra de interoperabilidade com o .NET](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) inclui o seguinte exemplo de uma operação Q#:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

Para chamar essa operação no .NET em um simulador quântico, use o método `Run` da classe .NET `RunAlgorithm` gerada pelo compilador Q#:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

_**
    
## <a name="next-steps"></a>Próximas etapas

Agora que você tem o Quantum Development Kit configurado para os dois aplicativos Q# e para interoperabilidade com o .NET, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
