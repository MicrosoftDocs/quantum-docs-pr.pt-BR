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
# <a name="using-q-with-c-and-f"></a><span data-ttu-id="ebfc8-102">Usando Q # com C\# e F\#</span><span class="sxs-lookup"><span data-stu-id="ebfc8-102">Using Q# with C\# and F\#</span></span>

<span data-ttu-id="ebfc8-103">O Q # foi criado para ser bem executado com linguagens .NET, como C# e F #.</span><span class="sxs-lookup"><span data-stu-id="ebfc8-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="ebfc8-104">Neste guia, demonstraremos como usar o Q # com um programa de host escrito em uma linguagem .NET.</span><span class="sxs-lookup"><span data-stu-id="ebfc8-104">In this guide, we'll demonstrate how to use Q# with a host program written in a .NET language.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ebfc8-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ebfc8-105">Prerequisites</span></span>

- <span data-ttu-id="ebfc8-106">Instale o kit de desenvolvimento Quantum [para uso com projetos de linha de comando Q #](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="ebfc8-106">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="ebfc8-107">Criando uma biblioteca de Q # e um host .NET</span><span class="sxs-lookup"><span data-stu-id="ebfc8-107">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="ebfc8-108">A primeira etapa é criar projetos para a biblioteca do Q # e para o host do .NET que chamará as operações e funções definidas em sua biblioteca do Q #.</span><span class="sxs-lookup"><span data-stu-id="ebfc8-108">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

### <a name="visual-studio-2019"></a>[<span data-ttu-id="ebfc8-109">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ebfc8-109">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="ebfc8-110">Criar uma nova biblioteca do Q #</span><span class="sxs-lookup"><span data-stu-id="ebfc8-110">Create a new Q# library</span></span>
  - <span data-ttu-id="ebfc8-111">Ir para **arquivo** -> **novo** -> **projeto**</span><span class="sxs-lookup"><span data-stu-id="ebfc8-111">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="ebfc8-112">Digite "Q #" na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="ebfc8-112">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="ebfc8-113">Selecionar **biblioteca de Q #**</span><span class="sxs-lookup"><span data-stu-id="ebfc8-113">Select **Q# Library**</span></span>
  - <span data-ttu-id="ebfc8-114">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ebfc8-114">Select **Next**</span></span>
  - <span data-ttu-id="ebfc8-115">Escolha um nome e um local para sua biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebfc8-115">Choose a name and location for your library</span></span>
  - <span data-ttu-id="ebfc8-116">Certifique-se de que "colocar projeto e solução no mesmo diretório" esteja **desmarcado**</span><span class="sxs-lookup"><span data-stu-id="ebfc8-116">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="ebfc8-117">Selecione **criar**</span><span class="sxs-lookup"><span data-stu-id="ebfc8-117">Select **Create**</span></span>
- <span data-ttu-id="ebfc8-118">Criar um novo programa de host C# ou F #</span><span class="sxs-lookup"><span data-stu-id="ebfc8-118">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="ebfc8-119">Vá para **arquivo** → **novo** **projeto** →</span><span class="sxs-lookup"><span data-stu-id="ebfc8-119">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="ebfc8-120">Selecione "aplicativo de console (.NET Core") "para C# ou F #</span><span class="sxs-lookup"><span data-stu-id="ebfc8-120">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="ebfc8-121">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ebfc8-121">Select **Next**</span></span>
  - <span data-ttu-id="ebfc8-122">Em *solução*, selecione "adicionar à solução"</span><span class="sxs-lookup"><span data-stu-id="ebfc8-122">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="ebfc8-123">Escolha um nome para o programa host</span><span class="sxs-lookup"><span data-stu-id="ebfc8-123">Choose a name for your host program</span></span>
  - <span data-ttu-id="ebfc8-124">Selecione **criar**</span><span class="sxs-lookup"><span data-stu-id="ebfc8-124">Select **Create**</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="ebfc8-125">Visual Studio Code ou linha de comando</span><span class="sxs-lookup"><span data-stu-id="ebfc8-125">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="ebfc8-126">Criar uma nova biblioteca do Q #</span><span class="sxs-lookup"><span data-stu-id="ebfc8-126">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="ebfc8-127">Criar um novo projeto de console C# ou F #</span><span class="sxs-lookup"><span data-stu-id="ebfc8-127">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="ebfc8-128">Adicione sua biblioteca do Q # como uma referência do seu programa de host</span><span class="sxs-lookup"><span data-stu-id="ebfc8-128">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="ebfc8-129">Adicional Criar uma solução para ambos os projetos</span><span class="sxs-lookup"><span data-stu-id="ebfc8-129">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="ebfc8-130">Chamando Q # do .NET</span><span class="sxs-lookup"><span data-stu-id="ebfc8-130">Calling into Q# from .NET</span></span>

<span data-ttu-id="ebfc8-131">Depois de configurar seus projetos seguindo as instruções acima, você pode chamar o Q # do seu aplicativo de console .NET.</span><span class="sxs-lookup"><span data-stu-id="ebfc8-131">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="ebfc8-132">O compilador Q # criará classes .NET para cada operação Q # e função que permitirá que você execute seus programas Quantum em um simulador.</span><span class="sxs-lookup"><span data-stu-id="ebfc8-132">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="ebfc8-133">Por exemplo, o [exemplo de interoperabilidade .net](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) inclui o exemplo a seguir de uma operação Q #:</span><span class="sxs-lookup"><span data-stu-id="ebfc8-133">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="ebfc8-134">Para chamar essa operação do .NET em um simulador Quantum, você pode usar `Run` o método da `RunAlgorithm` classe .net gerada pelo compilador Q #:</span><span class="sxs-lookup"><span data-stu-id="ebfc8-134">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="ebfc8-135">C#</span><span class="sxs-lookup"><span data-stu-id="ebfc8-135">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="ebfc8-136">Fixo #</span><span class="sxs-lookup"><span data-stu-id="ebfc8-136">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="whats-next"></a><span data-ttu-id="ebfc8-137">O que vem a seguir?</span><span class="sxs-lookup"><span data-stu-id="ebfc8-137">What's next?</span></span>

<span data-ttu-id="ebfc8-138">Agora que você tem o kit de desenvolvimento Quantum configurado para os dois programas de linha de comando Q # e para interoperabilidade com o .NET, você pode escrever e executar [seu primeiro programa Quantum](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="ebfc8-138">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
