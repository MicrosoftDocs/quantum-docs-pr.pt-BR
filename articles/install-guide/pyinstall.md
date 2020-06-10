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
# <a name="develop-with-q-and-python"></a>Desenvolver com Q # e Python

Instale o QDK para desenvolver programas de host do Python para chamar as operações de Q #.

1. Pré-requisitos

    - [Python](https://www.python.org/downloads/) 3,6 ou posterior
    - O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [SDK do .NET Core 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Instale o `qsharp` pacote, um pacote do Python que habilita a interoperabilidade entre Q # e Python.

    ```
    pip install qsharp
    ```

1. Instale o IQ #, um kernel usado pelo Jupyter e Python que fornece a funcionalidade básica para compilar e executar operações de Q #.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Se você receber um erro durante a `dotnet iqsharp install` etapa, abra uma nova janela do terminal e tente novamente.
    > Se isso ainda não funcionar, tente localizar a `dotnet-iqsharp` ferramenta instalada (no Windows `dotnet-iqsharp.exe` ) e executar:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > onde `/path/to/dotnet-iqsharp` o deve ser substituído pelo caminho absoluto para a `dotnet-iqsharp` ferramenta no sistema de arquivos.
    > Normalmente, isso estará em `.dotnet/tools` na sua pasta de perfil do usuário.
  
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

        ```
        python hello_world.py
        ```

    - Verifique a saída. Seu programa deverá gerar as seguintes linhas:

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * Você também pode usar notebooks Jupyter do Python para escrever o programa de Python clássico e chamar as operações Q # das células. O código Python é apenas um programa Python normal.

## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
