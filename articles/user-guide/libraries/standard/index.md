---
title: Introdução às bibliotecas padrão Q# da Microsoft
description: Saiba mais sobre as bibliotecas padrão Q# da Microsoft, que definem as operações, as funções e os tipos de dados usados em programas quânticos.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: conceptual
uid: microsoft.quantum.libraries.standard.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 58e271fefba84e45c5558eeee066bc37c22bf63b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858313"
---
# <a name="introduction-to-the-no-locq-standard-libraries"></a>Introdução às Bibliotecas Padrão Q#

O Q# é compatível com uma variedade de diferentes operações, funções e tipos definidos pelo usuário úteis que abrangem as *bibliotecas padrão* do Q#.
O [`Microsoft.Quantum.Development.Kit` pacote NuGet](https://www.nuget.org/packages/microsoft.quantum.development.kit) instalado durante a [instalação e validação](xref:microsoft.quantum.install) fornece o compilador do Q# e partes da biblioteca padrão implementadas pelos computadores de destino.
O [`Microsoft.Quantum.Standard` pacote](https://www.nuget.org/packages/microsoft.quantum.standard) oferece a parte das bibliotecas padrão Q# portáteis entre os computadores de destino.

Os símbolos definidos pelas bibliotecas padrão Q# são definidos em muito mais detalhes na [documentação da API](xref:microsoft.quantum.apiref-intro).

Nas seções a seguir, descreveremos os recursos mais evidentes de cada parte da biblioteca padrão e forneceremos algum contexto sobre como cada recurso pode ser usado na prática.
