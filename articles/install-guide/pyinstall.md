---
title: 'Desenvolver com Q # e Python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 1ae208e7047cb040fb44945a59c3cc6508a09723
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630278"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="1ff8e-102">Desenvolver com Q # e Python</span><span class="sxs-lookup"><span data-stu-id="1ff8e-102">Develop with Q# and Python</span></span>

<span data-ttu-id="1ff8e-103">Instale o QDK para desenvolver programas de host do Python para chamar as operações de Q #.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="1ff8e-104">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1ff8e-104">Prerequisites</span></span>

    - <span data-ttu-id="1ff8e-105">[Python](https://www.python.org/downloads/) 3,6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1ff8e-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="1ff8e-106">O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="1ff8e-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="1ff8e-107">SDK do .NET Core 3,1</span><span class="sxs-lookup"><span data-stu-id="1ff8e-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="1ff8e-108">Instale o `qsharp` pacote, um pacote do Python que habilita a interoperabilidade entre Q # e Python.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="1ff8e-109">Instale o IQ #, um kernel usado pelo Jupyter e Python que fornece a funcionalidade básica para compilar e executar operações de Q #.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="1ff8e-110">Se você receber um erro durante a `dotnet iqsharp install` etapa, abra uma nova janela do terminal e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-110">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="1ff8e-111">Se isso ainda não funcionar, tente localizar a `dotnet-iqsharp` ferramenta instalada (no Windows `dotnet-iqsharp.exe` ) e executar:</span><span class="sxs-lookup"><span data-stu-id="1ff8e-111">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="1ff8e-112">onde `/path/to/dotnet-iqsharp` o deve ser substituído pelo caminho absoluto para a `dotnet-iqsharp` ferramenta no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-112">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="1ff8e-113">Normalmente, isso estará em `.dotnet/tools` na sua pasta de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-113">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
  
1. <span data-ttu-id="1ff8e-114">Embora você possa usar o Q # com Python em qualquer IDE, é altamente recomendável usar o IDE Visual Studio Code (VS Code) para seus aplicativos do Q # + Python.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-114">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="1ff8e-115">Usando Visual Studio Code e a extensão de Visual Studio Code QDK, você obterá acesso à funcionalidade mais rica.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-115">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="1ff8e-116">Instalar o [vs Code](https://code.visualstudio.com/download) (Windows, Linux e Mac)</span><span class="sxs-lookup"><span data-stu-id="1ff8e-116">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="1ff8e-117">Instale a [extensão QDK para vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="1ff8e-117">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="1ff8e-118">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="1ff8e-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="1ff8e-119">Crie uma operação Q# mínima criando um arquivo chamado `Operation.qs` e adicionando o seguinte código a ele:</span><span class="sxs-lookup"><span data-stu-id="1ff8e-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="1ff8e-120">Crie um programa Python chamado `hello_world.py` para chamar a operação Q# `SayHello()`:</span><span class="sxs-lookup"><span data-stu-id="1ff8e-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="1ff8e-121">Execute o programa:</span><span class="sxs-lookup"><span data-stu-id="1ff8e-121">Run the program:</span></span>

        ```
        python hello_world.py
        ```

    - <span data-ttu-id="1ff8e-122">Verifique a saída.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-122">Verify the output.</span></span> <span data-ttu-id="1ff8e-123">Seu programa deverá gerar as seguintes linhas:</span><span class="sxs-lookup"><span data-stu-id="1ff8e-123">Your program should output the following lines:</span></span>

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * <span data-ttu-id="1ff8e-124">Você também pode usar notebooks Jupyter do Python para escrever o programa de Python clássico e chamar as operações Q # das células.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-124">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="1ff8e-125">O código Python é apenas um programa Python normal.</span><span class="sxs-lookup"><span data-stu-id="1ff8e-125">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1ff8e-126">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="1ff8e-126">Next steps</span></span>

<span data-ttu-id="1ff8e-127">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="1ff8e-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
