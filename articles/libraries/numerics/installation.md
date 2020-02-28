---
title: Biblioteca de numéricos do Microsoft Quantum-instalação e validação
description: Saiba como adicionar a biblioteca de números de Quantum da Microsoft à sua instalação do Visual Studio 2019 ou posterior.
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: cb0d00a509b3986b605dd7f15f9bccc0661bb894
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906331"
---
# <a name="numerics-library-installation-and-validation"></a><span data-ttu-id="64f42-103">Instalação e validação de biblioteca de numéricos</span><span class="sxs-lookup"><span data-stu-id="64f42-103">Numerics Library Installation and Validation</span></span>

<span data-ttu-id="64f42-104">O kit de desenvolvimento Quantum fornece suporte para a funcionalidade de numéricos por meio do pacote NuGet [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) .</span><span class="sxs-lookup"><span data-stu-id="64f42-104">The Quantum Development Kit provides support for numerics functionality through the [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) NuGet package.</span></span>

<span data-ttu-id="64f42-105">**Visual Studio > = 2019:** Se você estiver usando o Visual Studio 2019 ou posterior, poderá adicionar o pacote numéricos usando o Gerenciador de pacotes NuGet.</span><span class="sxs-lookup"><span data-stu-id="64f42-105">**Visual Studio >=2019:** If you are using Visual Studio 2019 or later, you can add the numerics package using the NuGet Package Manager.</span></span>
<span data-ttu-id="64f42-106">Para fazer isso, selecione "gerenciar pacotes NuGet..." do item de menu "projeto" no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="64f42-106">To do so, select "Manage NuGet Packages..." from the "Project" menu item in Visual Studio.</span></span>

<span data-ttu-id="64f42-107">Na guia procurar, procure o nome do pacote "Microsoft. Quantum. Numerics"</span><span class="sxs-lookup"><span data-stu-id="64f42-107">From the Browse tab, search for the package name "Microsoft.Quantum.Numerics"</span></span>

> [!NOTE]
> <span data-ttu-id="64f42-108">Certifique-se de marcar "incluir pré-lançamento"</span><span class="sxs-lookup"><span data-stu-id="64f42-108">Make sure to tick "Include prerelease"</span></span>

<span data-ttu-id="64f42-109">Isso listará os pacotes disponíveis para download.</span><span class="sxs-lookup"><span data-stu-id="64f42-109">This will list the packages available for download.</span></span>
<span data-ttu-id="64f42-110">Passar o mouse sobre "Microsoft. Quantum. Numerics" revela uma seta apontando para baixo à direita do número de versão.</span><span class="sxs-lookup"><span data-stu-id="64f42-110">Hovering over "Microsoft.Quantum.Numerics" reveals a downward-pointing arrow to the right of the version number.</span></span>
<span data-ttu-id="64f42-111">Clique na seta para instalar o pacote numéricos.</span><span class="sxs-lookup"><span data-stu-id="64f42-111">Click on the arrow in order to install the numerics package.</span></span>

<span data-ttu-id="64f42-112">Para obter mais detalhes, consulte o [Guia de interface do usuário do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="64f42-112">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="64f42-113">Como alternativa, você pode usar o console do Gerenciador de pacotes para adicionar a biblioteca de numéricos ao seu projeto por meio da interface de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="64f42-113">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![Usar o console do Gerenciador de pacotes na linha de comando](../../media/vs2017-nuget-console-menu.png)

<span data-ttu-id="64f42-115">No console do Gerenciador de pacotes, execute o seguinte:</span><span class="sxs-lookup"><span data-stu-id="64f42-115">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="64f42-116">Para obter mais detalhes, consulte o [Guia do console do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="64f42-116">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="64f42-117">**Linha de comando ou Visual Studio Code:** Usando a linha de comando por conta própria ou de dentro Visual Studio Code, você pode usar o comando `dotnet` para adicionar a referência do pacote NuGet ao seu projeto:</span><span class="sxs-lookup"><span data-stu-id="64f42-117">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a><span data-ttu-id="64f42-118">Verificando sua instalação</span><span class="sxs-lookup"><span data-stu-id="64f42-118">Verifying your installation</span></span>

<span data-ttu-id="64f42-119">Como o restante do kit de desenvolvimento Quantum, a biblioteca de numéricos vem com exemplos que ajudam você a começar o mais rapidamente possível.</span><span class="sxs-lookup"><span data-stu-id="64f42-119">Like the rest of the Quantum Development Kit, the numerics library comes with samples that help you get started as quickly as possible.</span></span>
<span data-ttu-id="64f42-120">Para testar a instalação usando esses exemplos, clone o [repositório principal de exemplos](https://github.com/Microsoft/Quantum) e, em seguida, execute um dos exemplos.</span><span class="sxs-lookup"><span data-stu-id="64f42-120">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum) and then run one of the samples.</span></span>

<span data-ttu-id="64f42-121">Para executar o exemplo de [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) :</span><span class="sxs-lookup"><span data-stu-id="64f42-121">To run the [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
