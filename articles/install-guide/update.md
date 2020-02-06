---
title: Saiba como atualizar o Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: f19285ae0e008b3460d06430a236f098d716e268
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036297"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Atualizar o Microsoft Quantum Development Kit (QDK)

Saiba como atualizar o Microsoft Quantum Development Kit (QDK) para a versão mais recente.

Este artigo pressupõe que você já tenha o QDK instalado. Se você estiver instalando o pela primeira vez, consulte o guia de [instalação](xref:microsoft.quantum.install).

É recomendável manter-se atualizado com a versão mais recente do QDK. Siga este guia de atualização para atualizar para a versão mais recente do QDK. O processo consiste em duas partes:
1. Atualizando seus arquivos e projetos do Q # existentes para alinhar seu código com qualquer sintaxe atualizada
2. Atualizando o próprio QDK para seu ambiente de desenvolvimento escolhido 

## <a name="updating-q-projects"></a>Atualizando projetos de Q # 

Independentemente de você estar usando C# ou Python para hospedar operações Q #, siga estas instruções para atualizar seus projetos do q #.

1. Primeiro, verifique se você tem a versão mais recente do [SDK do .NET Core 3,1](https://dotnet.microsoft.com/download). Execute o seguinte comando no prompt de comando:

    ```dotnetcli
    dotnet --version
    ```

    Verifique se a saída é `3.1.100` ou superior. Caso contrário, instale a [versão mais recente](https://dotnet.microsoft.com/download) e verifique novamente. Em seguida, siga as instruções abaixo, dependendo da sua configuração (Visual Studio, Visual Studio Code ou diretamente a linha de comando).

### <a name="update-q-projects-in-visual-studio"></a>Atualizar projetos do Q # no Visual Studio
 
1. Atualize para a versão mais recente do Visual Studio 2019, consulte [aqui](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) para obter instruções
2. Abra sua solução no Visual Studio
3. No menu, selecione **criar** -> **solução de limpeza**
4. Em cada um dos seus arquivos. csproj, atualize a estrutura de destino para `netcoreapp3.0` (ou `netstandard2.1` se for um projeto de biblioteca).
    Ou seja, edite as linhas do formulário:

    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```

    Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).
5. Salvar e fechar todos os arquivos em sua solução
6. Selecione **ferramentas** ->  -> de **linha de comando** **prompt de comando do desenvolvedor**
7. Para cada projeto na solução, execute o seguinte comando:

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Se seus projetos usarem qualquer outro pacote do Microsoft. Quantum (por exemplo, Microsoft. Quantum. Numerics), execute o comando para eles também.
8. Feche o prompt de comando e selecione **compilar** -> **Compilar solução** ( *não selecione* recompilar solução)

Agora você pode pular para [atualizar sua extensão QDK do Visual Studio](#update-visual-studio-qdk-extension).


### <a name="update-q-projects-in-visual-studio-code"></a>Atualizar projetos do Q # no Visual Studio Code

1. Em Visual Studio Code, abra a pasta que contém o projeto a ser atualizado
2. Selecionar **terminal** -> **novo terminal**
3. Siga as instruções para atualizar usando a linha de comando (diretamente abaixo)

### <a name="update-q-projects-using-the-command-line"></a>Atualizar projetos do Q # usando a linha de comando

1. Navegue até a pasta que contém o arquivo de projeto
2. Execute o seguinte comando:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Em cada um dos seus arquivos. csproj, atualize a estrutura de destino para `netcoreapp3.0` (ou `netstandard2.1` se for um projeto de biblioteca).
    Ou seja, edite as linhas do formulário:

    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```

    Você pode encontrar mais detalhes sobre como especificar estruturas de destino [aqui](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).
4. Execute o seguinte comando:

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    Se seu projeto usar qualquer outro pacote do Microsoft. Quantum (por exemplo, Microsoft. Quantum. Numerics), execute o comando para eles também.
5. Salve e feche todos os arquivos.
6. Repita a 1-4 para cada dependência do projeto e, em seguida, navegue de volta para a pasta que contém o projeto principal e execute:

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

1. Atualizar o kernel `iqsharp` 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Verificar a versão do `iqsharp`

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Você deve ver o seguinte resultado:

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    Não se preocupe se sua versão de `iqsharp` for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).

3. Atualizar o pacote de `qsharp`

    ```bash
    pip install qsharp --upgrade
    ```

4. Verificar a versão do `qsharp`

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

5. Execute o seguinte comando no local de seus arquivos de `.qs`

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. Agora você pode usar a versão atualizada do QDK para executar seus programas de Quantum existentes.

### <a name="update-iq-for-jupyter-notebooks"></a>Atualizar IQ # para notebooks Jupyter

1. Atualizar o kernel `iqsharp`

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Verificar a versão do `iqsharp`

    ```dotnetcli
    dotnet iqsharp --version
    ```

    A saída deve ser semelhante a esta:

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    Não se preocupe se sua versão de `iqsharp` for maior, ela deverá corresponder à [versão mais recente](xref:microsoft.quantum.relnotes).

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

   - Acesse **Exibir** -> **Paleta de Comandos**
   - Selecione **Q #: instalar modelos de projeto**
   - Após alguns segundos, você deve obter um pop-up confirmando "modelos de projeto instalados com êxito"

### <a name="c-using-the-dotnet-command-line-tool"></a>C#, usando a ferramenta de linha de comando `dotnet`

1. Atualizar os modelos de projeto Quantum para .NET

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a>O que vem a seguir?

Agora que você atualizou o kit de desenvolvimento Quantum em seu ambiente preferido, você pode continuar a desenvolver e executar seus programas Quantum. Se você ainda não escreveu um programa, você pode começar com [seu primeiro programa Quantum](xref:microsoft.quantum.write-program).
