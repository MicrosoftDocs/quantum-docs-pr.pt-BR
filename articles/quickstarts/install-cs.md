---
title: Desenvolver com o Q# e o .NET
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 13d73bdf0287941c89e03ba63869095e5fca4e70
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867549"
---
# <a name="develop-with-no-locq-and-net"></a><span data-ttu-id="ccb38-102">Desenvolver com o Q# e o .NET</span><span class="sxs-lookup"><span data-stu-id="ccb38-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="ccb38-103">O Q# foi criado visando a uma boa compatibilidade com as linguagens .NET, como C# e F#.</span><span class="sxs-lookup"><span data-stu-id="ccb38-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="ccb38-104">Neste guia, demonstramos como usar o Q# com um programa de host escrito em uma linguagem .NET.</span><span class="sxs-lookup"><span data-stu-id="ccb38-104">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="ccb38-105">Primeiro, criamos o aplicativo Q# e o host .NET, depois demonstramos como chamar Q# do host.</span><span class="sxs-lookup"><span data-stu-id="ccb38-105">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ccb38-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb38-106">Prerequisites</span></span>

- <span data-ttu-id="ccb38-107">Instalar o Quantum Development Kit [para uso com projetos de linha de comando do Q#](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="ccb38-107">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-no-locq-library-and-a-net-host"></a><span data-ttu-id="ccb38-108">Criar uma biblioteca do Q# e um host do .NET</span><span class="sxs-lookup"><span data-stu-id="ccb38-108">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="ccb38-109">A primeira etapa é criar projetos para a biblioteca do Q# e para o host do .NET que chamará as operações e as funções definidas na biblioteca do Q#.</span><span class="sxs-lookup"><span data-stu-id="ccb38-109">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="ccb38-110">Siga as instruções na guia correspondente ao seu ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="ccb38-110">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="ccb38-111">Se estiver usando um editor diferente do Visual Studio ou do VS Code, basta seguir as etapas referentes à linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ccb38-111">If you are using an editor other than Visual Studio or VS Code, simply follow the command line steps.</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="ccb38-112">Visual Studio Code ou linha de comando</span><span class="sxs-lookup"><span data-stu-id="ccb38-112">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="ccb38-113">Criar uma nova biblioteca do Q#</span><span class="sxs-lookup"><span data-stu-id="ccb38-113">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="ccb38-114">Criar um projeto de console C# ou F#</span><span class="sxs-lookup"><span data-stu-id="ccb38-114">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="ccb38-115">Adicione a biblioteca do Q# como uma referência do programa de host</span><span class="sxs-lookup"><span data-stu-id="ccb38-115">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="ccb38-116">[Opcional] Crie uma solução para os dois projetos</span><span class="sxs-lookup"><span data-stu-id="ccb38-116">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="ccb38-117">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ccb38-117">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="ccb38-118">Criar uma nova biblioteca do Q#</span><span class="sxs-lookup"><span data-stu-id="ccb38-118">Create a new Q# library</span></span>
  - <span data-ttu-id="ccb38-119">Acesse **Arquivo** -> **Novo** -> **Projeto**</span><span class="sxs-lookup"><span data-stu-id="ccb38-119">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="ccb38-120">Digite "Q#" na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="ccb38-120">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="ccb38-121">Selecione **Biblioteca Q#**</span><span class="sxs-lookup"><span data-stu-id="ccb38-121">Select **Q# Library**</span></span>
  - <span data-ttu-id="ccb38-122">Selecione **Avançar**</span><span class="sxs-lookup"><span data-stu-id="ccb38-122">Select **Next**</span></span>
  - <span data-ttu-id="ccb38-123">Escolha um nome e um local para a biblioteca</span><span class="sxs-lookup"><span data-stu-id="ccb38-123">Choose a name and location for your library</span></span>
  - <span data-ttu-id="ccb38-124">Verifique se a opção "Colocar projeto e solução no mesmo diretório" está **desmarcada**</span><span class="sxs-lookup"><span data-stu-id="ccb38-124">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="ccb38-125">Escolha **Criar**</span><span class="sxs-lookup"><span data-stu-id="ccb38-125">Select **Create**</span></span>
- <span data-ttu-id="ccb38-126">Criar um programa de host C# ou F#</span><span class="sxs-lookup"><span data-stu-id="ccb38-126">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="ccb38-127">Acesse **Arquivo** → **Novo** → **Projeto**</span><span class="sxs-lookup"><span data-stu-id="ccb38-127">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="ccb38-128">Selecione "Aplicativo de Console (.NET Core)" para C# ou F#</span><span class="sxs-lookup"><span data-stu-id="ccb38-128">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="ccb38-129">Selecione **Avançar**</span><span class="sxs-lookup"><span data-stu-id="ccb38-129">Select **Next**</span></span>
  - <span data-ttu-id="ccb38-130">Em *Solução*, selecione "Adicionar à solução"</span><span class="sxs-lookup"><span data-stu-id="ccb38-130">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="ccb38-131">Escolha um nome para o programa de host</span><span class="sxs-lookup"><span data-stu-id="ccb38-131">Choose a name for your host program</span></span>
  - <span data-ttu-id="ccb38-132">Escolha **Criar**</span><span class="sxs-lookup"><span data-stu-id="ccb38-132">Select **Create**</span></span>

***

## <a name="calling-into-no-locq-from-net"></a><span data-ttu-id="ccb38-133">Chamar o Q# no .NET</span><span class="sxs-lookup"><span data-stu-id="ccb38-133">Calling into Q# from .NET</span></span>

<span data-ttu-id="ccb38-134">Depois de configurar seus projetos seguindo as instruções acima, chame o Q# no aplicativo de console .NET.</span><span class="sxs-lookup"><span data-stu-id="ccb38-134">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="ccb38-135">O compilador Q# criará as classes .NET para cada operação e função Q# que permite executar seus programas quânticos em um simulador.</span><span class="sxs-lookup"><span data-stu-id="ccb38-135">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="ccb38-136">Por exemplo, a [amostra de interoperabilidade com o .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) inclui o seguinte exemplo de uma operação Q#:</span><span class="sxs-lookup"><span data-stu-id="ccb38-136">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="ccb38-137">Para chamar essa operação no .NET em um simulador quântico, use o método `Run` da classe .NET `RunAlgorithm` gerada pelo compilador Q#:</span><span class="sxs-lookup"><span data-stu-id="ccb38-137">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="ccb38-138">C#</span><span class="sxs-lookup"><span data-stu-id="ccb38-138">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="ccb38-139">F#</span><span class="sxs-lookup"><span data-stu-id="ccb38-139">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="ccb38-140">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="ccb38-140">Next steps</span></span>

<span data-ttu-id="ccb38-141">Agora que você tem o Quantum Development Kit configurado para os dois programas de linha de comando do Q# e para interoperabilidade com o .NET, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="ccb38-141">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
