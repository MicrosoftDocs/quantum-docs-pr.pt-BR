---
title: Guia do usuário do Q#
description: Visão geral da finalidade e do conteúdo do guia do usuário
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
no-loc:
- Q#
- $$v
ms.openlocfilehash: 979e468cc743bd9125eaba0b71f794977c914447
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231750"
---
# <a name="the-no-locq-user-guide"></a>Guia do usuário do Q#

Bem-vindo(a) ao guia do usuário do Q#! 

Nos diferentes tópicos deste guia, apresentamos algumas das noções básicas para o desenvolvimento de programas quantum usando o Q#.

Nós nos referimos ao guia da linguagem [Q#](xref:microsoft.quantum.qsharp.index) para obter uma especificação e documentação completas da linguagem de programação quantum Q#. 

## <a name="user-guide-contents"></a>Conteúdo do guia do usuário

- Programas [Q#](xref:microsoft.quantum.guide.programs): uma rápida introdução aos programas quânticos no Q#. 

- [Maneiras de executar um programa Q#](xref:microsoft.quantum.guide.host-programs): descreve como um programa Q# é executado e mostra uma visão geral das diversas formas de chamar o programa: da linha de comando, de Jupyter Notebooks Q# ou de um programa de host clássico escrito em uma linguagem Python ou .NET.

- [Testando e depurando](xref:microsoft.quantum.guide.testingdebugging): Detalha algumas técnicas para verificar se o código está fazendo o que deveria fazer. 
    Devido à opacidade geral das informações quânticas, a depuração de um programa quântico pode exigir técnicas especializadas. 
    Felizmente, o Q# é compatível com muitas das técnicas de depuração clássicas que os programadores já conhecem, bem como aquelas específicas para computação quântica. Isso inclui a criação e execução de testes de unidade em Q#, a inserção de *declarações* em valores e probabilidades no código e as funções `Dump`, que produzem os estados dos computadores de destino. 
    Essas últimas podem ser usadas junto com nosso simulador de estado completo para depurar determinadas partes de computações contornando algumas limitações da computação quântica (por exemplo, o [teorema da não clonagem](xref:microsoft.quantum.concepts.pauli)).

### <a name="quantum-simulators-and-resource-estimators"></a>Simuladores Quantum e avaliadores de recursos

- [Simuladores e aplicativos host quânticos](xref:microsoft.quantum.machines): Uma visão geral dos diferentes simuladores disponíveis e de como os programas host e os computadores de destino funcionam juntos para executar programas Q#.

- [Simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator): O computador de destino que simula o estado quântico completo. Útil para execução ou depuração completa de programas de menor escala (menos que algumas dúzias de qubits)

- [Estimador de recursos](xref:microsoft.quantum.machines.resources-estimator): Estima os recursos necessários para executar uma determinada instância de uma operação em Q# em um computador quântico.

- [Simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Executa um programa quântico da Microsoft sem realmente simular o estado de um computador quântico e, portanto, pode executar programas quânticos que usam milhares de qubits. Útil para depurar um código clássico dentro de um programa quantum, bem como estimar os recursos necessários.

- [Simulador do Toffoli](xref:microsoft.quantum.machines.toffoli-simulator): Um simulador quantum de uso especial que pode ser usado com milhões de qubits, mas somente para programas com um conjunto restrito de operações quantum (X, CNOT e X multicontrolado).

### <a name="quick-reference-pages"></a>Páginas de referência rápida

- Comandos magic do [IQ#](xref:microsoft.quantum.guide.quickref.iqsharp): Página de referência rápida para comandos magic do IQ# do Jupyter Notebooks no Q#.
