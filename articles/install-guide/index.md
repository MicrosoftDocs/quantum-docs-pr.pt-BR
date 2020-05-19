---
title: Instalar o QDK (Microsoft Quantum development kit)
description: Como instalar o Microsoft Quantum Development Kit para diferentes ambientes.
author: natke
ms.author: nakersha
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2041b90ba021b7640615d73c35841cc21f025ac0
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426467"
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

[**Desenvolver com aplicativos de linha de comando do Q#** ](xref:microsoft.quantum.install.standalone) – escolha essa abordagem para trabalhar com o Q# na linha de comando. Isso não exige um driver ou um programa de host como as opções abaixo.

[**Desenvolver com Jupyter Notebooks em Q#** ](xref:microsoft.quantum.install.jupyter) – selecione esse ambiente para executar o código do Q# em células com texto inserido ou criar tutoriais interativos de computação quântica. 

[**Desenvolver com Q# e Python**](xref:microsoft.quantum.install.python) – permite que você combine o Python e o Q# para criar um programa host do Python que chama operações Q#.

[**Desenvolver com o C# ou F#** ](xref:microsoft.quantum.install.cs) – combine o C#, F# e VB.NET com o Q# para criar um programa host do .NET que chama operações Q#.
