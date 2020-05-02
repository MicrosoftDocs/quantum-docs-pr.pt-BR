---
title: Desenvolvimento com Q# + C#
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 5bcb036b0b32e64d43f90e9a068d9dcc237890ba
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680173"
---
# <a name="using-q-with-c-and-f"></a>Usando Q # com C\# e F\#

O Q # foi criado para ser bem executado com linguagens .NET, como C# e F #.
Neste guia, demonstraremos como usar o Q # com um programa de host escrito em uma linguagem .NET.

## <a name="prerequisites"></a>Pré-requisitos

- Instale o kit de desenvolvimento Quantum [para uso com projetos de linha de comando Q #](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-q-library-and-a-net-host"></a>Criando uma biblioteca de Q # e um host .NET

A primeira etapa é criar projetos para a biblioteca do Q # e para o host do .NET que chamará as operações e funções definidas em sua biblioteca do Q #.

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Criar uma nova biblioteca do Q #
  - Ir para **arquivo** -> **novo** -> **projeto**
  - Digite "Q #" na caixa de pesquisa
  - Selecionar **biblioteca de Q #**
  - Selecione **Avançar**.
  - Escolha um nome e um local para sua biblioteca
  - Certifique-se de que "colocar projeto e solução no mesmo diretório" esteja **desmarcado**
  - Selecione **criar**
- Criar um novo programa de host C# ou F #
  - Vá para **arquivo** → **novo** **projeto** →
  - Selecione "aplicativo de console (.NET Core") "para C# ou F #
  - Selecione **Avançar**.
  - Em *solução*, selecione "adicionar à solução"
  - Escolha um nome para o programa host
  - Selecione **criar**

### <a name="visual-studio-code-or-command-line"></a>[Visual Studio Code ou linha de comando](#tab/tabid-cmdline)

- Criar uma nova biblioteca do Q #

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Criar um novo projeto de console C# ou F #

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Adicione sua biblioteca do Q # como uma referência do seu programa de host

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- Adicional Criar uma solução para ambos os projetos

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a>Chamando Q # do .NET

Depois de configurar seus projetos seguindo as instruções acima, você pode chamar o Q # do seu aplicativo de console .NET.
O compilador Q # criará classes .NET para cada operação Q # e função que permitirá que você execute seus programas Quantum em um simulador.

Por exemplo, o [exemplo de interoperabilidade .net](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) inclui o exemplo a seguir de uma operação Q #:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

Para chamar essa operação do .NET em um simulador Quantum, você pode usar `Run` o método da `RunAlgorithm` classe .net gerada pelo compilador Q #:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[Fixo #](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="whats-next"></a>O que vem a seguir?

Agora que você tem o kit de desenvolvimento Quantum configurado para os dois programas de linha de comando Q # e para interoperabilidade com o .NET, você pode escrever e executar [seu primeiro programa Quantum](xref:microsoft.quantum.write-program).
