---
title: Usando Q# bibliotecas adicionais
description: Saiba como adicionar bibliotecas adicionais Q# aos seus aplicativos Quantum.
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
no-loc:
- Q#
- $$v
ms.openlocfilehash: ef88ca765a394a7092eb0a60bf6f3615c082ef6a
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869572"
---
# <a name="using-additional-no-locq-libraries"></a><span data-ttu-id="f1258-103">Usando Q# bibliotecas adicionais</span><span class="sxs-lookup"><span data-stu-id="f1258-103">Using Additional Q# Libraries</span></span>

<span data-ttu-id="f1258-104">O kit de desenvolvimento Quantum fornece funcionalidade adicional específica de domínio por meio de _pacotes NuGet_ que podem ser adicionados aos seus Q# projetos.</span><span class="sxs-lookup"><span data-stu-id="f1258-104">The Quantum Development Kit provides additional domain-specific functionality through _NuGet packages_ that can be added to your Q# projects.</span></span>

| <span data-ttu-id="f1258-105">Q#Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1258-105">Q# Library</span></span>  | <span data-ttu-id="f1258-106">Pacote NuGet</span><span class="sxs-lookup"><span data-stu-id="f1258-106">NuGet package</span></span> | <span data-ttu-id="f1258-107">Observações</span><span class="sxs-lookup"><span data-stu-id="f1258-107">Notes</span></span> |
|---------|---------|--------|
| [<span data-ttu-id="f1258-108">Q#biblioteca padrão</span><span class="sxs-lookup"><span data-stu-id="f1258-108">Q# standard library</span></span>](xref:microsoft.quantum.libraries.standard.intro) | [<span data-ttu-id="f1258-109">**Microsoft. Quantum. Standard**</span><span class="sxs-lookup"><span data-stu-id="f1258-109">**Microsoft.Quantum.Standard**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | <span data-ttu-id="f1258-110">Incluído por padrão</span><span class="sxs-lookup"><span data-stu-id="f1258-110">Included by default</span></span> |
| [<span data-ttu-id="f1258-111">Biblioteca de química do Quantum</span><span class="sxs-lookup"><span data-stu-id="f1258-111">Quantum chemistry library</span></span>](xref:microsoft.quantum.chemistry.concepts.intro) | [<span data-ttu-id="f1258-112">**Microsoft.Quantum.Chemistry**</span><span class="sxs-lookup"><span data-stu-id="f1258-112">**Microsoft.Quantum.Chemistry**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [<span data-ttu-id="f1258-113">Biblioteca de numéricos do Quantum</span><span class="sxs-lookup"><span data-stu-id="f1258-113">Quantum numerics library</span></span>](xref:microsoft.quantum.numerics.intro) | [<span data-ttu-id="f1258-114">**Microsoft. Quantum. Numerics**</span><span class="sxs-lookup"><span data-stu-id="f1258-114">**Microsoft.Quantum.Numerics**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [<span data-ttu-id="f1258-115">Biblioteca de aprendizado de máquina quântico</span><span class="sxs-lookup"><span data-stu-id="f1258-115">Quantum machine learning library</span></span>](xref:microsoft.quantum.libraries.machine-learning.intro) | [<span data-ttu-id="f1258-116">**Microsoft.Quantum.MachineLearning**</span><span class="sxs-lookup"><span data-stu-id="f1258-116">**Microsoft.Quantum.MachineLearning**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

<span data-ttu-id="f1258-117">Depois de instalar o kit de desenvolvimento Quantum para uso com seu ambiente e idioma de host preferenciais, você poderá adicionar bibliotecas a projetos individuais com facilidade Q# sem nenhuma outra instalação.</span><span class="sxs-lookup"><span data-stu-id="f1258-117">Once you have installed the Quantum Development Kit for use with your preferred environment and host language, you can easily add libraries to individual Q# projects without any further installation.</span></span>

> [!NOTE]
> <span data-ttu-id="f1258-118">Algumas Q# bibliotecas podem funcionar bem com ferramentas adicionais que funcionam junto Q# com seus programas ou que se integram aos seus aplicativos host.</span><span class="sxs-lookup"><span data-stu-id="f1258-118">Some Q# libraries may work well with additional tools that work alongside your Q# programs, or that integrate with your host applications.</span></span>
> <span data-ttu-id="f1258-119">Por exemplo, as [instruções de instalação da biblioteca do química](xref:microsoft.quantum.chemistry.concepts.installation) descrevem como usar o [pacote **Microsoft. Quantum. química** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) junto com a plataforma química computacional NWChem e como instalar as `qdk-chem` ferramentas de linha de comando para trabalhar com dados de química do Quantum.</span><span class="sxs-lookup"><span data-stu-id="f1258-119">For example, the [chemistry library installation instructions](xref:microsoft.quantum.chemistry.concepts.installation) describe how to use the [**Microsoft.Quantum.Chemistry** package](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) together with the NWChem computational chemistry platform, and how to install the `qdk-chem` command-line tools for working with quantum chemistry data.</span></span>

## <a name="no-locq-command-line-applications-or-net-interopability"></a>[<span data-ttu-id="f1258-120">Q#aplicativos de linha de comando ou interoperabilidade do .NET</span><span class="sxs-lookup"><span data-stu-id="f1258-120">Q# command-line applications or .NET interopability</span></span>](#tab/tabid-csproj)

<span data-ttu-id="f1258-121">**Linha de comando ou Visual Studio Code:** Usando a linha de comando por conta própria ou de dentro Visual Studio Code, você pode usar o `dotnet` comando para adicionar uma referência de pacote NuGet ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="f1258-121">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add a NuGet package reference to your project.</span></span>
<span data-ttu-id="f1258-122">Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) , execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f1258-122">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package, run the following command:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

<span data-ttu-id="f1258-123">**Visual Studio:** Se você estiver usando o Visual Studio 2019 ou posterior, poderá adicionar Q# pacotes adicionais usando o Gerenciador de pacotes NuGet.</span><span class="sxs-lookup"><span data-stu-id="f1258-123">**Visual Studio:** If you are using Visual Studio 2019 or later, you can add additional Q# packages using the NuGet Package Manager.</span></span>
<span data-ttu-id="f1258-124">Para carregar um pacote:</span><span class="sxs-lookup"><span data-stu-id="f1258-124">To load a package:</span></span> 
1. <span data-ttu-id="f1258-125">Com um projeto aberto no Visual Studio, selecione **gerenciar pacotes NuGet...** no menu **projeto** .</span><span class="sxs-lookup"><span data-stu-id="f1258-125">With a project open in Visual Studio, select **Manage NuGet Packages...** from the **Project** menu.</span></span>

2. <span data-ttu-id="f1258-126">Clique em **procurar**, selecione **incluir pré-lançamento** e procure o nome do pacote "Microsoft. Quantum. Numerics".</span><span class="sxs-lookup"><span data-stu-id="f1258-126">Click **Browse**, select **Include prerelease** and search for the package name "Microsoft.Quantum.Numerics".</span></span> <span data-ttu-id="f1258-127">Isso listará os pacotes disponíveis para download.</span><span class="sxs-lookup"><span data-stu-id="f1258-127">This will list the packages available for download.</span></span>

3. <span data-ttu-id="f1258-128">Passe o mouse sobre **Microsoft. Quantum. Numerics** e clique na seta apontando para baixo à direita do número de versão para instalar o pacote numérico.</span><span class="sxs-lookup"><span data-stu-id="f1258-128">Hover over **Microsoft.Quantum.Numerics** and click the downward-pointing arrow to the right of the version number to install the numerics package.</span></span>

<span data-ttu-id="f1258-129">Para obter mais detalhes, consulte o [Guia de interface do usuário do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="f1258-129">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="f1258-130">Como alternativa, você pode usar o console do Gerenciador de pacotes para adicionar a biblioteca de numéricos ao seu projeto por meio da interface de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f1258-130">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![Usar o console do Gerenciador de pacotes na linha de comando](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="f1258-132">No console do Gerenciador de pacotes, execute o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f1258-132">From the Package Manager Console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="f1258-133">Para obter mais detalhes, consulte o [Guia do console do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="f1258-133">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

## <a name="ino-locq-notebooks"></a>[<span data-ttu-id="f1258-134">Q#Blocos de anotações</span><span class="sxs-lookup"><span data-stu-id="f1258-134">IQ# Notebooks</span></span>](#tab/tabid-notebook)

<span data-ttu-id="f1258-135">Você pode disponibilizar pacotes adicionais para uso em um Q# bloco de anotações I usando o [ `%package` comando mágico](xref:microsoft.quantum.iqsharp.magic-ref.package).</span><span class="sxs-lookup"><span data-stu-id="f1258-135">You can make additional packages available for use in an IQ# Notebook by using the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="f1258-136">Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) para uso em um Q# bloco de anotações I, execute o seguinte comando em uma célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="f1258-136">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following command in a notebook cell:</span></span>

```
%package Microsoft.Quantum.Numerics
```

<span data-ttu-id="f1258-137">Após esse comando, o pacote estará disponível para qualquer célula no bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="f1258-137">Following this command, the package is available to any cells within the notebook.</span></span>
<span data-ttu-id="f1258-138">Para disponibilizar o pacote do Q# código no espaço de trabalho atual, recarregue o espaço de trabalho depois de adicionar o pacote:</span><span class="sxs-lookup"><span data-stu-id="f1258-138">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```
%workspace reload
```

## <a name="python-interoperability"></a>[<span data-ttu-id="f1258-139">Interoperabilidade do Python</span><span class="sxs-lookup"><span data-stu-id="f1258-139">Python interoperability</span></span>](#tab/tabid-python)


<span data-ttu-id="f1258-140">Você pode disponibilizar pacotes adicionais para uso em um programa de host do Python usando o [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) método.</span><span class="sxs-lookup"><span data-stu-id="f1258-140">You can make additional packages available for use in a Python host program by using the [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) method.</span></span>
<span data-ttu-id="f1258-141">Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) para uso em um Q# bloco de anotações I, execute o seguinte código Python:</span><span class="sxs-lookup"><span data-stu-id="f1258-141">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following Python code:</span></span>

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

<span data-ttu-id="f1258-142">Após esse comando, o pacote será disponibilizado para qualquer Q# código compilado usando `qsharp.compile` .</span><span class="sxs-lookup"><span data-stu-id="f1258-142">Following this command, the package will be made available to any Q# code compiled using `qsharp.compile`.</span></span>
<span data-ttu-id="f1258-143">Para disponibilizar o pacote do Q# código no espaço de trabalho atual, recarregue o espaço de trabalho depois de adicionar o pacote:</span><span class="sxs-lookup"><span data-stu-id="f1258-143">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```python
qsharp.reload()
```

***
