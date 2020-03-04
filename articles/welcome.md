---
uid: microsoft.quantum.welcome
title: Introdução ao QDK (Quantum Development Kit)
description: Saiba como começar a programar projetos quânticos no Q# com o QDK (Microsoft Quantum Development Kit).
author: natke
ms.author: nakersha
ms.date: 10/23/2019
ms.topic: overview
ms.openlocfilehash: cea39e47ec5e7e2ad97adbbb39ba586274564967
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907623"
---
# <a name="get-started-with-the-quantum-development-kit-qdk"></a>Introdução ao QDK (Quantum Development Kit)

Bem-vindo ao Microsoft Quantum development kit!  
O QDK contém todas as ferramentas necessárias para criar programas e experimentos quânticos com Q#, uma linguagem de programação projetada especificamente para o desenvolvimento de aplicativos quânticos. 

Para começar, acesse o [Guia de instalação do QDK](xref:microsoft.quantum.install).
Em seguida, você verá as instruções de instalação do Quantum Development Kit em computadores Windows, Linux ou macOS para que possa gravar seus próprios programas quânticos.

Se você não se sentir pronto para começar a codificar, mas quiser saber mais sobre a computação quântica e o Q#, incentivamos você a ler este artigo para ter uma ideia dos recursos à sua disposição. Na seção [Cinco perguntas sobre computação quântica](#five-questions-about-quantum-computing), você encontrará links para exatamente o que está procurando!

## <a name="get-started-programming"></a>Introdução à programação

O Quantum Development Kit oferece várias maneiras de aprender a desenvolver um programa quântico com Q#.
Para começar a usar a força do quantum, confira nossos *inícios rápidos*:

