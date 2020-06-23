---
title: Instalar o QDK (Microsoft Quantum development kit)
description: Como instalar o Microsoft Quantum Development Kit para diferentes ambientes.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 6a52eb0a9cdf699e8bb37578ffa3d73fe96a990e
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273176"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Instalar o QDK (Microsoft Quantum development kit)

Saiba como instalar o QDK (Microsoft Quantum development kit) para começar a usar a programação quântica. O QDK consiste no seguinte:

- A linguagem de programação Q#
- Um conjunto de bibliotecas que abstraem a funcionalidade complexa em Q#
- APIs para as linguagens Python e .Net (C#, F# e VB.NET) para executar programas quânticos escritos em Q#
- Ferramentas para facilitar seu desenvolvimento

Os programas Q# podem ser executados como aplicativos autônomos usando o Visual Studio Code ou o Visual Studio ou por meio de Jupyter Notebooks com o kernel IQ# do Jupyter.

Eles também podem ser emparelhados com um programa host escrito em uma linguagem .NET (normalmente C# ) ou Python, permitindo que você chame operações quantum de dentro de um programa clássico.

O QDK está disponível para vários ambientes de desenvolvimento. Selecione a configuração preferencial entre:

[Desenvolver com aplicativos de linha de comando do Q#](xref:microsoft.quantum.install.standalone) – Escolha essa abordagem para trabalhar com o Q# na linha de comando. Isso não exige um driver ou um programa de host como as opções abaixo.

[Desenvolver com Jupyter Notebooks em Q#](xref:microsoft.quantum.install.jupyter) – Selecione esse ambiente para executar o código do Q# em células com texto inserido ou criar tutoriais interativos de computação quântica. 

[Desenvolver com Q# e Python](xref:microsoft.quantum.install.python) – Permite que você combine o Python e o Q# para criar um programa do host do Python que chama operações Q#.

[Desenvolver com Q# e .NET](xref:microsoft.quantum.install.cs) – Combine C#, F# e VB.NET com Q# para criar um programa do host do .NET que chama operações Q#.
