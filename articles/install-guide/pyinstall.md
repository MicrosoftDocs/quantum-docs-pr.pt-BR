---
title: 'Desenvolver com Q # e Python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 35499daae0cd0ae329e39b43b0d8dd5a00183871
ms.sourcegitcommit: 328f45a0b64cb6b325fa9d3b3ddb74a6a7a97ee9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83660737"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="ce709-102">Desenvolver com Q # e Python</span><span class="sxs-lookup"><span data-stu-id="ce709-102">Develop with Q# and Python</span></span>

<span data-ttu-id="ce709-103">Instale o QDK para desenvolver programas de host do Python para chamar as operações de Q #.</span><span class="sxs-lookup"><span data-stu-id="ce709-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="ce709-104">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ce709-104">Pre-requisites</span></span>

    - <span data-ttu-id="ce709-105">[Python](https://www.python.org/downloads/) 3,6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ce709-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="ce709-106">O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="ce709-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="ce709-107">SDK do .NET Core 3,1</span><span class="sxs-lookup"><span data-stu-id="ce709-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="ce709-108">Instale o `qsharp` pacote, um pacote do Python que habilita a interoperabilidade entre Q # e Python.</span><span class="sxs-lookup"><span data-stu-id="ce709-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="ce709-109">Instale o IQ #, um kernel usado pelo Jupyter e Python que fornece a funcionalidade básica para compilar e executar operações de Q #.</span><span class="sxs-lookup"><span data-stu-id="ce709-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. <span data-ttu-id="ce709-110">Embora você possa usar o Q # com Python em qualquer IDE, é altamente recomendável usar o IDE Visual Studio Code (VS Code) para seus aplicativos do Q # + Python.</span><span class="sxs-lookup"><span data-stu-id="ce709-110">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="ce709-111">Usando Visual Studio Code e a extensão de Visual Studio Code QDK, você obterá acesso à funcionalidade mais rica.</span><span class="sxs-lookup"><span data-stu-id="ce709-111">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="ce709-112">Instalar o [vs Code](https://code.visualstudio.com/download) (Windows, Linux e Mac)</span><span class="sxs-lookup"><span data-stu-id="ce709-112">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="ce709-113">Instale a [extensão QDK para vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="ce709-113">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="ce709-114">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="ce709-114">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ce709-115">Crie uma operação Q# mínima criando um arquivo chamado `Operation.qs` e adicionando o seguinte código a ele:</span><span class="sxs-lookup"><span data-stu-id="ce709-115">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="ce709-116">Crie um programa Python chamado `hello_world.py` para chamar a operação Q# `SayHello()`:</span><span class="sxs-lookup"><span data-stu-id="ce709-116">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="ce709-117">Execute o programa:</span><span class="sxs-lookup"><span data-stu-id="ce709-117">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="ce709-118">Verifique a saída.</span><span class="sxs-lookup"><span data-stu-id="ce709-118">Verify the output.</span></span> <span data-ttu-id="ce709-119">Seu programa deverá gerar as seguintes linhas:</span><span class="sxs-lookup"><span data-stu-id="ce709-119">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * <span data-ttu-id="ce709-120">Você também pode usar notebooks Jupyter do Python para escrever o programa de Python clássico e chamar as operações Q # das células.</span><span class="sxs-lookup"><span data-stu-id="ce709-120">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="ce709-121">O código Python é apenas um programa Python normal.</span><span class="sxs-lookup"><span data-stu-id="ce709-121">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ce709-122">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="ce709-122">Next steps</span></span>

<span data-ttu-id="ce709-123">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="ce709-123">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
