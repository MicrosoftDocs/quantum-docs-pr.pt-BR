---
title: 'Desenvolver com o Q # Jupyter notebooks'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 38db14ccc5f2406043ff4baee3f562385cdf47a8
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426388"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="73fc1-102">Desenvolver com o Q # Jupyter notebooks</span><span class="sxs-lookup"><span data-stu-id="73fc1-102">Develop with Q# Jupyter notebooks</span></span>

<span data-ttu-id="73fc1-103">Instale o QDK para desenvolver operações Q # em notebooks do Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="73fc1-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="73fc1-104">Os notebooks Jupyter permitem a execução de código in-loco juntamente com instruções, observações e outros conteúdos.</span><span class="sxs-lookup"><span data-stu-id="73fc1-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="73fc1-105">Esse ambiente é ideal para escrever código Q # com explicações incorporadas ou tutoriais interativos de computação Quantum.</span><span class="sxs-lookup"><span data-stu-id="73fc1-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="73fc1-106">Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.</span><span class="sxs-lookup"><span data-stu-id="73fc1-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="73fc1-107">IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.</span><span class="sxs-lookup"><span data-stu-id="73fc1-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="73fc1-108">Em Jupyter notebooks do Q #, você só pode executar o código Q # e as operações não podem ser chamadas de programas de host externos (por exemplo, arquivos Python ou C#).</span><span class="sxs-lookup"><span data-stu-id="73fc1-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="73fc1-109">Esse ambiente não será apropriado se o seu objetivo for combinar um programa host clássico externo com o programa Quantum.</span><span class="sxs-lookup"><span data-stu-id="73fc1-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="73fc1-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="73fc1-110">Pre-requisites</span></span>

    - <span data-ttu-id="73fc1-111">[Python](https://www.python.org/downloads/) 3,6 ou posterior</span><span class="sxs-lookup"><span data-stu-id="73fc1-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="73fc1-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="73fc1-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="73fc1-113">SDK do .NET Core 3,1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="73fc1-113">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="73fc1-114">Instalar o pacote `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="73fc1-114">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="73fc1-115">Verificar a instalação criando um aplicativo `Hello World`</span><span class="sxs-lookup"><span data-stu-id="73fc1-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="73fc1-116">Execute o seguinte comando para iniciar o servidor de notebook:</span><span class="sxs-lookup"><span data-stu-id="73fc1-116">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="73fc1-117">Para abrir a cópia do bloco de anotações Jupyter e cole a URL fornecida pela linha de comando no navegador.</span><span class="sxs-lookup"><span data-stu-id="73fc1-117">To open the Jupyter notebook copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="73fc1-118">Crie um Jupyter Notebook com um kernel do Q# e adicione o seguinte código à primeira célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="73fc1-118">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="73fc1-119">Execute esta célula do notebook:</span><span class="sxs-lookup"><span data-stu-id="73fc1-119">Run this cell of the notebook:</span></span>

        ![Célula do Jupyter Notebook com código Q#](~/media/install-guide-jupyter.png)

        <span data-ttu-id="73fc1-121">Você deverá ver `SayHello` na saída da célula.</span><span class="sxs-lookup"><span data-stu-id="73fc1-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="73fc1-122">Durante a execução em Jupyter notebooks, o código Q# é compilado e o notebook gera o nome das operações encontradas.</span><span class="sxs-lookup"><span data-stu-id="73fc1-122">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="73fc1-123">Em uma nova célula, execute a operação que você acabou de criar (em um simulador) usando o `%simulate` comando:</span><span class="sxs-lookup"><span data-stu-id="73fc1-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Célula do Jupyter Notebook com a mágica %simulate](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="73fc1-125">Você deve ver a mensagem impressa na tela junto com o resultado da operação que você chamou (aqui, vemos a tupla vazia `()` porque nossa operação simplesmente retorna um `Unit` tipo).</span><span class="sxs-lookup"><span data-stu-id="73fc1-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="73fc1-126">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="73fc1-126">Next steps</span></span>

<span data-ttu-id="73fc1-127">Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="73fc1-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
