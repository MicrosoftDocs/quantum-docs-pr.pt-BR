---
title: Configurar o Microsoft QDK (Quantum Development Kit)
description: Aprenda a instalar o Microsoft Quantum Development Kit para diferentes ambientes.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: quickstart
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 15067f1762f4468345beee38c98e1b943081fc1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859019"
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

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><b>Código VS<br>(2019 ou posterior)</b></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="Visual Studio" width="50"/><br><b>Visual Studio<br>(2019 ou posterior)</b></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><b>Jupyter Notebooks</b></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><b>Linha de comando</b></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><b>Suporte a SO:</b></td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Somente Windows</td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Windows, macOS, Linux</td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><b>Q# autônomo</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Instalar</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Instalar</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.jupyter">Instalar</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Instalar</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><b>Q# e Python</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Instalar</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Instalar</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Instalar</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Instalar</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><b>Q# e .NET (C#, F#)</b></td> 
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Instalar</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Instalar</a></td>
        <td align="center">&#10006;</td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Instalar</a></td>
   </tr>
</table>

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
