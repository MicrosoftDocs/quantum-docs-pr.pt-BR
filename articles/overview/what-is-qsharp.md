---
title: O que é o Q#?
description: Saiba mais sobre o Q#, uma linguagem de programação criada pela Microsoft para desenvolver aplicativos para computadores quânticos
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: e04228ff62092a15c529297bd56b9ee48399f4a5
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443946"
---
# <a name="what-is-q"></a>O que é o Q#?

O Q# é uma linguagem de programação com recursos que são especiais à computação quântica. O Q# fornece aos programadores quânticos uma estrutura que permite que você se concentre nos algoritmos sem precisar se preocupar com detalhes técnicos, como a otimização da sequência de portão ou a implementação física de um computador quântico.

A linguagem de programação Q# fornece um conjunto intuitivo de tipos, operações e expressões lógicas para desenvolver algoritmos sem precisar se preocupar com a lógica interna do computador quântico.

## <a name="code-algorithms"></a>Algoritmos de código

Nos primórdios da computação quântica, os algoritmos eram visualizados como diagramas da mesma forma que os diagramas de circuito na computação clássica.  Embora o modelo de circuito tenha sido muito útil por muitos anos na pesquisa da computação quântica, aqui na Microsoft, acreditamos que os desenvolvedores podem ir além dos circuitos quânticos e desenvolver aplicativos e algoritmos quânticos usando o Q#. A linguagem Q# foi criada para aproveitar o que aprendemos ao longo de décadas de desenvolvimento de software clássico e capacitar os desenvolvedores quânticos com uma funcionalidade de linguagem de alto nível especificamente destinada à computação quântica.


## <a name="how-does-q-work"></a>Como funciona o Q#?

Um dos blocos de construção fundamentais do Q# é o tipo `Qubit`, que não pode ser copiado nem acessado diretamente, assim como um qubit real. Em vez disso, podemos medi-lo e armazenar o resultado da medida em uma variável `Result`, um tipo Q# que pode usar dois valores possíveis: `Zero` e `One`. Constructos como esse garantem que os algoritmos sempre respeitem as leis da física quântica e possam ser executados corretamente em simuladores ou computadores quânticos.

O Q# também inclui recursos lógicos clássicos como condicionais ou loops com algumas sutilezas para garantir que todas as regras quânticas sejam respeitadas. Por exemplo, as operações quânticas precisam ser reversíveis. Isso impõe algumas restrições sobre o modo como os loops são executados.

Os programas Q# geralmente são emparelhados com um programa host escrito em C# ou no Python, que possa fornecer uma organização conveniente dos códigos clássico e quântico. Além de dar suporte a linguagens .NET, como C# e Python, o QDK fornece suporte do Jupyter Notebook com o kernel IQ# Jupyter.

## <a name="use-q-to-learn-quantum-computing"></a>Usar o Q# para aprender computação quântica

Até agora, para aprender computação quântica, você precisava aprender o modelo de circuito para entender os algoritmos na forma de sequências ordenadas de medidas e portões quânticos. Com o Q#, você pode seguir outro caminho: aprender a computação quântica escrevendo programas quânticos.

## <a name="use-q-to-design-quantum-algorithms"></a>Usar o Q# para criar algoritmos quânticos

O Q# fornece um número cada vez maior de bibliotecas e tipos definidos pelo usuário que ajudarão você a implementar ferramentas e a criar algoritmos quânticos avançados. Por exemplo, você precisa entrelaçar os dois qubits q1 e q2? Em vez de aplicar individualmente os portões necessários para entrelaçar os qubits, você pode usar a operação já interna `PrepareEntangledState([q1], [q2])`.

## <a name="use-q-to-estimate-quantum-resources"></a>Usar o Q# para estimar recursos quânticos

Você pode simular a execução do seu programa em Q# usando o simulador quântico de estado completo que é fornecido com o QDK (Quantum Development Kit).  O QDK também fornece avaliadores de recursos que fornecem insights sobre o desempenho de programas em Q# muito grandes para serem executados em um simulador.  Isso é altamente valioso para designers de algoritmos, porque eles podem ajustar seus programas para usar menos recursos (por ex., menor número de qubits sendo executados para um menor número de operações), para executar em um hardware quântico de menor escala anterior.   

## <a name="use-q-to-validate-hardware-performance"></a>Usar o Q# para validar o desempenho do hardware

A beleza do Q# é que um programa pode ser gravado uma vez e ser executado em simuladores quânticos para depuração e executado em vários hardwares de computação quântica.  Os programas de benchmark gravados em Q# podem ser executados para validar o desempenho do hardware e comparar os resultados à medida que os computadores quânticos evoluem e novos ficam disponíveis.  

## <a name="next-steps"></a>Próximas etapas

* [Como fazer para aprender computação quântica?](xref:microsoft.quantum.overview.learn)
* [Introdução ao Microsoft Quantum development kit](xref:microsoft.quantum.welcome)
