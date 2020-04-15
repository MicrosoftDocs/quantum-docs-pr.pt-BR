---
title: Técnicas de desenvolvimento quântico
description: Aprenda as noções básicas do desenvolvimento de programas em Q#, trabalhe com operações, funções, variáveis e qubits e crie um programa quântico simples.
keywords: Não adicione ou edite palavras-chave sem consultar seu especialista em SEO.
author: QuantumWriter
ms.author: MSFT-alias-person-or-DL
ms.date: 9/20/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.techniques.intro
ms.openlocfilehash: e5b7fbde18afbc0333d89f70c5e4596848e30f4f
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2020
ms.locfileid: "77907708"
---
# <a name="quantum-development-techniques"></a>Técnicas de desenvolvimento quântico

Esta seção da nossa documentação fornece detalhes dos conceitos principais usados para a criação de programas quânticos em Q# e para a interação com esses programas em aplicativos clássicos.
Presumimos que você tenha *algum* conhecimento sobre conceitos de computação quântica, como aqueles descritos em [Conceitos de computação quântica](xref:microsoft.quantum.concepts.intro), mas não é necessário que você seja nenhum especialista em computação quântica para que encontre muito valor nessas seções.

Os conteúdos delas são descritos a seguir.

- [Visão geral do programa Q#](xref:microsoft.quantum.techniques.file-structure) fornece uma visão geral da finalidade e da funcionalidade da linguagem de programação Q#. 
    Em particular, ele esclarece como o Q# *não* é uma linguagem de programação meramente para simulação da mecânica quântica, embora naturalmente essa funcionalidade seja fornecida por nosso simulador de estado completo. 
    Em vez disso, o Q# foi projetado visando o futuro e os programas nessa linguagem descrevem como um computador de controle clássico *interage* com qubits. 

- [Operações e funções](xref:microsoft.quantum.techniques.opsandfunctions) detalha os dois tipos que podem ser chamados da linguagem Q#: *operações* (que incluem ação em sistemas quantum e de qubits) e *funções* (que funcionam estritamente com informações clássicas). 
    Se as informações clássicas e quânticas não funcionassem em conjunto, a computação quântica continuaria fora do nosso alcance. 
    Esta seção descreve como definir e usar esses chamadores no fluxo de controle de um programa em Q#.

- [Variáveis locais](xref:microsoft.quantum.techniques.local-variables) descreve a função de variáveis em programas em Q# e como aproveitá-las com eficiência. 
    Em particular, você aprenderá a diferença entre variáveis imutáveis/mutáveis e como atribuí-las pela primeira vez e atribuí-las novamente.

- [Trabalhar com qubits](xref:microsoft.quantum.techniques.qubits) descreve os recursos do Q# que você pode usar para lidar com qubits individuais e sistemas de qubits. 
    Especificamente, isso envolve a alocação e a medição desses qubits, bem como a execução de operações neles. 
    Além disso, você aprenderá algumas técnicas úteis de fluxo de controle.

- Em [Reunindo tudo](xref:microsoft.quantum.techniques.puttingittogether), você aproveitará as técnicas das seções acima para criar um programa que executa **teletransportação quântica**: o uso de dois bits clássicos para "teletransportar" o estado completo de um qubit para outro.

- [Aprofundar-se](xref:microsoft.quantum.techniques.going-further) apresenta técnicas avançadas que podem ser úteis à medida que você se move em direção à programação quântica mais complexa. 
    Em particular, discutimos o uso de operações e funções *parametrizadas por tipo* em Q#, que permitem um fluxo de controle de ordem superior ao permanecerem independentes dos tipos específicos de entrada/saída das próprias operações e funções, bem como ao *emprestarem* qubits. 
    Esse segundo caso difere da alocação básica do qubit, pois uma operação em Q# pode usar qubits "sujos" (qubits não necessariamente inicializados para um estado conhecido) para auxiliar nos cálculos.

- [Teste e depuração](xref:microsoft.quantum.techniques.testing-and-debugging) detalha algumas técnicas para garantir que o código esteja fazendo o que deveria fazer. 
    Devido à opacidade geral das informações quânticas, a depuração de um programa quântico pode exigir técnicas especializadas. 
    Felizmente, o Q# dá suporte a muitas das técnicas de depuração clássicas com as quais os programadores estão acostumados, bem como àquelas que são específicas para computação quântica. Isso inclui a criação/execução de testes de unidade em Q#, a inserção de *asserções* em valores e probabilidades em seu código e as funções de `Dump`, que produzem o estado do computador de destino. 
    Essas últimas podem ser usadas junto com nosso simulador de estado completo para depurar determinadas partes de computações, contornando algumas limitações da computação quântica (por exemplo, o teorema da não clonagem).


![Quantum](~/media/mobius_strip_preview.png)
