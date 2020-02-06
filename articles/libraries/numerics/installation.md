---
title: Instalação e validação de biblioteca de numéricos | Microsoft Docs
description: Instalação e validação de biblioteca de numéricos
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: c41bb73ea484271689eea2ca1b59ce6639dc15a7
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036450"
---
# <a name="numerics-library-installation-and-validation"></a>Instalação e validação de biblioteca de numéricos

O kit de desenvolvimento Quantum fornece suporte para a funcionalidade de numéricos por meio do pacote NuGet [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) .

**Visual Studio > = 2019:** Se você estiver usando o Visual Studio 2019 ou posterior, poderá adicionar o pacote numéricos usando o Gerenciador de pacotes NuGet.
Para fazer isso, selecione "gerenciar pacotes NuGet..." do item de menu "projeto" no Visual Studio.

Na guia procurar, procure o nome do pacote "Microsoft. Quantum. Numerics"

> [!NOTE]
> Certifique-se de marcar "incluir pré-lançamento"

Isso listará os pacotes disponíveis para download.
Passar o mouse sobre "Microsoft. Quantum. Numerics" revela uma seta apontando para baixo à direita do número de versão.
Clique na seta para instalar o pacote numéricos.

Para obter mais detalhes, consulte o [Guia de interface do usuário do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Como alternativa, você pode usar o console do Gerenciador de pacotes para adicionar a biblioteca de numéricos ao seu projeto por meio da interface de linha de comando.

![](../../media/vs2017-nuget-console-menu.png)

No console do Gerenciador de pacotes, execute o seguinte:

```
Install-Package Microsoft.Quantum.Numerics
```

Para obter mais detalhes, consulte o [Guia do console do Gerenciador de pacotes](https://docs.microsoft.com/nuget/tools/package-manager-console).

**Linha de comando ou Visual Studio Code:** Usando a linha de comando por conta própria ou de dentro Visual Studio Code, você pode usar o comando `dotnet` para adicionar a referência do pacote NuGet ao seu projeto:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a>Verificando sua instalação

Como o restante do kit de desenvolvimento Quantum, a biblioteca de numéricos vem com exemplos que ajudam você a começar o mais rapidamente possível.
Para testar a instalação usando esses exemplos, clone o [repositório principal de exemplos](https://github.com/Microsoft/Quantum) e, em seguida, execute um dos exemplos.

Para executar o exemplo de [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) :

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