* O [gerador de números aleatórios quânticos](xref:microsoft.quantum.quickstarts.qrng) é um aplicativo no estilo "Olá, Mundo, do Q#", que oferece uma breve introdução aos conceitos quânticos e permite criar e executar um aplicativo quântico em minutos.
* [Conceitos básicos quânticos com Q#](xref:microsoft.quantum.write-program) orienta você a gravar um programa em Q# que demonstra alguns dos conceitos fundamentais sobre programação quântica. 
    Caso você não esteja pronto para iniciar a codificação, ainda poderá acompanhar sem instalar o QDK e obter uma visão geral da linguagem de programação Q# e dos primeiros conceitos da computação quântica.
* O [algoritmo de pesquisa de Grover](xref:microsoft.quantum.quickstarts.search) oferece um exemplo de um programa Q# para ter uma ideia do poder do Q# para expressar o algoritmo quântico de modo a abstrair as operações quânticas de baixo nível. 
    Esse início rápido orienta você no desenvolvimento do programa usando uma variedade de ambientes de programação (com um host Python ou um host da linguagem .NET e com o Visual Studio ou o Visual Studio Code).

### <a name="learning-further"></a>Aprenda ainda mais
* Se você quiser se aprofundar na programação em Q#, confira o [Quantum Katas](https://github.com/Microsoft/QuantumKatas), uma coleção de exercícios de programação individuais que apresenta a você a computação quântica por meio de exercícios de programação em Q#.
    Muitos desses katas também estão disponíveis como notebooks do Q#. 
* Nosso [repositório de exemplos](https://github.com/Microsoft/Quantum) apresenta vários exemplos de como gravar programas quânticos usando o Q#. A maior parte desses exemplos é gravada usando nossas [bibliotecas quânticas](https://github.com/Microsoft/QuantumLibraries) de software livre, incluindo as bibliotecas [padrão](xref:microsoft.quantum.libraries.standard.intro) e de [química](xref:microsoft.quantum.chemistry.concepts.intro) (mais informações sobre elas abaixo).

## <a name="five-questions-about-quantum-computing"></a>Cinco perguntas sobre computação quântica

Se você é novato no desenvolvimento quântico, sabemos que isso pode parecer um pouco assustador. Fornecemos recursos para ajudar você a começar a aprender sobre a computação quântica. Com a ajuda desses breves artigos, estamos confiantes de que você ficará ansioso para começar a programar em breve.
* [O que é computação quântica?](xref:microsoft.quantum.overview.what)
* [O que os computadores quânticos fazem?](xref:microsoft.quantum.overview.computers)
* [Por que aprender computação quântica?](xref:microsoft.quantum.overview.why)
* [O que é o Q#?](xref:microsoft.quantum.overview.qsharp)
* [Como aprender computação quântica com o Q#](xref:microsoft.quantum.overview.learn)

## <a name="quantum-development-kit-documentation"></a>Documentação do Quantum Development Kit

A documentação atual inclui os seguintes tópicos adicionais:

### <a name="using-q"></a>Como usar o Q#
* [Técnicas de desenvolvimento quânticas](xref:microsoft.quantum.techniques.intro): especifica os principais conceitos usados para criar programas quânticos em Q#. Os tópicos incluem estruturas de arquivo, operações e funções, trabalhos com qubits e alguns tópicos avançados.
* [Referência da linguagem Q#](xref:microsoft.quantum.language.intro): detalha a linguagem Q#, incluindo o modelo de tipo, as expressões, as instruções e o uso do compilador.
* [Simuladores quânticos e aplicativos host](xref:microsoft.quantum.machines): descreve como os algoritmos quânticos são executados, quais computadores quânticos estão disponíveis e como gravar um driver não Q# para o programa quântico.

### <a name="q-libraries"></a>Bibliotecas do Q#
* [Bibliotecas padrão do Q#](xref:microsoft.quantum.libraries.standard.intro): descreve as operações e funções compatíveis com o requisito de controle de linguagem clássica e os algoritmos quânticos do Q#. 
    Os tópicos incluem fluxo de controle, estruturas de dados, correção de erros, teste e depuração. 
* [Biblioteca de química do Q#](xref:microsoft.quantum.chemistry.concepts.intro): descreve as operações e funções compatíveis com simulações de química quântica, uma aplicação crítica da computação quântica. Os tópicos incluem a simulação da dinâmica hamiltoniana e a estimativa da fase quântica, entre outros.
* [Biblioteca de numéricos Q#](xref:microsoft.quantum.numerics.intro): descreve as operações e funções que dão suporte a expressão de funções aritméticas complicadas em termos das operações nativas dos computadores de destino.
* [Referência de biblioteca do Q#](xref:microsoft.quantum.standardlibsintro): contém informações de referência sobre entidades de biblioteca por namespace.

### <a name="general-quantum-computing"></a>Computação quântica geral
* [Conceitos de computação quântica](xref:microsoft.quantum.concepts.intro): inclui tópicos como a relevância da álgebra linear para computação quântica, a natureza e o uso de um qubit, como ler um circuito quântico e muito mais.
* [Glossário de computação quântica](xref:microsoft.quantum.glossary): mostra os principais termos específicos da computação quântica e do desenvolvimento de programas. 
    Se você for novato, essa poderá ser uma referência útil ao ler a documentação.
* [Leitura adicional](xref:microsoft.quantum.more-information): contém referências selecionadas especialmente para a cobertura aprofundada de tópicos de computação quântica.

### <a name="additional-info"></a>Informações adicionais
* [Notas sobre a versão do Microsoft Quantum Development Kit](xref:microsoft.quantum.relnotes).


## <a name="be-a-part-of-the-q-open-source-community"></a>Faça parte da comunidade de software livre do Q#
O Quantum Development Kit é um kit de desenvolvimento de software livre que permite aos desenvolvedores tornar a computação quântica mais acessível para todos, para que possamos resolver alguns dos problemas mais desafiadores do mundo.  Instituições acadêmicas que exigem softwares livres poderão implantar o Q# para aprendizado e desenvolvimento quântico. Transformar o kit de desenvolvimento em um kit de software livre também dá aos desenvolvedores e especialistas de domínio uma oportunidade de contribuir com melhorias e ideias por meio de código.

Seus comentários, sua participação e suas contribuições para o Quantum Development Kit são importantes.  Confira [Contribuir para o Quantum Development Kit](xref:microsoft.quantum.contributing) para saber mais sobre as fontes do Quantum Development Kit, fazer comentários, descobrir como participar das decisões e contribuir para essa plataforma de desenvolvimento quântico em crescimento.

Se você quiser mais informações gerais sobre a iniciativa de computação quântica da Microsoft, confira [Microsoft Quantum](https://www.microsoft.com/en-us/quantum/).
