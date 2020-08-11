---
uid: microsoft.quantum.welcome
title: Introdução ao QDK (Quantum Development Kit)
description: Saiba como começar a programar projetos quânticos no Q# com o Microsoft Quantum Development Kit.
author: bradben
ms.author: bradben
ms.date: 5/10/2020
ms.topic: overview
no-loc:
- Q#
- $$v
ms.openlocfilehash: ff5eb9984da0b22a65f3919599ee18605a206fa0
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867499"
---
# <a name="get-started-with-the-quantum-development-kit-qdk"></a>Introdução ao QDK (Quantum Development Kit)

Bem-vindo ao Microsoft Quantum development kit!  

O QDK (Quantum Development Kit) conta com todas as ferramentas necessárias para criar programas e experimentos quânticos com o Q#, uma linguagem de programação projetada especificamente para o desenvolvimento de aplicativos quânticos.

Para ir direto ao ponto, comece com o [guia de instalação do QDK](xref:microsoft.quantum.install).
Você será guiado pela instalação do Quantum Development Kit em computadores Windows, Linux ou macOS para escrever programas quânticos próprios.

Caso não esteja familiarizado com a computação quântica, examine a seção [Visão geral](xref:microsoft.quantum.overview.introduction) para saber o que os computadores quânticos podem fazer e os conceitos básicos da computação quântica.

## <a name="get-started-programming"></a>Introdução à programação

O Quantum Development Kit oferece várias maneiras de aprender a desenvolver um programa quântico com Q#.
Para começar a usar o poder do quantum, experimente nossos tutoriais:

