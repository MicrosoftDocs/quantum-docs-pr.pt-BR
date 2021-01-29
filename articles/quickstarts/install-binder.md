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
# <a name="develop-with-no-locq-and-binder"></a>Como desenvolver com o Q# e o Binder

Será possível usar o Binder para executar e compartilhar Jupyter Notebooks online.

## <a name="use-binder-with-the-microsoft-qdk-samples"></a>Usar o Binder com exemplos do QDK da Microsoft

Para configurar o Binder de maneira automática com o objetivo de usar os exemplos do QDK da Microsoft:

1. Abra um navegador e execute https://aka.ms/try-qsharp.
1. Na página de aterrissagem **Exemplos do Kit de Desenvolvimento Quantum**, clique em **Q# Notebook** para saber como usar o IQ# a fim de gravar seus notebooks de aplicativos quânticos.

![Página de aterrissagem do QDK](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a>Use o Binder com seus notebooks e repositórios

Caso já tenha os notebooks em um repositório GitHub, será possível configurar o Binder para trabalhar com seu repositório:

1. Verifique se há um arquivo chamado *Dockerfile* na raiz do repositório. O arquivo deverá conter pelo menos as seguintes linhas:

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > Será possível verificar a versão mais atual do IQ# em [Notas sobre a versão](xref:microsoft.quantum.relnotes).

    Para obter mais informações sobre como criar um Dockerfile, confira a [Referência do Dockerfile](https://docs.docker.com/engine/reference/builder/).

2. Abra um navegador para executar [mybinder.org](https://mybinder.org).
3. Insira o nome do repositório conforme a **URL do GitHub** (por exemplo *MyName/MyRepo*) e clique em **Iniciar**.

![Formulário MyBinder](~/media/mybinder.png)
    
## <a name="next-steps"></a>Próximas etapas

Agora que você já configurou o ambiente do Binder, será possível gravar e executar [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
