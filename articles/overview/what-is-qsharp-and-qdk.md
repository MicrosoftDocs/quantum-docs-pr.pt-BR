---
title: O que são a linguagem de programação Q# e o QDK?
description: Saiba mais sobre o Microsoft Quantum Development Kit, a linguagem de programação Q# e como criar programas quânticos.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.q-sharp
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3ee9e897eb142bbc9503a617cc3e25c1a665ff35
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866937"
---
# <a name="what-are-the-no-locq-programming-language-and-qdk"></a>O que são a linguagem de programação Q# e o QDK?

O Q# é a linguagem de programação de software livre da Microsoft para o desenvolvimento e a execução de algoritmos quânticos. Ele faz parte do QDK (Quantum Development Kit), que inclui bibliotecas [Q#](xref:microsoft.quantum.libraries), [simuladores quânticos](xref:microsoft.quantum.machines), [extensões para outros ambientes de programação](xref:microsoft.quantum.install) e [documentação da API](xref:microsoft.quantum.standardlibsintro). Além da biblioteca padrão do Q#, o QDK inclui bibliotecas de Química, Machine Learning e Numéricas.

Como uma linguagem de programação, o Q# extrai elementos conhecidos do Python, do C# e do F# e é compatível com um modelo de procedimento básico para escrever programas com loops, instruções if/then e tipos de dados comuns. Ele também apresenta novas operações e estruturas de dados específicas do quantum.

## <a name="what-can-i-do-with-the-qdk"></a>O que posso fazer com o QDK?

O QDK é um kit de desenvolvimento completo para Q#, que pode ser usado com ferramentas e linguagens comuns para desenvolver aplicativos quânticos que podem ser executados em vários ambientes. Os programas Q# podem ser executados como um aplicativo de linha de comando, por meio de Jupyter Notebooks, ou usar um programa de host do Python ou do .NET.

### <a name="develop-in-common-tools-and-environments"></a>Desenvolvimento em ferramentas e ambientes comuns

Integre seu desenvolvimento quântico ao [Visual Studio, ao Visual Studio Code](xref:microsoft.quantum.install.standalone) e aos [Jupyter Notebooks](xref:microsoft.quantum.install.jupyter). Use as APIs internas para emparelhar seus programas com as linguagens de host [Python](xref:microsoft.quantum.install.python) e [.NET](xref:microsoft.quantum.install.cs).

### <a name="try-quantum-operations-and-domain-specific-libraries"></a>Experimentar as operações quânticas e as bibliotecas específicas do domínio

Escreva e teste algoritmos quânticos para explorar a superposição, o emaranhamento e outras operações quânticas. As bibliotecas Q# permitem executar operações quânticas complexas sem precisar criar sequências de operação de nível inferior.

### <a name="run-programs-in-simulators"></a>Executar programas em simuladores

Execute seus programas quânticos em um simulador quântico de estado completo, um simulador de Toffoli de escopo limitado ou teste seu código Q# em diferentes avaliadores de recursos. 

## <a name="where-can-i-learn-more"></a>Onde posso saber mais?

|||
| ---- | ---- |
| **Não estou familiarizado com a computação quântica** | Examine algumas noções básicas de física e computação quântica em [Principais conceitos](xref:microsoft.quantum.overview.understanding).|
| **Quero saber mais sobre a linguagem Q#** | Explore os tipos, as expressões, as variáveis e a estrutura do programa quântico no [Guia do Usuário do Q#](xref:microsoft.quantum.guide).|
| **Quero apenas começar a escrever programas quânticos** | Configure seu ambiente Q# e comece a escrever programas quânticos em [Inícios Rápidos](xref:microsoft.quantum.install).|

## <a name="how-does-no-locq-work"></a>Como funciona o Q#?

Um programa Q# pode ser compilado em um aplicativo de linha de comando autônomo ou chamado por um programa de host escrito em Python ou em uma linguagem .NET.

Quando você compila e executa o programa, ele cria uma instância do simulador quântico e transmite o código Q# para ele. O simulador usa o código Q# para criar qubits (simulações de partículas quânticas) e aplicar transformações para modificar o estado deles. Os resultados das operações quânticas no simulador são retornados para o programa.  

O isolamento do código Q# no simulador garante que os algoritmos sigam as leis da física quântica e possam ser executados corretamente em computadores quânticos.

![qsharp-code-flow](~/media/qsharp-code-flow.png)

## <a name="how-do-i-use-the-qdk"></a>Como usar o QDK?

Tudo o que você precisa para escrever e executar programas Q#, incluindo o compilador Q#, as bibliotecas Q# e os simuladores quânticos, pode ser instalado e executado no computador local. Por fim, você poderá executar seus programas Q# remotamente em um computador quântico real, mas até lá, os simuladores quânticos fornecidos com o QDK fornecem resultados precisos e confiáveis.

- Executar o [Q# na linha de comando](xref:microsoft.quantum.install.standalone) é a maneira mais rápida de começar a usá-lo.

- Execute [Jupyter Notebooks autônomos com o IQ#](xref:microsoft.quantum.install.jupyter), uma extensão do Jupyter para compilar, simular e visualizar programas Q#.

- Caso esteja familiarizado com o [Python](xref:microsoft.quantum.install.python), use-o como uma plataforma de programação de host para começar a usá-lo. O Python é famoso pelo uso difundido não apenas entre desenvolvedores, mas também entre cientistas, pesquisadores e professores.

- Caso já tenha experiência com o [C#, o F# ou o VB.NET](xref:microsoft.quantum.install.cs) e conheça com o ambiente de desenvolvimento do Visual Studio, há apenas algumas extensões que você precisa adicionar ao Visual Studio para prepará-lo para o Q#.  

## <a name="summary"></a>Resumo

O Q# é uma linguagem de programação de software livre para o desenvolvimento de programas quânticos. Ele conta com bibliotecas que permitem criar operações quânticas complexas e simuladores quânticos para executar e testar seus programas com precisão. Os programas Q# podem ser executados como aplicativos autônomos ou chamados em um programa de host do Python ou do .NET e podem ser escritos, executados e testados no computador local.

## <a name="next-steps"></a>Próximas etapas

[Álgebra linear para computação quântica](xref:microsoft.quantum.overview.algebra)
