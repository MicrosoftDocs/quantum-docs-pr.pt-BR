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
ms.openlocfilehash: 81f31a531a1b50ead332bb578ccf392ddced9e8d
ms.sourcegitcommit: d98190988ff03146d9ca2b0d325870cd717d729a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2020
ms.locfileid: "91771378"
---
# <a name="the-no-locq-user-guide"></a>Guia do usuário do Q#

Bem-vindo(a) ao guia do usuário do Q#! 

Nos diferentes tópicos deste guia, detalhamos os conceitos fundamentais da linguagem Q# e todas as informações de que você precisa para escrever programas quânticos.

## <a name="user-guide-contents"></a>Conteúdo do guia do usuário

- [Q# Noções básicas](xref:microsoft.quantum.guide.basics): Uma visão geral introdutória da finalidade e da funcionalidade da linguagem de programação Q#. 

- [Maneiras de executar um programa Q#](xref:microsoft.quantum.guide.host-programs): descreve como um programa Q# é executado e mostra uma visão geral das diversas formas de chamar o programa: da linha de comando, de Jupyter Notebooks Q# ou de um programa de host clássico escrito em uma linguagem Python ou .NET.

### <a name="no-locq-language"></a>Linguagem Q#

- [Tipos no Q#](xref:microsoft.quantum.guide.types): Cria o modelo de tipo Q# e descreve a sintaxe para especificar e trabalhar com tipos.

- [Expressões de tipo](xref:microsoft.quantum.guide.expressions): Detalha como especificar, referenciar, combinar e operar em valores de cada tipo em Q#. 

### <a name="using-no-locq"></a>Usando Q#

- [Q# Estrutura do arquivo](xref:microsoft.quantum.guide.filestructure): Descreve a estrutura e a sintaxe de um arquivo `*.qs` no Q#.

- [Operações e funções](xref:microsoft.quantum.guide.operationsfunctions): Detalha os dois tipos da linguagem Q# que podem ser chamados: *operações*, que incluem ação em registros qubit, e *funções*, que funcionam estritamente com informações clássicas. 
    Aqui você verá como defini-los e chamá-los, incluindo as versões adjacentes e controladas de operadores quantum.

- [Variáveis](xref:microsoft.quantum.guide.variables): Descreve a função de variáveis em programas Q# e como usá-las com eficiência. 
    Por exemplo, é possível encontrar informações sobre escopos de associação, bem como a diferença entre variáveis imutáveis e mutáveis e como atribuí-las ou reatribuí-las.

- [Trabalhar com qubits](xref:microsoft.quantum.guide.qubits): Descreve os recursos do Q# usados para tratar qubits e sistemas individuais do qubits, especificamente, alocando-os, executando operações neles e medindo-os. 

- [Fluxo de controle](xref:microsoft.quantum.guide.controlflow): Detalha os padrões do fluxo de controle de programação disponíveis no Q#, que incluem muitas técnicas padrão (como processamento condicional, loops *for* e loops *while*), bem como o padrão *Repeat-Until-Success* específico da computação quântica.

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
