---
title: Introdução às bibliotecas padrão Q# da Microsoft
description: Saiba mais sobre as bibliotecas padrão Q# da Microsoft, que definem as operações, as funções e os tipos de dados usados em programas quânticos.
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.intro
ms.openlocfilehash: 820ad885e7134aa723116d4c9f853d88210a5514
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2020
ms.locfileid: "77907147"
---
# <a name="introduction-to-the-q-standard-libraries"></a>Introdução às Bibliotecas Padrão Q# #

Há suporte para o Q# em uma variedade de diferentes operações úteis, funções e tipos definidos pelo usuário que abrangem as *bibliotecas padrão* do Q#.
O [pacote NuGet do `Microsoft.Quantum.Development.Kit`](https://www.nuget.org/packages/microsoft.quantum.development.kit) instalado durante a [instalação e validação](xref:microsoft.quantum.install) fornece o compilador do Q# e partes da biblioteca padrão implementadas pelos computadores de destino.
O [pacote do `Microsoft.Quantum.Standard`](https://www.nuget.org/packages/microsoft.quantum.standard) oferece a parte das bibliotecas padrão Q# portáteis entre os computadores de destino.

Os símbolos definidos pelas bibliotecas padrão Q# são definidos em detalhes muito maiores e mais exaustivos na [documentação da API](xref:microsoft.quantum.standardlibsintro).

Nas seções a seguir, descreveremos os recursos mais evidentes de cada parte da biblioteca padrão e forneceremos algum contexto sobre como cada recurso pode ser usado na prática.
