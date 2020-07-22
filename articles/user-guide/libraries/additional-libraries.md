---
title: 'Usando bibliotecas de Q # adicionais'
description: 'Saiba como adicionar mais bibliotecas Q # a seus aplicativos Quantum.'
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
ms.openlocfilehash: b82113b925870d07c8a28aecd50176e009826062
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86872605"
---
# <a name="using-additional-q-libraries"></a><span data-ttu-id="2c021-103">Usando bibliotecas de Q # adicionais</span><span class="sxs-lookup"><span data-stu-id="2c021-103">Using Additional Q# Libraries</span></span>

<span data-ttu-id="2c021-104">O kit de desenvolvimento Quantum fornece funcionalidade adicional específica de domínio por meio de _pacotes NuGet_ que podem ser adicionados aos seus projetos Q #.</span><span class="sxs-lookup"><span data-stu-id="2c021-104">The Quantum Development Kit provides additional domain-specific functionality through _NuGet packages_ that can be added to your Q# projects.</span></span>

| <span data-ttu-id="2c021-105">Biblioteca de Q #</span><span class="sxs-lookup"><span data-stu-id="2c021-105">Q# Library</span></span>  | <span data-ttu-id="2c021-106">Pacote NuGet</span><span class="sxs-lookup"><span data-stu-id="2c021-106">NuGet package</span></span> | <span data-ttu-id="2c021-107">Observações</span><span class="sxs-lookup"><span data-stu-id="2c021-107">Notes</span></span> |
|---------|---------|--------|
| [<span data-ttu-id="2c021-108">P # biblioteca padrão</span><span class="sxs-lookup"><span data-stu-id="2c021-108">Q# standard library</span></span>](xref:microsoft.quantum.libraries.standard.intro) | [<span data-ttu-id="2c021-109">**Microsoft. Quantum. Standard**</span><span class="sxs-lookup"><span data-stu-id="2c021-109">**Microsoft.Quantum.Standard**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | <span data-ttu-id="2c021-110">Incluído por padrão</span><span class="sxs-lookup"><span data-stu-id="2c021-110">Included by default</span></span> |
| [<span data-ttu-id="2c021-111">Biblioteca de química do Quantum</span><span class="sxs-lookup"><span data-stu-id="2c021-111">Quantum chemistry library</span></span>](xref:microsoft.quantum.chemistry.concepts.intro) | [<span data-ttu-id="2c021-112">**Microsoft.Quantum.Chemistry**</span><span class="sxs-lookup"><span data-stu-id="2c021-112">**Microsoft.Quantum.Chemistry**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [<span data-ttu-id="2c021-113">Biblioteca de numéricos do Quantum</span><span class="sxs-lookup"><span data-stu-id="2c021-113">Quantum numerics library</span></span>](xref:microsoft.quantum.numerics.intro) | [<span data-ttu-id="2c021-114">**Microsoft. Quantum. Numerics**</span><span class="sxs-lookup"><span data-stu-id="2c021-114">**Microsoft.Quantum.Numerics**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [<span data-ttu-id="2c021-115">Biblioteca de aprendizado de máquina quântico</span><span class="sxs-lookup"><span data-stu-id="2c021-115">Quantum machine learning library</span></span>](xref:microsoft.quantum.libraries.machine-learning.intro) | [<span data-ttu-id="2c021-116">**Microsoft.Quantum.MachineLearning**</span><span class="sxs-lookup"><span data-stu-id="2c021-116">**Microsoft.Quantum.MachineLearning**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

<span data-ttu-id="2c021-117">Depois de instalar o kit de desenvolvimento do Quantum para uso com seu ambiente e idioma de host preferenciais, você poderá adicionar bibliotecas a projetos individuais de Q # com facilidade sem nenhuma outra instalação.</span><span class="sxs-lookup"><span data-stu-id="2c021-117">Once you have installed the Quantum Development Kit for use with your preferred environment and host language, you can easily add libraries to individual Q# projects without any further installation.</span></span>

> [!NOTE]
> <span data-ttu-id="2c021-118">Algumas bibliotecas de Q # podem funcionar bem com ferramentas adicionais que funcionam junto com os programas Q # ou que se integram aos seus aplicativos host.</span><span class="sxs-lookup"><span data-stu-id="2c021-118">Some Q# libraries may work well with additional tools that work alongside your Q# programs, or that integrate with your host applications.</span></span>
> <span data-ttu-id="2c021-119">Por exemplo, as [instruções de instalação da biblioteca do química](xref:microsoft.quantum.chemistry.concepts.installation) descrevem como usar o [pacote **Microsoft. Quantum. química** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) junto com a plataforma química computacional NWChem e como instalar as `qdk-chem` ferramentas de linha de comando para trabalhar com dados de química do Quantum.</span><span class="sxs-lookup"><span data-stu-id="2c021-119">For example, the [chemistry library installation instructions](xref:microsoft.quantum.chemistry.concepts.installation) describe how to use the [**Microsoft.Quantum.Chemistry** package](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) together with the NWChem computational chemistry platform, and how to install the `qdk-chem` command-line tools for working with quantum chemistry data.</span></span>

## <a name="q-command-line-applications-or-net-interopability"></a>[<span data-ttu-id="2c021-120">P # aplicativos de linha de comando ou interoperabilidade do .NET</span><span class="sxs-lookup"><span data-stu-id="2c021-120">Q# command-line applications or .NET interopability</span></span>](#tab/tabid-csproj)

<span data-ttu-id="2c021-121">**Linha de comando ou Visual Studio Code:** Usando a linha de comando por conta própria ou de dentro Visual Studio Code, você pode usar o `dotnet` comando para adicionar uma referência de pacote NuGet ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="2c021-121">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add a NuGet package reference to your project.</span></span>
<span data-ttu-id="2c021-122">Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) , execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="2c021-122">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package, run the following command:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

<span data-ttu-id="2c021-123">**Visual Studio:** Se você estiver usando o Visual Studio 2019 ou posterior, poderá adicionar mais pacotes Q # usando o Gerenciador de pacotes NuGet.</span><span class="sxs-lookup"><span data-stu-id="2c021-123">**Visual Studio:** If you are using Visual Studio 2019 or later, you can add additional Q# packages using the NuGet Package Manager.</span></span>
<span data-ttu-id="2c021-124">Para carregar um pacote:</span><span class="sxs-lookup"><span data-stu-id="2c021-124">To load a package:</span></span> 
1. <span data-ttu-id="2c021-125">Com um projeto aberto no Visual Studio, selecione **gerenciar pacotes NuGet...** no menu **projeto** .</span><span class="sxs-lookup"><span data-stu-id="2c021-125">With a project open in Visual Studio, select **Manage NuGet Packages...** from the **Project** menu.</span></span>

2. <span data-ttu-id="2c021-126">Clique em **procurar**, selecione **incluir pré-lançamento** e procure o nome do pacote "Microsoft. Quantum. Numerics".</span><span class="sxs-lookup"><span data-stu-id="2c021-126">Click **Browse**, select **Include prerelease** and search for the package name "Microsoft.Quantum.Numerics".</span></span> <span data-ttu-id="2c021-127">Isso listará os pacotes disponíveis para download.</span><span class="sxs-lookup"><span data-stu-id="2c021-127">This will list the packages available for download.</span></span>

3. <span data-ttu-id="2c021-128">Passe o mouse sobre **Microsoft. Quantum. Numerics** e clique na seta apontando para baixo à direita do número de versão para instalar o pacote numérico.</span><span class="sxs-lookup"><span data-stu-id="2c021-128">Hover over **Microsoft.Quantum.Numerics** and click the downward-pointing arrow to the right of the version number to install the numerics package.</span></span>

<span data-ttu-id="2c021-129">Para obter mais detalhes, consulte o [Guia de interface do usuário do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="2c021-129">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="2c021-130">Como alternativa, você pode usar o console do Gerenciador de pacotes para adicionar a biblioteca de numéricos ao seu projeto por meio da interface de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="2c021-130">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![Usar o console do Gerenciador de pacotes na linha de comando](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="2c021-132">No console do Gerenciador de pacotes, execute o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2c021-132">From the Package Manager Console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="2c021-133">Para obter mais detalhes, consulte o [Guia do console do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="2c021-133">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

## <a name="iq-notebooks"></a>[<span data-ttu-id="2c021-134">Blocos de anotações de IQ #</span><span class="sxs-lookup"><span data-stu-id="2c021-134">IQ# Notebooks</span></span>](#tab/tabid-notebook)

<span data-ttu-id="2c021-135">Você pode disponibilizar pacotes adicionais para uso em um notebook de IQ # usando o [ `%package` comando mágico](xref:microsoft.quantum.iqsharp.magic-ref.package).</span><span class="sxs-lookup"><span data-stu-id="2c021-135">You can make additional packages available for use in an IQ# Notebook by using the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="2c021-136">Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) para uso em um notebook de IQ #, execute o seguinte comando em uma célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="2c021-136">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following command in a notebook cell:</span></span>

```
%package Microsoft.Quantum.Numerics
```

<span data-ttu-id="2c021-137">Após esse comando, o pacote estará disponível para qualquer célula no bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="2c021-137">Following this command, the package is available to any cells within the notebook.</span></span>
<span data-ttu-id="2c021-138">Para disponibilizar o pacote do código Q # no espaço de trabalho atual, recarregue o espaço de trabalho depois de adicionar o pacote:</span><span class="sxs-lookup"><span data-stu-id="2c021-138">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```
%workspace reload
```

## <a name="python-interoperability"></a>[<span data-ttu-id="2c021-139">Interoperabilidade do Python</span><span class="sxs-lookup"><span data-stu-id="2c021-139">Python interoperability</span></span>](#tab/tabid-python)


<span data-ttu-id="2c021-140">Você pode disponibilizar pacotes adicionais para uso em um programa de host do Python usando o [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) método.</span><span class="sxs-lookup"><span data-stu-id="2c021-140">You can make additional packages available for use in a Python host program by using the [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) method.</span></span>
<span data-ttu-id="2c021-141">Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) para uso em um bloco de anotações de IQ #, execute o seguinte código Python:</span><span class="sxs-lookup"><span data-stu-id="2c021-141">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following Python code:</span></span>

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

<span data-ttu-id="2c021-142">Após esse comando, o pacote será disponibilizado para qualquer código Q # compilado usando `qsharp.compile` .</span><span class="sxs-lookup"><span data-stu-id="2c021-142">Following this command, the package will be made available to any Q# code compiled using `qsharp.compile`.</span></span>
<span data-ttu-id="2c021-143">Para disponibilizar o pacote do código Q # no espaço de trabalho atual, recarregue o espaço de trabalho depois de adicionar o pacote:</span><span class="sxs-lookup"><span data-stu-id="2c021-143">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```python
qsharp.reload()
```

***
