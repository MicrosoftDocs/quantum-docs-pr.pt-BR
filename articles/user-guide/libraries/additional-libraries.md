---
title: Usando Q# bibliotecas adicionais
description: Saiba como adicionar bibliotecas adicionais Q# aos seus aplicativos Quantum.
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
no-loc:
- Q#
- $$v
ms.openlocfilehash: 39bf7dc52f4670a6e4536efc437d001c96f9584a
ms.sourcegitcommit: 11bd357baeb6ab53a402882979e75964d0869b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2020
ms.locfileid: "88992132"
---
# <a name="using-additional-no-locq-libraries"></a>Usando Q# bibliotecas adicionais

O kit de desenvolvimento Quantum fornece funcionalidade adicional específica de domínio por meio de _pacotes NuGet_ que podem ser adicionados aos seus Q# projetos.

| Q# Biblioteca  | Pacote NuGet | Observações |
|---------|---------|--------|
| [Q# biblioteca padrão](xref:microsoft.quantum.libraries.standard.intro) | [**Microsoft. Quantum. Standard**](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | Incluído por padrão |
| [Biblioteca de química do Quantum](xref:microsoft.quantum.chemistry.concepts.intro) | [**Microsoft.Quantum.Chemistry**](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [Biblioteca de numéricos do Quantum](xref:microsoft.quantum.numerics.intro) | [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [Biblioteca de aprendizado de máquina quântico](xref:microsoft.quantum.libraries.machine-learning.intro) | [**Microsoft.Quantum.MachineLearning**](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

Depois de instalar o kit de desenvolvimento Quantum para uso com seu ambiente e idioma de host preferenciais, você poderá adicionar bibliotecas a projetos individuais com facilidade Q# sem nenhuma outra instalação.

> [!NOTE]
> Algumas Q# bibliotecas podem funcionar bem com ferramentas adicionais que funcionam junto Q# com seus programas ou que se integram aos seus aplicativos host.
> Por exemplo, as [instruções de instalação da biblioteca do química](xref:microsoft.quantum.chemistry.concepts.installation) descrevem como usar o [pacote **Microsoft. Quantum. química** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) junto com a plataforma química computacional NWChem e como instalar as `qdk-chem` ferramentas de linha de comando para trabalhar com dados de química do Quantum.

## <a name="no-locq-applications-or-net-interopability"></a>[Q# aplicativos ou interoperabilidade do .NET](#tab/tabid-csproj)

**Prompt de comando ou Visual Studio Code:** Usando o prompt de comando por conta própria ou de dentro de Visual Studio Code, você pode usar o `dotnet` comando para adicionar uma referência de pacote NuGet ao seu projeto.
Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) , execute o seguinte comando:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

**Visual Studio:** Se você estiver usando o Visual Studio 2019 ou posterior, poderá adicionar Q# pacotes adicionais usando o Gerenciador de pacotes NuGet.
Para carregar um pacote: 
1. Com um projeto aberto no Visual Studio, selecione **gerenciar pacotes NuGet...** no menu **projeto** .

2. Clique em **procurar**, selecione **incluir pré-lançamento** e procure o nome do pacote "Microsoft. Quantum. Numerics". Isso listará os pacotes disponíveis para download.

3. Passe o mouse sobre **Microsoft. Quantum. Numerics** e clique na seta apontando para baixo à direita do número de versão para instalar o pacote numérico.

Para obter mais detalhes, consulte o [Guia de interface do usuário do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Como alternativa, você pode usar o console do Gerenciador de pacotes para adicionar a biblioteca de numéricos ao seu projeto por meio da interface de linha de comando.

![Usar o console do Gerenciador de pacotes no prompt de comando](~/media/vs2017-nuget-console-menu.png)

No console do Gerenciador de pacotes, execute o seguinte:

```
Install-Package Microsoft.Quantum.Numerics
```

Para obter mais detalhes, consulte o [Guia do console do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-console).

## <a name="ino-locq-notebooks"></a>[Q#Blocos de anotações](#tab/tabid-notebook)

Você pode disponibilizar pacotes adicionais para uso em um Q# bloco de anotações I usando o [ `%package` comando mágico](xref:microsoft.quantum.iqsharp.magic-ref.package).
Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) para uso em um Q# bloco de anotações I, execute o seguinte comando em uma célula do notebook:

```
%package Microsoft.Quantum.Numerics
```

Após esse comando, o pacote estará disponível para qualquer célula no bloco de anotações.
Para disponibilizar o pacote do Q# código no espaço de trabalho atual, recarregue o espaço de trabalho depois de adicionar o pacote:

```
%workspace reload
```

## <a name="python-interoperability"></a>[Interoperabilidade do Python](#tab/tabid-python)


Você pode disponibilizar pacotes adicionais para uso em um programa de host do Python usando o [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages) método.
Por exemplo, para adicionar o pacote [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) para uso em um Q# bloco de anotações I, execute o seguinte código Python:

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

Após esse comando, o pacote será disponibilizado para qualquer Q# código compilado usando `qsharp.compile` .
Para disponibilizar o pacote do Q# código no espaço de trabalho atual, recarregue o espaço de trabalho depois de adicionar o pacote:

```python
qsharp.reload()
```

***
