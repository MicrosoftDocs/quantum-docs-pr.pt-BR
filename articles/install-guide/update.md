---
title: Atualizar o kit de desenvolvimento Quantum (QDK)
description: 'Descreve como atualizar seus projetos do Q # e o Microsoft Quantum Development Kit para a versão atual.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 3245f587493ce12cfec15c8f932fd092d85f688e
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327554"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Atualizar o Microsoft Quantum Development Kit (QDK)

Saiba como atualizar o Microsoft Quantum Development Kit (QDK) para a versão mais recente.

Este artigo pressupõe que você já tenha o QDK instalado. Se você estiver instalando o pela primeira vez, consulte o guia de [instalação](xref:microsoft.quantum.install).

É recomendável manter-se atualizado com a versão mais recente do QDK. Siga este guia de atualização para atualizar para a versão mais recente do QDK. O processo consiste em duas partes:
1. Atualizando seus arquivos e projetos do Q # existentes para alinhar seu código com qualquer sintaxe atualizada.
2. Atualizar o próprio QDK para o ambiente de desenvolvimento escolhido.

## <a name="updating-q-projects"></a>Atualizando projetos de Q # 

Independentemente de você estar usando C# ou Python para hospedar operações Q #, siga estas instruções para atualizar seus projetos do Q #.

