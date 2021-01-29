---
title: Como desenvolver com o Q# e o Binder
description: Saiba como criar um aplicativo Q# usando o Binder.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: quickstart
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f7e9b1ae67d6275ec7ba39ea411842dc537536c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856722"
---
# <a name="develop-with-no-locq-and-binder"></a><span data-ttu-id="3cef3-103">Como desenvolver com o Q# e o Binder</span><span class="sxs-lookup"><span data-stu-id="3cef3-103">Develop with Q# and Binder</span></span>

<span data-ttu-id="3cef3-104">Será possível usar o Binder para executar e compartilhar Jupyter Notebooks online.</span><span class="sxs-lookup"><span data-stu-id="3cef3-104">You can use Binder to run and share your Jupyter Notebooks online.</span></span>

## <a name="use-binder-with-the-microsoft-qdk-samples"></a><span data-ttu-id="3cef3-105">Usar o Binder com exemplos do QDK da Microsoft</span><span class="sxs-lookup"><span data-stu-id="3cef3-105">Use Binder with the Microsoft QDK samples</span></span>

<span data-ttu-id="3cef3-106">Para configurar o Binder de maneira automática com o objetivo de usar os exemplos do QDK da Microsoft:</span><span class="sxs-lookup"><span data-stu-id="3cef3-106">To configure Binder automatically to use the Microsoft QDK samples:</span></span>

1. <span data-ttu-id="3cef3-107">Abra um navegador e execute https://aka.ms/try-qsharp.</span><span class="sxs-lookup"><span data-stu-id="3cef3-107">Open a browser and run https://aka.ms/try-qsharp.</span></span>
1. <span data-ttu-id="3cef3-108">Na página de aterrissagem **Exemplos do Kit de Desenvolvimento Quantum**, clique em **Q# Notebook** para saber como usar o IQ# a fim de gravar seus notebooks de aplicativos quânticos.</span><span class="sxs-lookup"><span data-stu-id="3cef3-108">On the **Quantum Development Kit Samples** landing page, click **Q# notebook** to learn how to use IQ# to write your own quantum application notebooks.</span></span>

![Página de aterrissagem do QDK](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a><span data-ttu-id="3cef3-110">Use o Binder com seus notebooks e repositórios</span><span class="sxs-lookup"><span data-stu-id="3cef3-110">Use Binder with your own notebooks and repository</span></span>

<span data-ttu-id="3cef3-111">Caso já tenha os notebooks em um repositório GitHub, será possível configurar o Binder para trabalhar com seu repositório:</span><span class="sxs-lookup"><span data-stu-id="3cef3-111">If you already have notebooks in a GitHub repository, you can configure Binder to work with your repo:</span></span>

1. <span data-ttu-id="3cef3-112">Verifique se há um arquivo chamado *Dockerfile* na raiz do repositório.</span><span class="sxs-lookup"><span data-stu-id="3cef3-112">Ensure that there is a file named *Dockerfile* in the root of your repository.</span></span> <span data-ttu-id="3cef3-113">O arquivo deverá conter pelo menos as seguintes linhas:</span><span class="sxs-lookup"><span data-stu-id="3cef3-113">The file must contain at least the following lines:</span></span>

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > <span data-ttu-id="3cef3-114">Será possível verificar a versão mais atual do IQ# em [Notas sobre a versão](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="3cef3-114">You can verify the most current version of IQ# in the [Release Notes](xref:microsoft.quantum.relnotes).</span></span>

    <span data-ttu-id="3cef3-115">Para obter mais informações sobre como criar um Dockerfile, confira a [Referência do Dockerfile](https://docs.docker.com/engine/reference/builder/).</span><span class="sxs-lookup"><span data-stu-id="3cef3-115">For more information about creating a Dockerfile, see the [Dockerfile reference](https://docs.docker.com/engine/reference/builder/).</span></span>

2. <span data-ttu-id="3cef3-116">Abra um navegador para executar [mybinder.org](https://mybinder.org).</span><span class="sxs-lookup"><span data-stu-id="3cef3-116">Open a browser to [mybinder.org](https://mybinder.org).</span></span>
3. <span data-ttu-id="3cef3-117">Insira o nome do repositório conforme a **URL do GitHub** (por exemplo *MyName/MyRepo*) e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="3cef3-117">Enter your repository name as the **GitHub URL** (for example *MyName/MyRepo*), and click **launch**.</span></span>

![Formulário MyBinder](~/media/mybinder.png)
    
## <a name="next-steps"></a><span data-ttu-id="3cef3-119">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="3cef3-119">Next steps</span></span>

<span data-ttu-id="3cef3-120">Agora que você já configurou o ambiente do Binder, será possível gravar e executar [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="3cef3-120">Now that you have set up your Binder environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
