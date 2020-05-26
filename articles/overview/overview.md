---
title: Introdução à computação quântica
description: Saiba o que é a computação quântica, o que computadores quânticos podem fazer e como aprender computação quântica.
author: bradben
ms.author: bradben
ms.date: 05/05/2020
ms.topic: overview
uid: microsoft.quantum.overview.introduction
ms.openlocfilehash: 7c55420bd35f9b6e0e7ec80ddffe8a861cb7df39
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430774"
---
# <a name="introduction-to-quantum-computing-and-the-quantum-development-kit"></a>Introdução à computação quântica e ao Quantum Development Kit

O Microsoft QDK (Quantum Development Kit) é um conjunto de ferramentas de software livre projetado para ajudar os desenvolvedores a aprender algoritmos quânticos e a escrever programas quânticos. A computação quântica traz consigo a promessa de resolver alguns dos maiores desafios do nosso planeta, nas áreas de meio ambiente, agricultura, saúde, energia, clima, ciência de materiais e outras ainda não encontradas.  

Para alguns desses problemas, mesmo os computadores mais avançados apresentam problemas. Embora a tecnologia quântica esteja apenas começando a impactar o mundo da computação, ela pode ter um amplo alcance e mudar a maneira como pensamos sobre a computação.

## <a name="what-is-quantum-computing"></a>O que é computação quântica?

No uso moderno, a palavra quantum significa a menor unidade discreta possível de qualquer propriedade física, geralmente referindo-se às propriedades de partículas atômicas ou subatômicas. Os computadores quânticos usam partículas quânticas reais, átomos artificiais ou propriedades coletivas de partículas quânticas como unidades de processamento e são dispositivos grandes, complexos e caros.

Aproveitando o comportamento exclusivo da física quântica e aplicando-o à computação, os computadores quânticos apresentam novos conceitos aos métodos tradicionais de programação e usam comportamentos da física quântica, como superposição, emaranhamento e interferência quântica.

## <a name="what-can-a-quantum-computer-do"></a>O que um computador quântico pode fazer?

Um computador quântico não é um supercomputador que pode fazer tudo mais rapidamente, mas há algumas áreas em que os computadores quânticos apresentam excelente desempenho.