* [Gerador de números aleatórios quânticos](xref:microsoft.quantum.quickstarts.qrng): comece com um aplicativo no estilo "Olá, Mundo do Q#" que oferece uma breve introdução aos conceitos quânticos e permite criar e executar um aplicativo quântico em poucos minutos.
* [Explorar o emaranhamento com o Q#](xref:microsoft.quantum.write-program): esse tutorial ajuda a escrever um programa Q# que demonstra alguns dos conceitos fundamentais da programação quântica.
    Caso não esteja tudo pronto para iniciar a codificação, você ainda poderá acompanhar sem instalar o QDK e ter uma visão geral da linguagem de programação Q# e dos primeiros conceitos da computação quântica.
* [Algoritmo de pesquisa de Grover](xref:microsoft.quantum.quickstarts.search): explore este exemplo de programa Q# para ter uma ideia da capacidade do Q# de expressar o algoritmo quântico de modo a abstrair as operações quânticas de nível inferior.
    Este tutorial descreverá o desenvolvimento do programa como um aplicativo de linha de comando Q# usando o Visual Studio ou o Visual Studio Code.

### <a name="learning-further"></a>Aprenda ainda mais
* Os [módulos do Microsoft Learn sobre computação quântica](https://docs.microsoft.com/learn/browse/?term=quantum) ensinarão você a dominar os principais conceitos de acordo com seu ritmo e com sua agenda. Aprenda os conceitos básicos de como criar programas quânticos com o QDK com o nosso [primeiro módulo](https://docs.microsoft.com/learn/modules/qsharp-create-first-quantum-development-kit/).
* Para saber ainda mais sobre a programação em Q#, confira o [Quantum Katas](https://github.com/Microsoft/QuantumKatas), uma coleção de exercícios individuais de programação que apresenta a computação quântica por meio de atividades de programação em Q#.
    Muitos desses katas também estão disponíveis como notebooks do Q#. 
* Nosso [repositório de exemplos](https://github.com/Microsoft/Quantum) apresenta vários exemplos de como escrever programas quânticos usando o Q#. A maior parte desses exemplos é gravada usando nossas [bibliotecas quânticas](https://github.com/Microsoft/QuantumLibraries) de software livre, incluindo as bibliotecas [padrão](xref:microsoft.quantum.libraries.standard.intro) e de [química](xref:microsoft.quantum.chemistry.concepts.intro) (mais informações sobre elas abaixo).

## <a name="key-concepts-for-quantum-computing"></a>Principais conceitos da computação quântica

Se você é novato no desenvolvimento quântico, sabemos que isso pode parecer um pouco assustador. Esses principais conceitos foram desenvolvidos para ajudar você a entrar no mundo quântico e entender as diferenças entre a computação quântica e a computação clássica.

* [Noções básicas sobre a computação quântica](xref:microsoft.quantum.overview.understanding)
* [Computadores e simuladores quânticos](xref:microsoft.quantum.overview.simulators)
* [O que são a linguagem de programação Q# e o QDK?](xref:microsoft.quantum.overview.q-sharp)
* [Álgebra linear para computação quântica](xref:microsoft.quantum.overview.algebra)

## <a name="quantum-development-kit-documentation"></a>Documentação do Quantum Development Kit

A documentação atual inclui os seguintes tópicos adicionais:

### <a name="no-locq-developer-guides"></a>Guias do desenvolvedor do Q#

* O [Guia do Usuário do Q#](xref:microsoft.quantum.guide) detalha os principais conceitos para criar programas quânticos em Q#.
* [Simuladores quânticos e aplicativos host](xref:microsoft.quantum.machines): descreve como os algoritmos quânticos são executados, quais computadores quânticos estão disponíveis e como gravar um driver não Q# para o programa quântico.

### <a name="no-locq-libraries"></a>Bibliotecas Q#

* [Bibliotecas padrão do Q#](xref:microsoft.quantum.libraries.standard.intro): descreve as operações e as funções compatíveis com o requisito de controle de linguagem clássica e os algoritmos quânticos do Q#. 
    Os tópicos incluem fluxo de controle, estruturas de dados, correção de erros, teste e depuração. 
* [Biblioteca de química doQ#:](xref:microsoft.quantum.chemistry.concepts.intro) descreve as operações e as funções compatíveis com simulações de química quântica, uma aplicação crítica da computação quântica. Os tópicos incluem a simulação da dinâmica hamiltoniana e a estimativa da fase quântica, entre outros.
* [Biblioteca de numéricosQ#:](xref:microsoft.quantum.numerics.intro) descreve as operações e as funções compatíveis com a expressão de funções aritméticas complexas em termos das operações nativas dos computadores de destino.
* [Referência de biblioteca doQ#:](xref:microsoft.quantum.standardlibsintro) contém informações de referência sobre entidades de biblioteca por namespace.

### <a name="general-quantum-computing"></a>Computação quântica geral

* [Conceitos de computação quântica](xref:microsoft.quantum.concepts.intro): inclui tópicos como a relevância da álgebra linear para computação quântica, a natureza e o uso de um qubit, como ler um circuito quântico e muito mais.
* [Glossário de computação quântica](xref:microsoft.quantum.glossary): mostra os principais termos específicos da computação quântica e do desenvolvimento de programas.
    Se você for novato, essa poderá ser uma referência útil ao ler a documentação.
* [Leitura adicional](xref:microsoft.quantum.more-information): contém referências selecionadas especialmente para a cobertura aprofundada de tópicos de computação quântica.

### <a name="additional-info"></a>Informações adicionais

* [Notas sobre a versão do Microsoft Quantum Development Kit](xref:microsoft.quantum.relnotes).


## <a name="be-a-part-of-the-no-locq-open-source-community"></a>Faça parte da Comunidade de Software Livre do Q#

O Quantum Development Kit é um kit de desenvolvimento de software livre que permite aos desenvolvedores tornar a computação quântica mais acessível para todos, para que possamos resolver alguns dos problemas mais desafiadores do mundo.  Instituições acadêmicas que exigem softwares livres poderão implantar o Q# para aprendizado e desenvolvimento quântico. Transformar o kit de desenvolvimento em um kit de software livre também dá aos desenvolvedores e especialistas de domínio uma oportunidade de contribuir com melhorias e ideias por meio de código.

Seus comentários, sua participação e suas contribuições para o Quantum Development Kit são importantes.  Confira [Contribuir para o Quantum Development Kit](xref:microsoft.quantum.contributing) para saber mais sobre as fontes do Quantum Development Kit, fazer comentários, descobrir como participar das decisões e contribuir para essa plataforma de desenvolvimento quântico em crescimento.

Se você quiser mais informações gerais sobre a iniciativa de computação quântica da Microsoft, confira [Microsoft Quantum](https://www.microsoft.com/en-us/quantum/).
