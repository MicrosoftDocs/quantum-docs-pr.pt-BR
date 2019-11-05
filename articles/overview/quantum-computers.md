---
title: O que os computadores quânticos podem fazer?
description: Saiba mais sobre o impacto da computação quântica, dos novos algoritmos quânticos aos algoritmos inspirados em quantum executados em computadores clássicos.
author: natke
ms.author: nakersha
ms.date: 10/23/2019
ms.topic: article
uid: microsoft.quantum.overview.computers
ms.openlocfilehash: d4be970c635ca090e8dcb1b58d5c840eebd4d110
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443827"
---
# <a name="what-can-a-quantum-computer-do"></a>O que um computador quântico pode fazer?

O que podemos fazer com um computador quântico que não pode ser feito com um clássico?

Para resolver alguns dos problemas mais complexos do mundo, em que encontrar uma solução levaria bilhões de anos para os computadores atuais, um computador quântico poderia fazer isso em dias, horas ou, até mesmo, minutos. A computação quântica permitirá que os pesquisadores desenvolvam novos catalizadores e materiais, aprimorem medicamentos, acelerem os avanços em inteligência artificial e respondam a perguntas fundamentais sobre as origens de nosso universo.

## <a name="quantum-simulation"></a>Simulação quântica

O uso de programas quânticos para modelar os próprios sistemas quânticos tem um grande potencial para desbloquear insights que levam a inovações em vários setores. Fotossíntese, supercondutores e moléculas complexas são exemplos de sistemas quânticos que podem ser simulados usando programas quânticos.

A simulação de sistemas microscópicos que se comportam de acordo com as leis da mecânica quântica é computacionalmente cara. Precisamos levar em consideração todos os estados possíveis que possam estar em superposição e o número de estados aumenta exponencialmente com o tamanho do sistema. Em um computador quântico, não precisamos modelar todos os estados do sistema. Em vez disso, inserimos o estado quântico do sistema que desejamos simular no qubits do próprio computador e executamos a simulação com um conjunto específico de portões quânticos. Em outras palavras, usamos um computador quântico para simular um sistema quântico.

As moléculas químicas são sistemas quânticos e, portanto, podem ser analisadas dessa maneira. Um desses produtos químicos específicos é a enzima _nitrogenase_, que, com uma melhor compreensão das propriedades dela, pode ter o potencial de reduzir o consumo de energia e a emissão de gases de efeito estufa dos fertilizantes atuais.

## <a name="cryptography"></a>Criptografia

Talvez a aplicação mais famosa de computadores quânticos está na criptografia, em que Peter Shor mostrou, em 1994, que um computador quântico escalonável podia quebrar toda técnica de criptografia amplamente usada.  A criptografia clássica depende da intratabilidade de operações em grandes números, como fatoração de números grandes em dois números primos.  A computação quântica torna essas operações teoricamente tratáveis (por meio do algoritmo de Shor). Embora a implementação desse algoritmo não seja fisicamente possível com a escala atual do hardware quântico, ela gerou o desenvolvimento de algoritmos resistentes ao quantum para a segurança de dados à prova de obsolescência, incluindo novos algoritmos quânticos para criptografia e distribuição de chave de criptografia.  Aqui na Microsoft, temos a equipe líder mundial em criptografia pós-quântica e em segurança no desenvolvimento de algoritmos resistentes a quantum. 

## <a name="optimization"></a>Otimização

A otimização é a tarefa de executar uma grande pesquisa em um espaço altamente dimensional para uma solução realmente boa que minimize uma determina função de custo.   Em um computador quântico, podemos acelerar os algoritmos de otimização, o que permite que encontremos soluções que não eram possíveis de outra maneira. Os aplicativos variam de transporte e logística, saúde, diagnóstico e ciência de materiais. Pode haver um impacto profundo sobre como esses setores podem se tornar mais eficientes. 

A otimização com a computação quântica nos permite inovar em relação ao transporte e à logística de uma maneira que não é possível com os sistemas clássicos atuais. Otimizar o fluxo de tráfego pode reduzir o congestionamento.  Além do planejamento de rota, há atribuição de portões de avião, entrega de pacotes, agendamento de trabalho e muito mais.  Com inovações em ciência de materiais, haverá novas formas de energia, baterias com maior capacidade, materiais mais leves e mais fortes. 

## <a name="machine-learning"></a>Aprendizado de máquina

Um grande número de cálculos numéricos na computação clássica consiste principalmente na solução de sistemas lineares de equações. Isso é especialmente verdadeiro no campo do aprendizado de máquina, em que a maior parte do custo de computação é usada para calcular o inverso de matrizes enormes.

A boa notícia é que existe um algoritmo quântico que nos permite resolver o sistema de maneira aproximada exponencialmente com mais rapidez do que um computador clássico. Isso abre a porta para grandes aumentos de velocidade em cada problema que precisa da solução para sistemas lineares de equações.

Soluções para problemas nessas áreas ajudarão a resolver a crise de energia, a mudança climática e a escassez de alimentos, além de oferecer um diagnóstico médico pessoal e preciso.

## <a name="quantum-inspired-computing"></a>Computação inspirada em quantum

Os algoritmos inspirados em quantum são implementados com um software clássico, mas usam princípios quânticos para aumentar a velocidade e a precisão.

Os algoritmos inspirados em quantum estão sendo aplicados à pesquisa médica. Por exemplo, para melhorar a precisão da geração de MRI (Imagens de Ressonância Magnética). A computação inspirada em quantum está sendo usada para otimizar a configuração dos computadores de MRI para identificação de doenças específicas.

## <a name="next-steps"></a>Próximas etapas

* [Por que devo aprender computação quântica?](xref:microsoft.quantum.overview.why)
* [Introdução ao Microsoft Quantum development kit](xref:microsoft.quantum.welcome)
