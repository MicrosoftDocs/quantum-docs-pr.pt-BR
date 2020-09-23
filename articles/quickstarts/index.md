---
title: Configurar o Microsoft QDK (Quantum Development Kit)
description: Aprenda a instalar o Microsoft Quantum Development Kit para diferentes ambientes.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834475"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a>Configurar o Microsoft QDK (Quantum Development Kit)

Saiba como configurar o Microsoft QDK (Quantum Development Kit) para seu ambiente e comece a usar a programação quântica. O QDK consiste no seguinte:

- A linguagem de programação Q#
- Um conjunto de bibliotecas que abstraem o recurso complexo em Q#
- APIs para as linguagens Python e .NET (C#, F# e VB.NET) para executar programas quânticos escritos em Q#
- Ferramentas para facilitar seu desenvolvimento

Os programas Q# podem ser executados como aplicativos autônomos usando o Visual Studio Code ou o Visual Studio, por meio dos Jupyter Notebooks com o kernel lQ# do Jupyter ou emparelhados com um programa host escrito em Python ou em uma linguagem .NET (C#, F#). Você também pode executar programas Q# online usando o [Codespaces](https://online.visualstudio.com/), o [MyBinder.org](https://mybinder.org/) ou o [Docker](#use-the-qdk-with-docker). 

## <a name="options-for-setting-up-the-qdk"></a>Opções para configurar o QDK

Você pode usar o QDK de três maneiras:

- [Instalar o QDK localmente](#install-the-qdk-locally)
- [Usar o QDK online](#use-the-qdk-online)
- [Usar uma imagem do Docker QDK](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a>Instalar o QDK localmente

Você pode desenvolver o código Q# na maioria dos seus IDEs favoritos, bem como integrar Q# a outras linguagens, como Python e .NET (C#, F#).

|&nbsp; | **VS Code<br>(2019 ou versões posteriores)**| **Visual Studio<br>(2019 ou versões posteriores)** | **Jupyter Notebooks** | **Linha de comando**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|**SO** |Windows, macOS, Linux |Somente Windows |Windows, macOS, Linux |Windows, macOS, Linux |
|<br>**Q# autônomo** |<br>[Instalar](xref:microsoft.quantum.install.standalone) |<br> [Instalar](xref:microsoft.quantum.install.standalone)  |<br> [Instalar](xref:microsoft.quantum.install.jupyter) |<br>[Instalar](xref:microsoft.quantum.install.standalone)|
|**Q# e Python** |[Instalar](xref:microsoft.quantum.install.python) |[Instalar](xref:microsoft.quantum.install.python) |[Instalar](xref:microsoft.quantum.install.jupyter) |[Instalar](xref:microsoft.quantum.install.python) |
|**Q# e .NET (C#, F#)**|[Instalar](xref:microsoft.quantum.install.cs) |[Instalar](xref:microsoft.quantum.install.cs)|&#10006; |[Instalar](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a>Usar o QDK online

Você também pode desenvolver o código Q# sem instalar nada localmente com estas opções:

|Recurso|Vantagens|Limitações|
|---|---|---|
|[**Codespaces do Visual Studio**](xref:microsoft.quantum.install.standalone)|Um ambiente de desenvolvimento online avançado  |Requer uma assinatura e um plano do Azure |
|[**Binder**](xref:microsoft.quantum.install.binder) | Experiência gratuita de notebook online |Sem persistência |

## <a name="use-the-qdk-with-docker"></a>Usar o QDK com o Docker

Você pode usar nossa imagem do Docker QDK em sua instalação local do Docker ou na nuvem por meio de qualquer serviço que dê suporte a imagens do Docker, como a ACI.

Você pode baixar a imagem do Docker IQ# de https://github.com/microsoft/iqsharp/#using-iq-as-a-container. 

Você também pode usar o Docker com um Contêiner de Desenvolvimento Remoto do Visual Studio Code para definir ambientes de desenvolvimento com rapidez. Para obter mais informações sobre Contêineres de Desenvolvimento do VS Code, confira https://github.com/microsoft/Quantum/tree/master/.devcontainer.

## <a name="next-steps"></a>Próximas etapas

Os fluxos de trabalho de cada uma dessas configurações são descritos e comparados em [Maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).
