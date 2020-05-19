---
title: Guia do usuário do Q#
description: Visão geral da finalidade e do conteúdo do guia do usuário
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: f535aaedbe6ce181375d48f7023409ad8212c702
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430604"
---
# <a name="the-q-user-guide"></a>Guia do usuário do Q#

Bem-vindo ao guia do usuário do Q#! 

Aqui detalhamos os conceitos fundamentais da linguagem Q# e todas as informações de que você precisa para escrever programas quânticos.

## <a name="user-guide-contents"></a>Conteúdo do guia do usuário

- [Noções básicas do Q#](xref:microsoft.quantum.guide.basics): uma visão geral introdutória da finalidade e da funcionalidade da linguagem de programação Q#. 

### <a name="q-language"></a>Linguagem Q#

- [Tipos em Q#](xref:microsoft.quantum.guide.types): cria o modelo de tipo Q# e descreve a sintaxe para especificar e trabalhar com tipos.

- [Expressões de tipo](xref:microsoft.quantum.guide.expressions): detalha como especificar, referenciar, combinar e operar em valores de cada tipo em Q#. 

### <a name="using-q"></a>Como usar o Q#

- [Estrutura de arquivos Q#](xref:microsoft.quantum.guide.filestructure): descreve a estrutura e a sintaxe de um arquivo `*.qs` Q#.

- [Operações e funções](xref:microsoft.quantum.guide.operationsfunctions): detalha os dois tipos da linguagem Q# que podem ser chamados, isto é, *operações*, que incluem ação em registros qubit, e *funções*, que funcionam estritamente com informações clássicas. 
    Aqui você verá como defini-los e chamá-los, incluindo as versões adjacentes e controladas de operadores quantum.

- [Variáveis](xref:microsoft.quantum.guide.variables): descreve a função de variáveis em programas em Q# e como usá-las com eficiência. 
    Por exemplo, é possível encontrar informações sobre escopos de associação, bem como a diferença entre variáveis imutáveis/mutáveis e como atribuí-las/reatribuí-las.

- [Trabalhar com qubits](xref:microsoft.quantum.guide.qubits): descreve os recursos do Q# usados para lidar com qubits individuais e sistemas de qubits. 
    Especificamente, isso envolve a alocação e a medição desses qubits, bem como a execução de operações neles. 

- [Fluxo de controle](xref:microsoft.quantum.guide.controlflow): detalha os padrões do fluxo de controle de programação disponíveis no Q#, que inclui muitas técnicas padrão (execução condicional, loops for, loops while etc.), bem como o padrão “Repeat-Until-Success” específico do quantum.

- [Teste e depuração](xref:microsoft.quantum.guide.testingdebugging): detalha algumas técnicas para verificar se o código está fazendo o que deveria fazer. 
    Devido à opacidade geral das informações quânticas, a depuração de um programa quântico pode exigir técnicas especializadas. 
    Felizmente, o Q# dá suporte a muitas das técnicas de depuração clássicas com as quais os programadores estão acostumados, bem como àquelas que são específicas para computação quântica. Isso inclui a criação/execução de testes de unidade em Q#, a inserção de *asserções* em valores e probabilidades em seu código e as funções de `Dump`, que produzem o estado do computador de destino. 
    Essas últimas podem ser usadas junto com nosso simulador de estado completo para depurar determinadas partes de computações contornando algumas limitações da computação quântica (por exemplo, o teorema da não clonagem).

### <a name="quantum-simulators-and-resource-estimators"></a>Simuladores Quantum e avaliadores de recursos

- [Simuladores quantum e aplicativos host](xref:microsoft.quantum.machines): uma visão geral dos diferentes simuladores disponíveis, bem como o modelo de execução geral entre o programa host e os computadores de destino.

- [Simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator): o computador de destino que simula o estado quântico completo. Útil para execução ou depuração completa de programas de menor escala (menos de duas dúzias de qubits)

- [Avaliador de recursos](xref:microsoft.quantum.machines.resources-estimator): estima os recursos necessários para executar uma determinada instância de uma operação em Q# em um computador quantum.

- [Simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro): executa um programa quantum da Microsoft sem realmente simular o estado de um computador quantum e, portanto, pode executar programas quantum que usam milhares de qubits. Útil para depurar um código clássico dentro de um programa quantum, bem como estimar os recursos necessários.

- [Simulador Toffoli](xref:microsoft.quantum.machines.toffoli-simulator): um simulador quantum de uso especial que pode ser usado com milhões de qubits, mas somente para programas com um conjunto restrito de operações quantum (ou seja, X, CNOT e X com vários controlados).

### <a name="quick-reference-pages"></a>Páginas de referência rápida

- [Comandos magic do IQ#](xref:microsoft.quantum.guide.quickref.iqsharp): Página de referência rápida para comandos magic do IQ# Jupyter Notebooks em Q#.
