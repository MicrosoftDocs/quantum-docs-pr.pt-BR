---
title: Desenvolver com Q# no Jupyter Notebooks
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 10b1faafa70c87a99ea09916e2c386b32f9a570f
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866801"
---
# <a name="develop-with-no-locq-jupyter-notebooks"></a>Desenvolver com Q# no Jupyter Notebooks

Instale o QDK para desenvolver operações Q# no Jupyter Notebooks do Q#.

Os Jupyter Notebooks permitem a execução de código in-loco juntamente com instruções, observações e outros tipos de conteúdo. É o ambiente ideal para escrever código Q# com explicações inseridas ou tutoriais interativos de computação quântica. Veja o que você precisa para começar a criar seus notebooks do Q#.

> [!NOTE]
> * Com os Jupyter Notebooks do Q#, é possível executar somente código Q#, e as operações não podem ser chamadas de programas de host externos (por exemplo, de arquivos de Python ou C#). Esse ambiente não será apropriado se sua meta for combinar um programa de host clássico externo com o programa quântico.

## <a name="install-the-ino-locq-jupyter-kernel"></a>Instalar o kernel de Jupyter do IQ#

IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade básica para compilar e simular operações Q#.

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

### <a name="install-using-net-cli-advanced"></a>[Instalar usando a CLI do .NET (avançado)](#tab/tabid-dotnetcli)

1. Pré-requisitos:

    - [Python](https://www.python.org/downloads/) 3.6 ou posterior
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [SDK do .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Instale o pacote `Microsoft.Quantum.IQSharp`.

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
    
***

É isso! Agora, você tem o kernel do IQ# para Jupyter, que fornece a funcionalidade básica para compilar e executar operações Q# nos Jupyter Notebooks do Q#.

## <a name="create-your-first-no-locq-notebook"></a>Criar seu primeiro notebook em Q#

Agora, você pode verificar a instalação do Jupyter Notebook do Q# escrevendo e executando uma operação simples em Q#.

1. No ambiente criado durante a instalação (ou seja, no ambiente de conda que você criou ou no ambiente de Python em que instalou o Jupyter), execute o seguinte comando para iniciar o servidor do Jupyter Notebook:

    ```
    jupyter notebook
    ```

    - Se o Jupyter Notebook não abrir automaticamente no navegador, copie e cole a URL fornecida pela linha de comando no navegador.

1. Escolha "Novo" → "Q#" para criar um Jupyter Notebook com um kernel do Q# e adicione o seguinte código à primeira célula do notebook:

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. Execute esta célula do notebook:

    ![Célula do Jupyter Notebook com o código Q#](~/media/install-guide-jupyter.png)

    Você deverá ver `SampleQuantumRandomNumberGenerator` na saída da célula. Durante a execução no Jupyter Notebook, o código Q# é compilado e a célula gera o nome das operações encontradas.

1. Em uma nova célula, execute a operação recém-criada (em um simulador) usando o comando `%simulate`:

    ![Célula do Jupyter Notebook com o magic %simulate](~/media/install-guide-jupyter-simulate.png)

    Você verá o resultado da operação que invocou. Nesse caso, como a operação gera um resultado aleatório, você verá `Zero` ou `One` impresso na tela. Se executar a célula repetidamente, você verá cada resultado em aproximadamente metade do tempo.

## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o QDK para Jupyter Notebooks do Q#, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng) escrevendo o código Q# diretamente no ambiente do Jupyter Notebook.

Para ver mais exemplos do que pode ser feito com o Jupyter Notebooks do Q#, confira:

- [Introdução ao Q# e ao Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Nesse artigo, há um Jupyter Notebook do Q# que mostra mais detalhes sobre como usar o Q# no ambiente do Jupyter.
- [Quantum Katas](xref:microsoft.quantum.overview.katas), uma coleção de software livre de tutoriais individuais e conjuntos de exercícios de programação na forma de Jupyter Notebooks do Q#. Os [notebooks do tutorial do Quantum Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) são um bom ponto de partida. O Quantum Katas tem como objetivo ensinar simultaneamente elementos da computação quântica e da programação com o Q#. É um excelente exemplo do tipo de conteúdo que você pode criar com Jupyter Notebooks do Q#.
