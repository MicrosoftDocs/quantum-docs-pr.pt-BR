---
title: Instalar o QDK (Microsoft Quantum development kit)
description: Como instalar o Microsoft Quantum Development Kit para diferentes ambientes.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 378970dc911ea5a794590f8336ffc6d3f9673285
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867566"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Instalar o QDK (Microsoft Quantum development kit)

Saiba como instalar o QDK (Microsoft Quantum development kit) para começar a usar a programação quântica. O QDK consiste no seguinte:

- A linguagem de programação Q#
- Um conjunto de bibliotecas que abstraem o recurso complexo em Q#
- APIs para as linguagens Python e .NET (C#, F# e VB.NET) para executar programas quânticos escritos em Q#
- Ferramentas para facilitar seu desenvolvimento

É possível executar programas Q# como aplicativos autônomos no Visual Studio Code, no Visual Studio ou nos Jupyter Notebooks com o kernel IQ# do Jupyter.
Eles também podem ser emparelhados com um programa host escrito em uma linguagem .NET (normalmente C# ) ou Python, permitindo que você chame operações quantum de dentro de um programa clássico.

Os fluxos de trabalho de cada uma dessas configurações são descritos e comparados em [Maneiras de executar um Q# programa](xref:microsoft.quantum.guide.host-programs).

Para prosseguir com a instalação do QDK e a criação de projetos Q#, selecione a configuração de sua preferência:

[Desenvolver com aplicativos de linha de comando do Q#](xref:microsoft.quantum.install.standalone) – Escolha essa abordagem para trabalhar com o Q# na linha de comando. Isso não exige um driver ou um programa de host como as opções abaixo.

[Desenvolver com Jupyter Notebooks em Q#](xref:microsoft.quantum.install.jupyter) – Selecione esse ambiente para executar o código Q# em células com texto inserido ou criar tutoriais interativos de computação quântica. 

[Desenvolver com Q# e Python](xref:microsoft.quantum.install.python) – Permite combinar o Python e o Q# para criar um programa do host do Python que chama operações Q#.

[Desenvolver com Q# e .NET](xref:microsoft.quantum.install.cs) – Combine C#, F# ou VB.NET com Q# para criar um programa do host do .NET que chama operações Q#.