- [Simulação quântica](xref:microsoft.quantum.overview.introduction#quantum-simulation)
- [Criptografia](xref:microsoft.quantum.overview.introduction#cryptography-and-shors-algorithm)
- [Pesquisar](xref:microsoft.quantum.overview.introduction#search-and-grovers-algorithm)
- [Otimização](xref:microsoft.quantum.overview.introduction#quantum-inspired-computing-and-optimization)
- [Aprendizado de máquina](xref:microsoft.quantum.overview.introduction#quantum-machine-learning)

## <a name="quantum-simulation"></a>Simulação quântica

Como os computadores quânticos usam os fenômenos quânticos na computação, eles são adequados para modelar outros sistemas quânticos. Fotossíntese, supercondutividade e formações moleculares complexas são exemplos de mecanismos quânticos que podem ser simulados pelos programas quânticos.

## <a name="cryptography-and-shors-algorithm"></a>Criptografia e algoritmo de Shor

Em 1994, Peter Shor demonstrou que um computador quântico escalonável pode decifrar técnicas de criptografia amplamente usadas, como o algoritmo RSA. A criptografia clássica depende da intratabilidade de problemas como fatoração de inteiros ou logaritmos discretos, muitos dos quais podem ser resolvidos com mais eficiência por meio de computadores quânticos.

## <a name="search-and-grovers-algorithm"></a>Pesquisa e algoritmo de Grover

Em 1996, Lov Grover desenvolveu um algoritmo quântico que acelera drasticamente a solução para pesquisas de dados não estruturados, executando a pesquisa em menos etapas do que qualquer algoritmo clássico.

## <a name="quantum-inspired-computing-and-optimization"></a>Computação e otimização inspiradas no quantum

Os algoritmos inspirados no quantum usam princípios quânticos para aumentar a velocidade e a precisão, mas para implementar em sistemas de computadores clássicos. Essa abordagem permite que os desenvolvedores aproveitem hoje mesmo o poder das novas técnicas quânticas sem esperar pelo hardware quântico, que ainda é um setor emergente.

A otimização é o processo de encontrar a melhor solução para um problema, considerando o resultado desejado e as restrições. Fatores como custo, qualidade ou tempo de produção são todos incluídos nas decisões críticas tomadas pela indústria e pela ciência. Os algoritmos de otimização inspirados no quantum em execução nos computadores clássicos de hoje podem encontrar soluções que até agora não foram possíveis. Além de otimizar o fluxo de tráfego para reduzir o congestionamento, há a atribuição de portões de avião, entrega de pacotes, agendamento de trabalhos, entre outros. Com as inovações em ciência de materiais, haverá novas formas de energia, baterias com maior capacidade, bem como materiais mais leves e mais duráveis.

> [!NOTE]
> Leia mais sobre como a computação inspirada no quantum da Microsoft está sendo usada na [ciência de materiais](https://cloudblogs.microsoft.com/quantum/2020/01/21/oti-lumionics-accelerating-materials-design-microsoft-azure-quantum/), no [gerenciamento de riscos](https://cloudblogs.microsoft.com/quantum/2019/05/22/microsoft-quantum-collaborates-with-willis-towers-watson-to-transform-risk-management-solutions/) e na [medicina](https://blogs.microsoft.com/blog/2018/05/18/microsoft-quantum-helps-case-western-reserve-university-advance-mri-research/).

## <a name="quantum-machine-learning"></a>Machine learning quântico

O machine learning em computadores clássicos está revolucionando o mundo da ciência e dos negócios. No entanto, o alto custo computacional do treinamento dos modelos impede o desenvolvimento e o escopo do campo. A área de machine learning quântico explora como desenvolver e implementar um software quântico que permita um machine learning executado mais rapidamente comparado aos computadores clássicos.

O Quantum Development Kit é fornecido com a [biblioteca de machine learning quântico](xref:microsoft.quantum.machine-learning.concepts.intro), que permite executar experimentos híbridos de machine learning quântico/clássico. A biblioteca inclui amostras e tutoriais e fornece as ferramentas necessárias para implementar um novo algoritmo quântico-clássico híbrido, o classificador quântico centrado em circuito, para resolver problemas de classificação supervisionados.

## <a name="q-and-the-microsoft-quantum-development-kit-qdk"></a>Q# e o Microsoft QDK (Quantum Development Kit)

O Q# é a linguagem de programação de software livre da Microsoft para o desenvolvimento e a execução de algoritmos quânticos. Ele faz parte do [QDK](https://docs.microsoft.com/quantum/), um kit de desenvolvimento completo para o Q#, que pode ser usado com ferramentas e linguagens padrão para desenvolver aplicativos quânticos que podem ser executados em vários ambientes, incluindo o simulador quântico completo de estado integral interno.

Há extensões para o Visual Studio e o VS Code, além de pacotes para uso com o Python e o Jupyter Notebook.

O QDK inclui uma biblioteca padrão juntamente com bibliotecas especializadas de química, machine learning e numéricas.

A documentação inclui um guia da linguagem Q#, tutoriais e um código de exemplo para uma introdução rápida, bem como artigos avançados para ajudar você a se aprofundar nos conceitos de computação quântica.  

## <a name="microsoft-quantum-hardware-partners"></a>Parceiros de hardware quântico da Microsoft

A Microsoft está fazendo uma parceria com empresas de hardware quântico para fornecer aos desenvolvedores o acesso à nuvem ao hardware quântico. Aproveitando a plataforma [Azure Quantum](https://azure.microsoft.com/services/quantum/) e a linguagem Q#, os desenvolvedores poderão explorar algoritmos quânticos e executar os programas quânticos em diferentes tipos de hardware quântico.

A [IonQ](https://ionq.com/news/november-4-2019-microsoft-partnership) e a [Honeywell](https://www.honeywell.com/en-us/newsroom/news/2019/11/the-future-of-quantum-computing) usam processadores **baseados em íon capturados**, utilizando íons individuais capturados em um campo eletrônico, enquanto a [QCI](https://quantumcircuits.com/news-and-publications/quantum-circuits-partners-with-microsoft-on-azure-quantum) usa circuitos supercondutores.

## <a name="next-steps"></a>Próximas etapas

[Principais conceitos da computação quântica](xref:microsoft.quantum.overview.understanding)
[Início rápido](xref:microsoft.quantum.welcome)