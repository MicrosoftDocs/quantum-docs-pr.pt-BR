---
title: Desenvolvimento com Q# + Python
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: e1b8a0c68b3ac0c059c6de6e478593321764ff88
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680158"
---
# <a name="develop-with-q--python"></a>Desenvolvimento com Q# + Python

Instale o QDK para desenvolver programas de host do Python para chamar as operações de Q #.

1. Pré-requisitos

    - [Python](https://www.python.org/downloads/) 3,6 ou posterior
    - O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [SDK do .NET Core 3,1 ou posterior](https://www.microsoft.com/net/download)


1. Instale o `qsharp` pacote, um pacote do Python que habilita a interoperabilidade entre Q # e Python.

    ```bash
    pip install qsharp
    ```

1. Instale o IQ #, um kernel usado pelo Jupyter e Python que fornece a funcionalidade básica para compilar e executar operações de Q #.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. Embora você possa usar o Q # com Python em qualquer IDE, é altamente recomendável usar o IDE Visual Studio Code (VS Code) para seus aplicativos do Q # + Python. Usando Visual Studio Code e a extensão de Visual Studio Code QDK, você obterá acesso à funcionalidade mais rica.

    - Instalar o [vs Code](https://code.visualstudio.com/download) (Windows, Linux e Mac)
    - Instale a [extensão QDK para vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

1. Verificar a instalação criando um aplicativo `Hello World`

    - Crie uma operação Q# mínima criando um arquivo chamado `Operation.qs` e adicionando o seguinte código a ele:

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - Crie um programa Python chamado `hello_world.py` para chamar a operação Q# `SayHello()`:

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - Execute o programa:

        ```bash
        python hello_world.py
        ```

    - Verifique a saída. Seu programa deverá gerar as seguintes linhas:

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * Você também pode usar notebooks Jupyter do Python para escrever o programa de Python clássico e chamar as operações Q # das células. O código Python é apenas um programa Python normal.

## <a name="whats-next"></a>O que vem a seguir?

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.write-program).
