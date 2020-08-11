---
title: Atualizar o QDK (Quantum Development Kit)
description: Descreve como atualizar projetos do Q# e o Microsoft Quantum Development Kit para a versão atual.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
no-loc:
- Q#
- $$v
ms.openlocfilehash: dd7360961aa728a6aa63b8d8c4e4840f5bf2afe8
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866750"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Atualizar o Microsoft QDK (Quantum Development Kit)

Saiba como atualizar o Microsoft QDK (Quantum Development Kit) para a última versão.

Este artigo pressupõe que você já tenha o QDK instalado. Se você estiver instalando-o pela primeira vez, consulte o [guia de instalação](xref:microsoft.quantum.install).

Recomendamos manter-se atualizado com a última versão do QDK. Siga este guia de atualização para atualizar o QDK para a última versão. O processo consiste em duas partes:
1. Atualizar os arquivos e os projetos Q# existentes para alinhar o código com qualquer sintaxe atualizada.
2. Atualização do próprio QDK para o ambiente de desenvolvimento escolhido.

## <a name="updating-no-locq-projects"></a>Atualizar projetos do Q# 

Independentemente de você estar usando o C# ou o Python para hospedar operações Q#, siga estas instruções para atualizar projetos do Q#.

1. Primeiro, verifique se você tem a última versão do [SDK do .NET Core 3.1](https://dotnet.microsoft.com/download). Execute o seguinte comando no prompt de comando:

    ```dotnetcli
    dotnet --version
    ```

    Verifique se a saída é `3.1.100` ou superior. Caso contrário, instale a [última versão](https://dotnet.microsoft.com/download) e verifique novamente. Em seguida, siga as instruções abaixo, dependendo da configuração (o Visual Studio, o Visual Studio Code ou diretamente a linha de comando).

### <a name="update-no-locq-projects-in-visual-studio"></a>Atualizar projetos do Q# no Visual Studio
 
1. Atualize para a última versão do Visual Studio 2019. Confira [este link](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) para obter instruções.
2. Abra sua solução no Visual Studio.
3. No menu, selecione **Compilar** -> **Limpar Solução**.
4. Em cada um dos arquivos .csproj, atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se ela for um projeto de biblioteca).
    Ou seja, edite as linhas do formulário:

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    Encontre mais detalhes sobre como especificar as estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

5. Em cada um dos arquivos .csproj, defina o SDK como `Microsoft.Quantum.Sdk`, conforme indicado na linha abaixo. Observe que o número de versão deve ser o último disponível. Determine isso examinando as [notas sobre a versão](https://docs.microsoft.com/quantum/relnotes/).

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    ```

6. Salve e feche todos os arquivos da solução.

7. Selecione **Ferramentas** -> **Linha de Comando** -> **Prompt de Comando do Desenvolvedor**. Como alternativa, você pode usar o console de gerenciamento de pacotes no Visual Studio.

8. Para cada projeto da solução, execute o seguinte comando para **remover** este pacote:

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Se os projetos usarem outros pacotes Microsoft.Quantum ou Microsoft.Azure.Quantum (por exemplo, Microsoft.Quantum.Numerics), execute o comando **add** neles para atualizar a versão usada.

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. Feche o prompt de comando e selecione **Compilar** -> **Compilar Solução** (*não* selecione Recompilar Solução).

Agora acesse [Atualizar sua extensão do QDK no Visual Studio](#update-visual-studio-qdk-extension).


### <a name="update-no-locq-projects-in-visual-studio-code"></a>Atualizar projetos do Q# no Visual Studio Code

1. No Visual Studio Code, abra a pasta que contém o projeto a ser atualizado.
2. Selecione **Terminal** -> **Novo Terminal**.
3. Siga as instruções de atualização usando a linha de comando (diretamente abaixo).

### <a name="update-no-locq-projects-using-the-command-line"></a>Atualizar projetos do Q# na linha de comando

1. Navegue até a pasta que contém o arquivo de projeto principal.

2. Execute o comando a seguir:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Determine a versão atual do QDK. Para encontrá-la, examine as [notas sobre a versão](https://docs.microsoft.com/quantum/relnotes/). A versão estará em um formato semelhante a `0.12.20072031`.

4. Em cada um dos arquivos `.csproj`, execute as seguintes etapas:

    - Atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se ela for um projeto de biblioteca). Ou seja, edite as linhas do formulário:

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        Encontre mais detalhes sobre como especificar as estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

    - Substitua a referência ao SDK na definição de projeto. Verifique se o número de versão corresponde ao valor determinado na **etapa 3**.

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
        ```

    - Remova a referência ao pacote `Microsoft.Quantum.Development.Kit`, se presente, que será especificada na seguinte entrada:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - Atualize a versão de todos os pacotes do Microsoft Quantum para a versão lançada mais recentemente do QDK (determinada na **etapa 3**). Esses pacotes são nomeados com os seguintes padrões:

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        As referências aos pacotes têm o seguinte formato:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.12.20072031" />
        ```

    - Salve o arquivo atualizado.

    - Restaure as dependências do projeto fazendo o seguinte:

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. Volte à pasta que contém o projeto principal e execute:

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

Com os projetos do Q# atualizados, siga estas instruções para atualizar o próprio QDK.

## <a name="updating-the-qdk"></a>Atualizar o QDK

O processo usado para atualizar o QDK varia de acordo com o ambiente e a linguagem de desenvolvimento.
Selecione o ambiente de desenvolvimento abaixo.

* [Python: atualizar o pacote `qsharp`](#update-the-qsharp-python-package)
* [Jupyter Notebooks: atualizar o kernel do IQ#](#update-the-iq-jupyter-kernel)
* [Visual Studio: atualizar a extensão do QDK](#update-visual-studio-qdk-extension)
* [VS Code: atualizar a extensão do QDK](#update-vs-code-qdk-extension)
* [Linha de comando e C#: atualizar modelos de projeto](#c-using-the-dotnet-command-line-tool)


### <a name="update-the-qsharp-python-package"></a>Atualizar o pacote `qsharp` do Python

O procedimento de atualização depende de a instalação original ter sido feita usando o conda ou a CLI do .NET e o pip.

#### <a name="update-using-conda-recommended"></a>[Atualizar usando o conda (recomendado)](#tab/tabid-conda)

1. Ative o ambiente de conda em que você instalou o pacote `qsharp` e execute este comando para atualizá-lo:

    ```
    conda update -c quantum-engineering qsharp
    ```

1. Execute o comando a seguir no local dos arquivos `.qs`:

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[Atualizar usando a CLI do .NET e o pip (avançado)](#tab/tabid-dotnetcli)

1. Atualize o kernel `iqsharp` 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Verifique a versão `iqsharp`

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Você deve ver o seguinte resultado:

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    Não se preocupe se sua versão do `iqsharp` for maior. Ela deve corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).

1. Atualize o pacote `qsharp`:

    ```
    pip install qsharp --upgrade
    ```

1. Verifique a versão `qsharp`:

    ```
    pip show qsharp
    ```

    Você deve ver o seguinte resultado:

    ```
    Name: qsharp
    Version: 0.12.2007.2031
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. Execute o comando a seguir no local dos arquivos `.qs`:

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

***

Agora você pode usar o pacote `qsharp` do Python atualizado para executar seus programas quânticos existentes.

### <a name="update-the-ino-locq-jupyter-kernel"></a>Atualizar o kernel de Jupyter do IQ#

O procedimento de atualização depende de a instalação original ter sido feita usando o conda ou a CLI do .NET e o pip.

#### <a name="update-using-conda-recommended"></a>[Atualizar usando o conda (recomendado)](#tab/tabid-conda)

1. Ative o ambiente de conda em que você instalou o pacote `qsharp` e execute este comando para atualizá-lo:

    ```
    conda update -c quantum-engineering qsharp
    ```

1. Execute o seguinte comando em uma célula em cada um dos Jupyter Notebooks do Q# existentes:

    ```
    %workspace reload
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[Atualizar usando a CLI do .NET e o pip (avançado)](#tab/tabid-dotnetcli)

1. Atualize o pacote `Microsoft.Quantum.IQSharp`:

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Verifique a versão `iqsharp`:

    ```dotnetcli
    dotnet iqsharp --version
    ```

    A saída deve ser semelhante a esta:

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    Não se preocupe se sua versão do `iqsharp` for maior. Ela deve corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).

1. Execute o seguinte comando em uma célula em cada um dos Jupyter Notebooks do Q# existentes:

    ```
    %workspace reload
    ```

***

Agora você pode usar o kernel do IQ# atualizado para executar os Jupyter Notebooks existentes do Q#.

### <a name="update-visual-studio-qdk-extension"></a>Atualizar a extensão do QDK para Visual Studio

1. Atualizar a extensão do Visual Studio do Q#

    - O Visual Studio exibe um aviso solicitando que você aceite as atualizações da [extensão do Quantum no Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Aceite a atualização

    > [!NOTE]
    > Os modelos de projeto serão atualizados com a extensão. Os modelos atualizados se aplicam apenas aos projetos recém-criados. O código para os projetos existentes não é atualizado quando a extensão é atualizada.

### <a name="update-vs-code-qdk-extension"></a>Atualizar a extensão do QDK para VS Code

1. Atualize a extensão do Quantum para VS Code

    - Reinicie o VS Code
    - Navegue até a guia **Extensões**
    - Selecione a extensão **Microsoft Quantum Development Kit para Visual Studio Code**
    - Recarregue a extensão

### <a name="c-using-the-dotnet-command-line-tool"></a>C#, usando a ferramenta de linha de comando `dotnet`

1. Atualizar os modelos de projeto do Quantum para .NET

    Na linha de comando:

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

   Como alternativa, se você pretende usar os modelos de linha de comando e já tiver a extensão VS Code QDK instalada, atualize os modelos de projeto da própria extensão:

   - [Atualizar a extensão QDK](#update-vs-code-qdk-extension)
   - No VS Code, acesse **Exibir** -> **Paleta de Comandos**
   - Selecione **Q#: Instalar modelos de projeto de linha de comando**
   - Após alguns segundos, você verá um pop-up com a mensagem "Modelos de projeto instalados com êxito"