1. Primeiro, verifique se você tem a versão mais recente do [SDK do .NET Core 3,1](https://dotnet.microsoft.com/download). Execute o seguinte comando no prompt de comando:

    ```dotnetcli
    dotnet --version
    ```

    Verifique se a saída é `3.1.100` ou mais alta. Caso contrário, instale a [versão mais recente](https://dotnet.microsoft.com/download) e verifique novamente. Em seguida, siga as instruções abaixo, dependendo da sua configuração (Visual Studio, Visual Studio Code ou diretamente a linha de comando).

### <a name="update-q-projects-in-visual-studio"></a>Atualizar projetos do Q # no Visual Studio
 
1. Atualize para a versão mais recente do Visual Studio 2019, consulte [aqui](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) para obter instruções.
2. Abra sua solução no Visual Studio.
3. No menu, selecione **criar**  ->  **solução limpa**.
4. Em cada um dos seus arquivos. csproj, atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se for um projeto de biblioteca).
    Ou seja, edite as linhas do formulário:

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

5. Em cada um dos arquivos. csproj, defina o SDK `Microsoft.Quantum.Sdk` como, conforme indicado na linha abaixo. Observe que o número de versão deve ser o mais recente disponível e você pode determinar isso revisando as [notas de versão](https://docs.microsoft.com/quantum/relnotes/).

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. Salve e feche todos os arquivos em sua solução.

7. Selecione **ferramentas**  ->  prompt de comando do desenvolvedor de**linha de comando**  ->  **Developer Command Prompt**. Como alternativa, você pode usar o console de gerenciamento de pacotes no Visual Studio.

8. Para cada projeto na solução, execute o seguinte comando para **remover** este pacote:

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Se seus projetos usarem outros pacotes Microsoft. Quantum ou Microsoft. Azure. Quantum (por exemplo, Microsoft. Quantum. Numerics), execute o comando **Add** para que eles atualizem a versão usada.

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. Feche o prompt de comando e selecione **criar**  ->  **solução** de compilação *not* (não selecione recompilar solução).

Agora você pode pular para [atualizar sua extensão QDK do Visual Studio](#update-visual-studio-qdk-extension).


### <a name="update-q-projects-in-visual-studio-code"></a>Atualizar projetos do Q # no Visual Studio Code

1. Em Visual Studio Code, abra a pasta que contém o projeto a ser atualizado.
2. Selecione **terminal**  ->  **novo terminal**.
3. Siga as instruções para atualizar usando a linha de comando (diretamente abaixo).

### <a name="update-q-projects-using-the-command-line"></a>Atualizar projetos do Q # usando a linha de comando

1. Navegue até a pasta que contém o arquivo de projeto principal.

2. Execute o comando a seguir:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Determine a versão atual do QDK. Para encontrá-lo, você pode revisar as [notas de versão](https://docs.microsoft.com/quantum/relnotes/). A versão estará em um formato semelhante a `0.11.2006.207` .

4. Em cada um de seus `.csproj` arquivos, percorra as seguintes etapas:

    - Atualize a estrutura de destino para `netcoreapp3.1` (ou `netstandard2.1` se for um projeto de biblioteca). Ou seja, edite as linhas do formulário:

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

    - Substitua a referência ao SDK na definição do projeto. Certifique-se de que o número de versão corresponde ao valor determinado na **etapa 3**.

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - Remova a referência ao pacote `Microsoft.Quantum.Development.Kit` , se presente, que será especificado na seguinte entrada:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - Atualize a versão de todos os pacotes Quantum da Microsoft para a versão lançada mais recentemente do QDK (determinado na **etapa 3**). Esses pacotes são nomeados com os seguintes padrões:

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        As referências a pacotes têm o seguinte formato:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - Salve o arquivo atualizado.

    - Restaure as dependências do projeto, fazendo o seguinte:

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. Navegue de volta para a pasta que contém o projeto principal e execute:

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

Com seus projetos do Q # agora atualizados, siga as instruções abaixo para atualizar o próprio QDK.

## <a name="updating-the-qdk"></a>Atualizando o QDK

O processo para atualizar o QDK varia de acordo com o ambiente e a linguagem de desenvolvimento.
Selecione seu ambiente de desenvolvimento abaixo.

* [Python: atualizar a extensão IQ #](#update-iq-for-python)
* [Blocos de anotações do Jupyter: Atualize a extensão IQ #](#update-iq-for-jupyter-notebooks)
* [Visual Studio: atualizar a extensão QDK](#update-visual-studio-qdk-extension)
* [VS Code: atualizar a extensão QDK](#update-vs-code-qdk-extension)
* [Linha de comando e C#: atualizar modelos de projeto](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a>Atualizar IQ # para Python

1. Atualizar o `iqsharp` kernel 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Verificar a `iqsharp` versão

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Você deve ver o seguinte resultado:

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    Não se preocupe se sua `iqsharp` versão for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).

3. Atualizar o `qsharp` pacote

    ```bash
    pip install qsharp --upgrade
    ```

4. Verificar a `qsharp` versão

    ```bash
    pip show qsharp
    ```

    Você deve ver o seguinte resultado:

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. Execute o seguinte comando no local de seus `.qs` arquivos

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. Agora você pode usar a versão atualizada do QDK para executar seus programas de Quantum existentes.

### <a name="update-iq-for-jupyter-notebooks"></a>Atualizar IQ # para notebooks Jupyter

1. Atualizar o `iqsharp` kernel

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Verificar a `iqsharp` versão

    ```dotnetcli
    dotnet iqsharp --version
    ```

    A saída deve ser semelhante a esta:

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    Não se preocupe se sua `iqsharp` versão for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).

3. Execute o seguinte comando de uma célula no seu Jupyter Notebook:

    ```
    %workspace reload
    ```

4. Agora você pode abrir um bloco de anotações do Jupyter existente e executá-lo com o QDK atualizado.

### <a name="update-visual-studio-qdk-extension"></a>Atualizar a extensão QDK do Visual Studio

1. Atualizar a extensão do Q # Visual Studio

    - O Visual Studio solicita que você aceite atualizações para a [extensão Quantum do Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Aceitar a atualização

    > [!NOTE]
    > Os modelos de projeto são atualizados com a extensão. Os modelos atualizados se aplicam apenas a projetos recém-criados. O código para seus projetos existentes não é atualizado quando a extensão é atualizada.

### <a name="update-vs-code-qdk-extension"></a>Atualizar VS Code extensão QDK

1. Atualizar a extensão de VS Code Quantum

    - Reiniciar VS Code
    - Navegue até a guia **extensões**
    - Selecione o **Microsoft Quantum Development Kit para Visual Studio Code** extensão
    - Recarregar a extensão

2. Atualize os modelos de projeto Quantum:

   - Ir para **Exibir**  ->  **paleta de comandos**
   - Selecione **Q #: instalar modelos de projeto**
   - Após alguns segundos, você deve obter um pop-up confirmando "modelos de projeto instalados com êxito"

### <a name="c-using-the-dotnet-command-line-tool"></a>C#, usando a `dotnet` ferramenta de linha de comando

1. Atualizar os modelos de projeto Quantum para .NET

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
