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
ms.openlocfilehash: 3aafe78d5910027e2836f7dce72c064e75fc4436
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863704"
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

[Fazer desenvolvimento com aplicativos Q#](xref:microsoft.quantum.install.standalone) – Escolha essa abordagem para trabalhar com o Q# no prompt de comando. Isso não exige um driver ou um programa de host como as opções abaixo.

[Desenvolver com Jupyter Notebooks em Q#](xref:microsoft.quantum.install.jupyter) – Selecione esse ambiente para executar o código Q# em células com texto inserido ou criar tutoriais interativos de computação quântica. 

[Desenvolver com Q# e Python](xref:microsoft.quantum.install.python) – Permite combinar o Python e o Q# para criar um programa do host do Python que chama operações Q#.

[Desenvolver com Q# e .NET](xref:microsoft.quantum.install.cs) – Combine C#, F# ou VB.NET com Q# para criar um programa do host do .NET que chama operações Q#.
