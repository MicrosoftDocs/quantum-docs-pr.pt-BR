---
title: O que são o Q# e o QDK?
description: Saiba mais sobre o Q#, uma linguagem de programação criada pela Microsoft para desenvolver aplicativos para computadores quânticos e um componente-chave do Microsoft Quantum Development Kit
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: a4bf21887e34ac85f75e5e0b9a033138464fd09d
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "77906994"
---
# <a name="what-are-q-and-the-qdk"></a>O que são o Q# e o QDK?

O Q# é uma linguagem de programação com recursos projetados especificamente para uso com a computação quântica.
Como o principal componente do QDK (Microsoft Quantum Development Kit), o Q# fornece aos programadores quânticos uma estrutura que permite se concentrar nos algoritmos sem precisar se preocupar com detalhes técnicos, como a otimização da sequência de portão ou a implementação física de um computador quântico.

O QDK inclui uma ampla variedade de ferramentas que oferecem aos desenvolvedores tudo o que eles precisam para começar a escrever programas quânticos.
Junto com a linguagem Q#, o QDK inclui:
* as *bibliotecas Q#* , que permitem aos desenvolvedores começar com o pé direito e criar aplicativos quânticos do mundo real hoje
* vários *computadores de destino* em que programas em Q# podem ser executados. Eles incluem avaliadores de recursos e simuladores para programas quânticos maiores, bem como um simulador quântico completo, que se comporta como um computador quântico sem ruído. O último é muito útil para a reformulação de ideias, depuração de programas e aprendizado da física quântica, mas eficiente apenas para programas com relativamente poucos qubits. Estamos muito ansiosos para disponibilizar o hardware de computação quântica como computadores de destino no futuro.
* As *ferramentas* para tornar o trabalho com o Q# o mais fácil possível, como extensões para o Visual Studio, o VS Code e pacotes para uso com Python e Jupyter Notebooks.
* *Documentação da API* para emparelhar o Q# com linguagens do host clássico, como Python e C#

Os aplicativos desenvolvidos com o Microsoft Quantum Development Kit consistem em duas partes:
1. Um ou mais algoritmos quânticos, implementados com a linguagem de programação quântica Q# e invocados pelo programa do host clássico. São formados por 
    - Operações Q#: sub-rotinas com operações quânticas e 
    - Funções Q#: sub-rotinas clássicas usadas dentro do algoritmo quântico.
2. Um programa clássico, implementado em uma linguagem de programação clássica como Python ou C#, que serve como o ponto de entrada principal e invoca operações Q# para executar um algoritmo quântico.

## <a name="write-quantum-programs-not-quantum-circuits"></a>Escrever programas quânticos, e não circuitos quânticos

Nos primórdios da computação quântica, os algoritmos eram visualizados como diagramas da mesma forma que os diagramas de circuito na computação clássica.
Embora o modelo de circuito tenha sido útil por muitos anos na pesquisa da computação quântica, aqui na Microsoft, acreditamos que os desenvolvedores podem ir além dos circuitos quânticos e desenvolver aplicativos e algoritmos quânticos usando o Q#.
A linguagem Q# foi criada para aproveitar o que aprendemos ao longo de décadas de desenvolvimento de software clássico e capacitar os desenvolvedores quânticos com uma funcionalidade de linguagem de alto nível direcionada à computação quântica.

## <a name="how-does-q-work"></a>Como funciona o Q#?

A linguagem de programação Q# fornece um conjunto intuitivo de tipos, operações e expressões lógicas para desenvolver algoritmos sem precisar se preocupar com a lógica interna do computador quântico.

Um dos blocos de construção fundamentais do Q# é o tipo `Qubit`, que não pode ser copiado nem acessado diretamente, assim como um qubit real.
Em vez disso, podemos medi-lo e armazenar o resultado da medida em uma variável `Result`, um tipo Q# que pode usar dois valores possíveis: `Zero` e `One`.
Constructos como esse garantem que os algoritmos sempre respeitem as leis da física quântica e possam ser executados corretamente em simuladores ou computadores quânticos.

O Q# também inclui recursos lógicos clássicos como condicionais e loops com algumas sutilezas para garantir que todas as regras quânticas sejam respeitadas.
Por exemplo, restringir a maneira como os loops são executados para garantir que as operações quânticas não sejam chamadas dentro de funções que podem conter apenas subrotinas determinísticas clássicas.

Os programas Q# geralmente são emparelhados com um programa host escrito em C# ou no Python, que possa fornecer uma organização conveniente dos códigos clássico e quântico.
Além de dar suporte a linguagens como C# e Python, o QDK dá suporte ao Jupyter Notebook com o kernel IQ# Jupyter.

## <a name="what-can-i-use-q-for"></a>Em que o Q# pode ser usado?

### <a name="use-q-to-learn-quantum-computing"></a>Usar o Q# para aprender computação quântica

Até agora, para aprender computação quântica, você precisava aprender o modelo de circuito para entender os algoritmos na forma de sequências ordenadas de medidas e portões quânticos. Com o Q#, você pode seguir outro caminho: aprender a computação quântica escrevendo programas quânticos.

### <a name="use-q-to-design-quantum-algorithms"></a>Usar o Q# para criar algoritmos quânticos

O Q# fornece um número cada vez maior de bibliotecas e tipos definidos pelo usuário que ajudarão você a implementar ferramentas e a criar algoritmos quânticos avançados. Por exemplo, você precisa entrelaçar os dois qubits q1 e q2? Em vez de aplicar individualmente os portões necessários para entrelaçar os qubits, você pode usar a operação já interna `PrepareEntangledState([q1], [q2])`.

### <a name="use-q-to-estimate-quantum-resources"></a>Usar o Q# para estimar recursos quânticos

Você pode simular a execução do seu programa em Q# usando o simulador quântico de estado completo que é fornecido com o QDK (Quantum Development Kit).  O QDK também oferece avaliadores de recursos que fornecem insights sobre o desempenho dos programas Q# que são muito grandes para serem executados em um simulador.  Isso é altamente valioso para designers de algoritmos, porque eles podem ajustar seus programas para usar menos recursos (por ex., menor número de qubits sendo executados para um menor número de operações), para executar em um hardware quântico de menor escala anterior.

### <a name="use-q-to-validate-hardware-performance"></a>Usar o Q# para validar o desempenho do hardware

O diferencial do Q# é que um programa pode ser gravado uma única vez e ser executado em simuladores quânticos para depuração e em vários hardwares de computação quântica.  Os programas de benchmark gravados em Q# podem ser executados para validar o desempenho do hardware e comparar os resultados à medida que os computadores quânticos evoluem e novos ficam disponíveis.  

## <a name="next-steps"></a>Próximas etapas

* [Como saber mais sobre a computação quântica?](xref:microsoft.quantum.overview.learn)
* [Introdução ao Microsoft Quantum development kit](xref:microsoft.quantum.welcome)
