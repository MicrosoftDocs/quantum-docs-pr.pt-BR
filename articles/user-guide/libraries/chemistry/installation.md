---
title: 'Instalação e validação da biblioteca do Microsoft Q # química'
description: Saiba como instalar a biblioteca química do Microsoft Quantum e usá-la com a plataforma química computacional NWChem.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: 48bf7bc980e238e622053f5c2bdd09604c572596
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274328"
---
# <a name="chemistry-library-installation-and-validation"></a><span data-ttu-id="21ee7-103">Instalação e validação da biblioteca de química</span><span class="sxs-lookup"><span data-stu-id="21ee7-103">Chemistry Library Installation and Validation</span></span>

<span data-ttu-id="21ee7-104">O kit de desenvolvimento Quantum fornece suporte para aplicativos químicas da Quantum por meio do [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) pacote NuGet.</span><span class="sxs-lookup"><span data-stu-id="21ee7-104">The Quantum Development Kit provides support for quantum chemistry applications through the [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) NuGet package.</span></span>
<span data-ttu-id="21ee7-105">Assim como acontece com outros pacotes NuGet, é simples adicionar a biblioteca química ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="21ee7-105">As with other NuGet packages, it's straightforward to add the chemistry library to your project.</span></span>

<span data-ttu-id="21ee7-106">**Visual Studio 2019:** Se você estiver usando o Visual Studio 2019, poderá adicionar os pacotes de química do Quantum usando o Gerenciador de pacotes NuGet.</span><span class="sxs-lookup"><span data-stu-id="21ee7-106">**Visual Studio 2019:** If you are using Visual Studio 2019, you can add the quantum chemistry packages by using the NuGet Package Manager.</span></span>
<span data-ttu-id="21ee7-107">Para abrir o Gerenciador de pacotes, clique com o botão direito do mouse no projeto ao qual você deseja adicionar a biblioteca de química e selecione "gerenciar pacotes NuGet...", como na captura de tela abaixo.</span><span class="sxs-lookup"><span data-stu-id="21ee7-107">To open the Package Manager, right-click on the project you'd like to add the chemistry library to and select "Manage NuGet Packages...," as in the screenshot below.</span></span>

![Usando o Gerenciador de pacotes NuGet no Visual Studio 2019](~/media/vs2017-nuget-manage-packages.png)

<span data-ttu-id="21ee7-109">Na guia procurar, procure o nome do pacote "Microsoft. Quantum. química".</span><span class="sxs-lookup"><span data-stu-id="21ee7-109">From the Browse tab, search for the package name "Microsoft.Quantum.Chemistry."</span></span>

> [!NOTE]
> <span data-ttu-id="21ee7-110">Certifique-se de marcar "incluir pré-lançamento".</span><span class="sxs-lookup"><span data-stu-id="21ee7-110">Make sure to tick "Include prerelease."</span></span>

![Caixa de seleção incluir pré-liberação](~/media/vs2017-nuget-package-search.png)

<span data-ttu-id="21ee7-112">Isso listará os pacotes disponíveis para download.</span><span class="sxs-lookup"><span data-stu-id="21ee7-112">This will list the packages available for download.</span></span>
<span data-ttu-id="21ee7-113">Clique no "Microsoft. Quantum. química no painel esquerdo, selecione a versão de pré-lançamento mais recente no painel direito e clique em" instalar ":</span><span class="sxs-lookup"><span data-stu-id="21ee7-113">Click on the "Microsoft.Quantum.Chemistry on the left-hand pane, select the latest pre-release version on the right-hand pane, and click "Install":</span></span>

![Instalar o pacote Microsoft. Quantum. química mais recente](~/media/vs2017-nuget-select-chem.png)

