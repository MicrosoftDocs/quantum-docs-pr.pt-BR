---
title: Desenvolver com o Q# e o Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 6513acd5b9cdce15ce61ed2c0454f46e6a6d9bd0
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274015"
---
# <a name="develop-with-q-and-python"></a>Desenvolver com o Q# e o Python

Instale o QDK para desenvolver programas de host do Python para chamar operações Q#.

1. Pré-requisitos

    - [Python](https://www.python.org/downloads/) 3.6 ou posterior
    - O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [SDK do .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Instale o pacote `qsharp`, um pacote do Python que permite a interoperabilidade entre o Q# e o Python.

    ```
    pip install qsharp
    ```

1. Instale o IQ#, um kernel usado pelo Jupyter e pelo Python que fornece a funcionalidade básica para compilar e executar operações Q#.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Se você receber um erro durante a etapa `dotnet iqsharp install`, abra uma nova janela de terminal e tente novamente.
    > Se isso ainda não funcionar, tente localizar a ferramenta `dotnet-iqsharp` instalada (no Windows, `dotnet-iqsharp.exe`) e executar:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > em que `/path/to/dotnet-iqsharp` deverá ser substituída pelo caminho absoluto para a ferramenta `dotnet-iqsharp` no sistema de arquivos.
    > Normalmente, isso estará em `.dotnet/tools` na pasta de perfil do usuário.
  
1. Embora você possa usar o Q# com o Python em qualquer IDE, recomendamos expressamente usar o IDE do VS Code (Visual Studio Code) para seus aplicativos Q# + Python. Ao usar o Visual Studio Code e a extensão do QDK para Visual Studio Code, você terá acesso a uma funcionalidade mais sofisticada.

    - Instalar o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac)
    - Instale a [extensão do QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

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
> * Use também Jupyter notebooks do Python para escrever o programa Python clássico e chamar as operações Q# por meio das células. O código Python é apenas um programa Python normal.

## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
