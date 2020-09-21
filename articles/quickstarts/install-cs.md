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
ms.openlocfilehash: 96a1d0d75f3ff7de11407fd76479cbae86ce7571
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759265"
---
# <a name="develop-with-no-locq-and-net"></a><span data-ttu-id="a7fef-102">Desenvolver com o Q# e o .NET</span><span class="sxs-lookup"><span data-stu-id="a7fef-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="a7fef-103">O Q# foi criado visando a uma boa compatibilidade com as linguagens .NET, como C# e F#.</span><span class="sxs-lookup"><span data-stu-id="a7fef-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="a7fef-104">Neste guia, demonstramos como usar o Q# com um programa de host escrito em uma linguagem .NET.</span><span class="sxs-lookup"><span data-stu-id="a7fef-104">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="a7fef-105">Primeiro, criamos o aplicativo Q# e o host .NET, depois demonstramos como chamar Q# do host.</span><span class="sxs-lookup"><span data-stu-id="a7fef-105">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a7fef-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a7fef-106">Prerequisites</span></span>

- <span data-ttu-id="a7fef-107">Instalar o Quantum Development Kit [para uso com projetos do Q#](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="a7fef-107">Install the Quantum Development Kit [for use with Q# projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-no-locq-library-and-a-net-host"></a><span data-ttu-id="a7fef-108">Criar uma biblioteca do Q# e um host do .NET</span><span class="sxs-lookup"><span data-stu-id="a7fef-108">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="a7fef-109">A primeira etapa é criar projetos para a biblioteca do Q# e para o host do .NET que chamará as operações e as funções definidas na biblioteca do Q#.</span><span class="sxs-lookup"><span data-stu-id="a7fef-109">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="a7fef-110">Siga as instruções na guia correspondente ao seu ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="a7fef-110">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="a7fef-111">Se estiver usando um editor diferente do Visual Studio ou do VS Code, basta seguir as etapas do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="a7fef-111">If you are using an editor other than Visual Studio or VS Code, simply follow the command prompt steps.</span></span>

### <a name="visual-studio-code-or-command-prompt"></a>[<span data-ttu-id="a7fef-112">Visual Studio Code ou prompt de comando</span><span class="sxs-lookup"><span data-stu-id="a7fef-112">Visual Studio Code or command prompt</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="a7fef-113">Criar uma nova biblioteca do Q#</span><span class="sxs-lookup"><span data-stu-id="a7fef-113">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="a7fef-114">Criar um projeto de console C# ou F#</span><span class="sxs-lookup"><span data-stu-id="a7fef-114">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="a7fef-115">Adicione a biblioteca do Q# como uma referência do programa de host</span><span class="sxs-lookup"><span data-stu-id="a7fef-115">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="a7fef-116">[Opcional] Crie uma solução para os dois projetos</span><span class="sxs-lookup"><span data-stu-id="a7fef-116">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="a7fef-117">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="a7fef-117">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="a7fef-118">Criar uma nova biblioteca do Q#</span><span class="sxs-lookup"><span data-stu-id="a7fef-118">Create a new Q# library</span></span>
  - <span data-ttu-id="a7fef-119">Acesse **Arquivo** -> **Novo** -> **Projeto**</span><span class="sxs-lookup"><span data-stu-id="a7fef-119">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="a7fef-120">Digite "Q#" na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="a7fef-120">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="a7fef-121">Selecione **Biblioteca Q#**</span><span class="sxs-lookup"><span data-stu-id="a7fef-121">Select **Q# Library**</span></span>
  - <span data-ttu-id="a7fef-122">Selecione **Avançar**</span><span class="sxs-lookup"><span data-stu-id="a7fef-122">Select **Next**</span></span>
  - <span data-ttu-id="a7fef-123">Escolha um nome e um local para a biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7fef-123">Choose a name and location for your library</span></span>
  - <span data-ttu-id="a7fef-124">Verifique se a opção "Colocar projeto e solução no mesmo diretório" está **desmarcada**</span><span class="sxs-lookup"><span data-stu-id="a7fef-124">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="a7fef-125">Escolha **Criar**</span><span class="sxs-lookup"><span data-stu-id="a7fef-125">Select **Create**</span></span>
- <span data-ttu-id="a7fef-126">Criar um programa de host C# ou F#</span><span class="sxs-lookup"><span data-stu-id="a7fef-126">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="a7fef-127">Acesse **Arquivo** → **Novo** → **Projeto**</span><span class="sxs-lookup"><span data-stu-id="a7fef-127">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="a7fef-128">Selecione "Aplicativo de Console (.NET Core)" para C# ou F#</span><span class="sxs-lookup"><span data-stu-id="a7fef-128">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="a7fef-129">Selecione **Avançar**</span><span class="sxs-lookup"><span data-stu-id="a7fef-129">Select **Next**</span></span>
  - <span data-ttu-id="a7fef-130">Em *Solução*, selecione "Adicionar à solução"</span><span class="sxs-lookup"><span data-stu-id="a7fef-130">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="a7fef-131">Escolha um nome para o programa de host</span><span class="sxs-lookup"><span data-stu-id="a7fef-131">Choose a name for your host program</span></span>
  - <span data-ttu-id="a7fef-132">Escolha **Criar**</span><span class="sxs-lookup"><span data-stu-id="a7fef-132">Select **Create**</span></span>

***

## <a name="calling-into-no-locq-from-net"></a><span data-ttu-id="a7fef-133">Chamar o Q# no .NET</span><span class="sxs-lookup"><span data-stu-id="a7fef-133">Calling into Q# from .NET</span></span>

<span data-ttu-id="a7fef-134">Depois de configurar seus projetos seguindo as instruções acima, chame o Q# no aplicativo de console .NET.</span><span class="sxs-lookup"><span data-stu-id="a7fef-134">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="a7fef-135">O compilador Q# criará as classes .NET para cada operação e função Q# que permite executar seus programas quânticos em um simulador.</span><span class="sxs-lookup"><span data-stu-id="a7fef-135">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="a7fef-136">Por exemplo, a [amostra de interoperabilidade com o .NET](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) inclui o seguinte exemplo de uma operação Q#:</span><span class="sxs-lookup"><span data-stu-id="a7fef-136">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="a7fef-137">Para chamar essa operação no .NET em um simulador quântico, use o método `Run` da classe .NET `RunAlgorithm` gerada pelo compilador Q#:</span><span class="sxs-lookup"><span data-stu-id="a7fef-137">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="a7fef-138">C#</span><span class="sxs-lookup"><span data-stu-id="a7fef-138">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="a7fef-139">F#</span><span class="sxs-lookup"><span data-stu-id="a7fef-139">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="a7fef-140">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a7fef-140">Next steps</span></span>

<span data-ttu-id="a7fef-141">Agora que você tem o Quantum Development Kit configurado para os dois aplicativos Q# e para interoperabilidade com o .NET, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="a7fef-141">Now that you have the Quantum Development Kit set up for both Q# applications and interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
