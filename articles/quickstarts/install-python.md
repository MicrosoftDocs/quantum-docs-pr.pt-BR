---
title: Desenvolver com o Q# e o Python
description: Saiba como criar um aplicativo Q# usando o Python.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.python
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1ec40b6f1b7a8d9144860e3b8cfd554eb51bae81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844264"
---
# <a name="develop-with-no-locq-and-python"></a>Desenvolver com o Q# e o Python

Instale o QDK para desenvolver programas de host do Python para chamar operações Q#.

## <a name="install-the-qsharp-python-package"></a>Instalar o pacote `qsharp` do Python

### <a name="install-using-conda-recommended"></a>[Instalar usando o conda (recomendado)](#tab/tabid-conda)

1. Instale o [Miniconda](https://docs.conda.io/en/latest/miniconda.html) ou o [Anaconda](https://www.anaconda.com/products/individual#Downloads). **Observação:** Instalação de 64 bits necessária.

1. Abra um prompt do Anaconda.

   - Ou, se preferir usar o PowerShell ou o pwsh: abra um shell, execute `conda init powershell` e feche-o e abra-o novamente.

1. Crie e ative um novo ambiente de conda chamado `qsharp-env` com os pacotes necessários (incluindo o Jupyter Notebook e o IQ#) executando os seguintes comandos:

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. Execute `python -c "import qsharp"` no mesmo terminal para confirmar a instalação e preencher o cache do pacote local com todos os componentes necessários do QDK.

### <a name="install-using-net-cli-and-pip-advanced"></a>[Instalar usando a CLI do .NET e o pip (avançado)](#tab/tabid-dotnetcli)

1. Pré-requisitos:

    - [Python](https://www.python.org/downloads/) 3.6 ou posterior
    - O gerenciador de pacotes Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [SDK do .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Instale o pacote `qsharp`, um pacote do Python que permite a interoperabilidade entre o Q# e o Python.

    ```
    pip install qsharp
    ```

1. Instale o IQ#, um kernel usado pelo Jupyter e pelo Python que fornece uma funcionalidade básica para compilar e executar operações Q#.

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
    
**_

É isso! Agora você tem o pacote `qsharp` do Python e o kernel do IQ# para Jupyter, que fornecem uma funcionalidade básica para compilar e executar operações Q# do Python e permite usar Jupyter Notebooks do Q#.

## <a name="choose-your-ide"></a>Escolher o IDE

Embora seja possível usar o Q# com o Python em qualquer IDE, é bastante recomendável usar o IDE do VS Code (Visual Studio Code) para os aplicativos Q# + Python. Com a extensão do Visual Studio Code para o QDK, você tem acesso a funcionalidades mais sofisticadas, como avisos, realce de sintaxe, modelos de projeto e muito mais.

Se quiser usar o VS Code:

- Instale o [VS Code](https://code.visualstudio.com/download) (Windows, Linux e Mac).
- Instale a [extensão do QDK para VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Se você prefere usar outro editor, as instruções acima fornecem todas as informações necessárias.

## <a name="write-your-first-no-locq-program"></a>Escrever seu primeiro programa Q#

Agora você está pronto para verificar a instalação do pacote `qsharp` do Python gravando e executando um programa de Q# simples.

1. Crie uma operação mínima de Q# criando um arquivo chamado `Operation.qs` e adicionando o seguinte código a ele:

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. Na mesma pasta de `Operation.qs`, crie um programa Python chamado `host.py` para simular a operação Q# `SampleQuantumRandomNumberGenerator()`:

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. No ambiente criado durante a instalação (ou seja, o ambiente de conda ou de Python em que você instalou `qsharp`), execute o programa:

    ```
    python host.py
    ```

1. Você verá o resultado da operação que invocou. Nesse caso, como a operação gera um resultado aleatório, você verá `0` ou `1` impresso na tela. Caso execute o programa várias vezes, será possível conferir cada resultado em aproximadamente metade do tempo.

> [!NOTE]
> _ O código Python é apenas um programa Python normal. É possível usar qualquer ambiente Python, incluindo Jupyter Notebooks baseados em Python, para escrever o programa nessa linguagem de programação e chamar as operações Q#. O programa Python pode importar operações de Q# de arquivos .qs localizados na mesma pasta que o código Python.

## <a name="next-steps"></a>Próximas etapas

Agora que você testou o Kit de Desenvolvimento Quantum em um ambiente preferencial, será possível seguir este tutorial para gravar e executar [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