<span data-ttu-id="21ee7-115">Para obter mais detalhes, consulte o [Guia de interface do usuário do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="21ee7-115">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="21ee7-116">Como alternativa, você pode usar o console do Gerenciador de pacotes para adicionar a biblioteca química do Quantum ao seu projeto com uma interface de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="21ee7-116">Alternatively, you can use the Package Manager Console to add the quantum chemistry library to your project with a command line interface.</span></span>

![Usar o console do Gerenciador de pacotes na linha de comando](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="21ee7-118">No console do Gerenciador de pacotes, execute o seguinte:</span><span class="sxs-lookup"><span data-stu-id="21ee7-118">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Chemistry
```

<span data-ttu-id="21ee7-119">Para obter mais detalhes, consulte o [Guia do console do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="21ee7-119">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="21ee7-120">**Linha de comando ou Visual Studio Code:** Usando a linha de comando por conta própria ou de dentro Visual Studio Code, você pode usar o `dotnet` comando para adicionar a referência do pacote NuGet ao seu projeto:</span><span class="sxs-lookup"><span data-stu-id="21ee7-120">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a><span data-ttu-id="21ee7-121">Verificando sua instalação</span><span class="sxs-lookup"><span data-stu-id="21ee7-121">Verifying Your Installation</span></span> 

<span data-ttu-id="21ee7-122">Assim como o restante do kit de desenvolvimento Quantum, a biblioteca química do Quantum vem com uma série de amostras totalmente documentadas para ajudá-lo a entrar em funcionamento rapidamente.</span><span class="sxs-lookup"><span data-stu-id="21ee7-122">Like the rest of the Quantum Development Kit, the quantum chemistry library comes with a number of fully documented samples to help you get up and running quickly.</span></span>
<span data-ttu-id="21ee7-123">Para testar a instalação usando esses exemplos, clone o [repositório principal de exemplos](https://github.com/Microsoft/Quantum)e, em seguida, execute um dos exemplos.</span><span class="sxs-lookup"><span data-stu-id="21ee7-123">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum), then run one of the samples.</span></span>  <span data-ttu-id="21ee7-124">Por exemplo, para executar o [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) exemplo:</span><span class="sxs-lookup"><span data-stu-id="21ee7-124">For example, to run the [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/chemistry/MolecularHydrogen
dotnet run
```

<span data-ttu-id="21ee7-125">Para verificar a instalação da biblioteca química do Quantum usando Microsoft Visual Studio depois de clonar o repositório:</span><span class="sxs-lookup"><span data-stu-id="21ee7-125">To verify the installation of the quantum chemistry library using Microsoft Visual Studio after cloning the repository:</span></span>
    1. <span data-ttu-id="21ee7-126">Abra a solução ChemistrySamples. sln na pasta química.</span><span class="sxs-lookup"><span data-stu-id="21ee7-126">Open the ChemistrySamples.sln solution in the Chemistry folder.</span></span>  
    2. <span data-ttu-id="21ee7-127">Selecione amostras/1.</span><span class="sxs-lookup"><span data-stu-id="21ee7-127">Select Samples/1.</span></span> <span data-ttu-id="21ee7-128">Moléculas/MolecularHydrogen simples como o projeto de inicialização.</span><span class="sxs-lookup"><span data-stu-id="21ee7-128">Simple Molecules/MolecularHydrogen as the StartUp project.</span></span>
    3. <span data-ttu-id="21ee7-129">Pressione F5 para executar a demonstração de estimativa da fase Quantum do molecular Hydrogen.</span><span class="sxs-lookup"><span data-stu-id="21ee7-129">Press F5 to run the molecular Hydrogen quantum phase estimation demo.</span></span>

<span data-ttu-id="21ee7-130">Consulte [obtendo estimativas de nível de energia](xref:microsoft.quantum.chemistry.examples.energyestimate) para obter mais informações sobre como estimar os valores dos níveis de energia.</span><span class="sxs-lookup"><span data-stu-id="21ee7-130">See [Obtaining energy level estimates](xref:microsoft.quantum.chemistry.examples.energyestimate) for more information on estimating the values of energy levels.</span></span>   


## <a name="using-the-quantum-development-kit-with-nwchem"></a><span data-ttu-id="21ee7-131">Usando o kit de desenvolvimento Quantum com NWChem</span><span class="sxs-lookup"><span data-stu-id="21ee7-131">Using the Quantum Development Kit with NWChem</span></span> ##

<span data-ttu-id="21ee7-132">O exemplo MolecularHydrogen usa os dados de entrada do molecular que são configurados manualmente.</span><span class="sxs-lookup"><span data-stu-id="21ee7-132">The MolecularHydrogen sample uses molecular input data that is manually configured.</span></span>  <span data-ttu-id="21ee7-133">Embora isso seja bom para exemplos pequenos, o quantum química em escala exige Hamiltonians com milhões ou bilhões de termos.</span><span class="sxs-lookup"><span data-stu-id="21ee7-133">While this is fine for small examples, quantum chemistry at scale require Hamiltonians with millions or billions of terms.</span></span> <span data-ttu-id="21ee7-134">Esses Hamiltonians, gerados por pacotes de química computacional escalonáveis, são muito grandes para serem importados manualmente.</span><span class="sxs-lookup"><span data-stu-id="21ee7-134">Such Hamiltonians, generated by scalable computational chemistry packages are too large to import by hand.</span></span> 

<span data-ttu-id="21ee7-135">A biblioteca química do Quantum para o kit de desenvolvimento Quantum foi projetada para funcionar bem com pacotes químicas computacionais, mais notavelmente a plataforma [**NWChem**](http://www.nwchem-sw.org/) computacional química desenvolvida pelo EMSL (ambiente Molecular Sciences Environment) no laboratório nacional do noroeste do Pacífico.</span><span class="sxs-lookup"><span data-stu-id="21ee7-135">The quantum chemistry library for the Quantum Development Kit is designed to work well with computational chemistry packages, most notably the [**NWChem**](http://www.nwchem-sw.org/) computational chemistry platform developed by the Environmental Molecular Sciences Laboratory (EMSL) at Pacific Northwest National Laboratory.</span></span>
<span data-ttu-id="21ee7-136">Em particular, o `Microsoft.Quantum.Chemistry` pacote fornece ferramentas para carregar instâncias de problemas de simulação de química do Quantum representados no [esquema Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), também com suporte para exportação por versões recentes do NWChem.</span><span class="sxs-lookup"><span data-stu-id="21ee7-136">In particular, the `Microsoft.Quantum.Chemistry` package provides tools for loading instances of quantum chemistry simulation problems represented in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), also supported for export by recent versions of NWChem.</span></span>

<span data-ttu-id="21ee7-137">Para começar a usar o NWChem junto com o kit de desenvolvimento Quantum, sugerimos um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="21ee7-137">To get up and running using NWChem together with the Quantum Development Kit, we suggest one of the following methods:</span></span>
- <span data-ttu-id="21ee7-138">Comece a usar os arquivos Broombridge existentes fornecidos com os exemplos em [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span><span class="sxs-lookup"><span data-stu-id="21ee7-138">Get started using existing Broombridge files provided with the samples at [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span></span>
- <span data-ttu-id="21ee7-139">Use o [Construtor de setas EMSL para o Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) que é um front-end baseado na Web para NWChem, para gerar novos arquivos de entrada molecular Broombridge.</span><span class="sxs-lookup"><span data-stu-id="21ee7-139">Use the [EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) which is a web-based frontend to NWChem, to generate new Broombridge-formated molecular input files.</span></span>  
- <span data-ttu-id="21ee7-140">Use a [imagem do Docker](https://hub.docker.com/r/nwchemorg/nwchem-qc/) fornecida pelo PNNL para executar NWChem ou</span><span class="sxs-lookup"><span data-stu-id="21ee7-140">Use the [Docker image](https://hub.docker.com/r/nwchemorg/nwchem-qc/) provided by PNNL to run NWChem, or</span></span>
- <span data-ttu-id="21ee7-141">[Compile o NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) para sua plataforma.</span><span class="sxs-lookup"><span data-stu-id="21ee7-141">[Compile NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) for your platform.</span></span>

<span data-ttu-id="21ee7-142">Consulte de [ponta a ponta com NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) para obter mais informações sobre como trabalhar com o NWChem para modelos químicos para analisar com a biblioteca do Quantum Developer Kit química.</span><span class="sxs-lookup"><span data-stu-id="21ee7-142">See [End-to-end with NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) for more information on how to work with NWChem to chemical models to analyze with the Quantum Developmen Kit chemistry library.</span></span>

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a><span data-ttu-id="21ee7-143">Introdução ao uso de arquivos Broombridge fornecidos com os exemplos</span><span class="sxs-lookup"><span data-stu-id="21ee7-143">Getting started using Broombridge files provided with the samples</span></span>

<span data-ttu-id="21ee7-144">A pasta [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) no repositório de exemplos do kit de desenvolvimento do Quantum contém arquivos de dados molécula com formato Broombridge.</span><span class="sxs-lookup"><span data-stu-id="21ee7-144">The [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) folder in the Quantum Development Kit Samples repository contains Broombridge-formated molecule data files.</span></span>  

<span data-ttu-id="21ee7-145">Como um exemplo simples, use o exemplo de biblioteca de química, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) para carregar o Hamiltonian de um dos arquivos Broombridge e executar estimativas de portão de algorigthms de simulação de Quantum:</span><span class="sxs-lookup"><span data-stu-id="21ee7-145">As a simple example, use the chemistry library sample, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) to load the Hamiltonian from one of Broombridge files and perform gate estimates of quantum simulation algorigthms:</span></span>

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

<span data-ttu-id="21ee7-146">Consulte [carregando um Hamiltonian do arquivo](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) para obter mais informações sobre como inserir moléculas representado pelo esquema Broombridge.</span><span class="sxs-lookup"><span data-stu-id="21ee7-146">See [Loading a Hamiltonian from file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) for more information on how to input molecules represented by the Broombridge schema.</span></span>  

<span data-ttu-id="21ee7-147">Confira [obtendo contagens de recursos](xref:microsoft.quantum.chemistry.examples.resourcecounts) para obter mais informações sobre a estimativa de recursos.</span><span class="sxs-lookup"><span data-stu-id="21ee7-147">See [Obtaining resource counts](xref:microsoft.quantum.chemistry.examples.resourcecounts) for more information on resource estimation.</span></span>  

### <a name="getting-started-using-the-emsl-arrows-builder"></a><span data-ttu-id="21ee7-148">Introdução ao uso do construtor de setas EMSL</span><span class="sxs-lookup"><span data-stu-id="21ee7-148">Getting started using the EMSL Arrows Builder</span></span>

<span data-ttu-id="21ee7-149">EMSL Arrows é uma ferramenta que usa bancos de dados computacionais NWChem e químicas para gerar molécula.</span><span class="sxs-lookup"><span data-stu-id="21ee7-149">EMSL Arrows is a tool that uses NWChem and chemical computational databases to generate molecule data.</span></span>  <span data-ttu-id="21ee7-150">[O EMSL Arrows Builder para o Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) permite que você insira seu modelo usando vários construtores de modelo molecular e gere o arquivo de configuração do Broombridge para ser usado pelo kit de desenvolvimento Quantum.</span><span class="sxs-lookup"><span data-stu-id="21ee7-150">[EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) allows you to enter your model using multiple molecular model builders and generate the Broombridge datafile to be used by the Quantum Development Kit.</span></span>  

<span data-ttu-id="21ee7-151">Na página EMSL, clique na guia [' instuctions '] e siga as instruções [' exemplos simples '] para gerar arquivos Broombridge.</span><span class="sxs-lookup"><span data-stu-id="21ee7-151">From the EMSL page, click on the ['Instuctions'] tab, and follow the ['Simple Examples'] instructions to generate Broombridge files.</span></span>  <span data-ttu-id="21ee7-152">Em seguida, tente executar [' GetGateCount '] para ver as estimativas de recursos Quantum para esses moléculas.</span><span class="sxs-lookup"><span data-stu-id="21ee7-152">Then try running the ['GetGateCount'] to see the quantum resource estimates for these molecules.</span></span>

### <a name="installing-nwchem-from-source"></a><span data-ttu-id="21ee7-153">Instalando o NWChem da origem</span><span class="sxs-lookup"><span data-stu-id="21ee7-153">Installing NWChem from Source</span></span>

<span data-ttu-id="21ee7-154">Instruções completas sobre como instalar o NWChem da origem [são fornecidas pelo PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span><span class="sxs-lookup"><span data-stu-id="21ee7-154">Full instructions on how to install NWChem from source [are provided by PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span></span>

> [!TIP]
> <span data-ttu-id="21ee7-155">Se você quiser usar o NWChem do Windows 10, o subsistema do Windows para Linux é uma ótima opção.</span><span class="sxs-lookup"><span data-stu-id="21ee7-155">If you wish to use NWChem from Windows 10, the Windows Subsystem for Linux is a great option.</span></span>
> <span data-ttu-id="21ee7-156">Depois de ter instalado o [Ubuntu 18, 4 LTS para Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab), execute `ubuntu18.04` do seu terminal favorito e siga as instruções acima para instalar o NWChem da origem.</span><span class="sxs-lookup"><span data-stu-id="21ee7-156">Once you have installed [Ubuntu 18.04 LTS for Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab), run `ubuntu18.04` from your favorite terminal and follow the instructions above to install NWChem from source.</span></span>

<span data-ttu-id="21ee7-157">Depois de compilar o NWChem da origem, você pode executar o `yaml_driver` script fornecido com NWChem para produzir rapidamente instâncias de Broombridge de baralhos de entrada NWChem:</span><span class="sxs-lookup"><span data-stu-id="21ee7-157">Once you have compiled NWChem from source, you can run the `yaml_driver` script provided with NWChem to quickly produce Broombridge instances from NWChem input decks:</span></span>

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

<span data-ttu-id="21ee7-158">Esse comando criará um novo `input.yaml` arquivo no formato Broombridge dentro do diretório atual.</span><span class="sxs-lookup"><span data-stu-id="21ee7-158">This command will create a new `input.yaml` file in the Broombridge format within your current directory.</span></span>

### <a name="using-nwchem-with-docker"></a><span data-ttu-id="21ee7-159">Usando o NWChem com o Docker</span><span class="sxs-lookup"><span data-stu-id="21ee7-159">Using NWChem with Docker</span></span>

<span data-ttu-id="21ee7-160">As imagens predefinidas para usar o NWChem estão disponíveis para a plataforma cruzada por meio do [Hub do Docker](https://hub.docker.com).</span><span class="sxs-lookup"><span data-stu-id="21ee7-160">Pre-built images for using NWChem are available cross-platform via [Docker Hub](https://hub.docker.com).</span></span>
<span data-ttu-id="21ee7-161">Para começar, siga as instruções de instalação do Docker para sua plataforma:</span><span class="sxs-lookup"><span data-stu-id="21ee7-161">To get started, follow the Docker installation instructions for your platform:</span></span>

- [<span data-ttu-id="21ee7-162">Instalar o Docker para Ubuntu</span><span class="sxs-lookup"><span data-stu-id="21ee7-162">Install Docker for Ubuntu</span></span>](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [<span data-ttu-id="21ee7-163">Instalar o Docker para macOS</span><span class="sxs-lookup"><span data-stu-id="21ee7-163">Install Docker for macOS</span></span>](https://docs.docker.com/docker-for-mac/install/)
- [<span data-ttu-id="21ee7-164">Instalar o Docker for Windows 10</span><span class="sxs-lookup"><span data-stu-id="21ee7-164">Install Docker for Windows 10</span></span>](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> <span data-ttu-id="21ee7-165">Se estiver usando Docker for Windows, você precisará compartilhar a unidade que contém seu diretório temporário (normalmente, essa é a `C:\` unidade) com o daemon do Docker.</span><span class="sxs-lookup"><span data-stu-id="21ee7-165">If you are using Docker for Windows, you will need to share the drive containing your temporary directory (usually this is the `C:\` drive) with the Docker daemon.</span></span> <span data-ttu-id="21ee7-166">Consulte a [documentação do Docker](https://docs.docker.com/docker-for-windows/#shared-drives) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="21ee7-166">See the [Docker documentation](https://docs.docker.com/docker-for-windows/#shared-drives) for more details.</span></span>

<span data-ttu-id="21ee7-167">Depois de instalar o Docker, você pode usar o módulo do PowerShell fornecido com os exemplos do kit de desenvolvimento do Quantum para executar a imagem ou pode executar a imagem manualmente.</span><span class="sxs-lookup"><span data-stu-id="21ee7-167">Once you have Docker installed, you can either use the PowerShell module provided with the Quantum Development Kit samples to run the image, or you can run the image manually.</span></span>
<span data-ttu-id="21ee7-168">Nós detalhamos o uso do PowerShell aqui; Se você quiser usar a imagem do Docker manualmente, consulte a [documentação fornecida com a imagem](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span><span class="sxs-lookup"><span data-stu-id="21ee7-168">We detail using PowerShell here; if you would like to use the Docker image manually, please see the [documentation provided with the image](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span></span>

#### <a name="running-nwchem-through-powershell-core"></a><span data-ttu-id="21ee7-169">Executando o NWChem por meio do PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="21ee7-169">Running NWChem through PowerShell Core</span></span>

<span data-ttu-id="21ee7-170">Para usar a imagem do Docker NWChem com o kit de desenvolvimento Quantum, fornecemos um pequeno módulo do PowerShell que lida com a movimentação de arquivos para dentro e fora do NWChem para você.</span><span class="sxs-lookup"><span data-stu-id="21ee7-170">To use the NWChem Docker image with the Quantum Development Kit, we provide a small PowerShell module that handles moving files in and out of NWChem for you.</span></span>
<span data-ttu-id="21ee7-171">Se você ainda não tiver o PowerShell Core instalado, poderá baixá-lo entre plataformas do [repositório do PowerShell no GitHub](https://github.com/PowerShell/PowerShell#get-powershell).</span><span class="sxs-lookup"><span data-stu-id="21ee7-171">If you don't already have PowerShell Core installed, you can download it cross-platform from the [PowerShell repository on GitHub](https://github.com/PowerShell/PowerShell#get-powershell).</span></span>

> [!NOTE]
> <span data-ttu-id="21ee7-172">O PowerShell Core também é usado para alguns exemplos para demonstrar a interoperabilidade com fluxos de trabalho de ciência de dados e análise de negócios.</span><span class="sxs-lookup"><span data-stu-id="21ee7-172">PowerShell Core is also used for some samples to demonstrate interoperability with data science and business analytics workflows.</span></span>

<span data-ttu-id="21ee7-173">Depois de instalar o PowerShell Core, importe `InvokeNWChem.psm1` para tornar os comandos do NWChem disponíveis na sessão atual:</span><span class="sxs-lookup"><span data-stu-id="21ee7-173">Once you have PowerShell Core installed, import `InvokeNWChem.psm1` to make NWChem commands available in your current session:</span></span>

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

<span data-ttu-id="21ee7-174">Isso tornará o `Convert-NWChemToBroombridge` comando disponível em sua sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21ee7-174">This will make the `Convert-NWChemToBroombridge` command available in your current PowerShell session.</span></span>
<span data-ttu-id="21ee7-175">Para baixar todas as imagens necessárias do Docker e usá-las para executar os baralhos de entrada do NWChem e capturar a saída para Broombridge, execute o seguinte:</span><span class="sxs-lookup"><span data-stu-id="21ee7-175">To download any needed images from Docker and use them to run NWChem input decks and capture output to Broombridge, run the following:</span></span>

```powershell
Convert-NWChemToBroombridge ./input.nw
```

<span data-ttu-id="21ee7-176">Isso criará um arquivo Broombridge executando NWChem em `input.nw` .</span><span class="sxs-lookup"><span data-stu-id="21ee7-176">This will create a Broombridge file by running NWChem on `input.nw`.</span></span>
<span data-ttu-id="21ee7-177">Por padrão, a saída Broombridge terá o mesmo nome e caminho que o baralho de entrada, com a `.nw` extensão substituída por `.yaml` .</span><span class="sxs-lookup"><span data-stu-id="21ee7-177">By default, the Broombridge output will have the same name and path as the input deck, with the `.nw` extension replaced by `.yaml`.</span></span>
<span data-ttu-id="21ee7-178">Isso pode ser substituído usando o `-DestinationPath` parâmetro para `Convert-NWChemToBroombridge` .</span><span class="sxs-lookup"><span data-stu-id="21ee7-178">This can be overridden by using the `-DestinationPath` parameter to `Convert-NWChemToBroombridge`.</span></span>
<span data-ttu-id="21ee7-179">Mais informações podem ser obtidas usando a funcionalidade interna de ajuda do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="21ee7-179">More information can be obtained by using PowerShell's built-in help functionality:</span></span>

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```
