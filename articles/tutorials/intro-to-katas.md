---
title: Introdução ao Quantum Katas
description: Saiba mais sobre os katas (exercícios de treinamento) fornecidos no QDK (Microsoft Quantum development kit)
author: bradben
ms.author: bradben
ms.date: 06/02/2020
ms.topic: overview
uid: microsoft.quantum.overview.katas
no-loc:
- Q#
- $$v
ms.openlocfilehash: 780f04aa941d416032ea3e50b05769f93fae769f
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759384"
---
# <a name="learn-quantum-computing-with-the-quantum-katas"></a>Conheça a computação quântica com o Quantum Katas

[Os katas Quantum são os](https://github.com/Microsoft/QuantumKatas/) tutoriais individualizados de software livre e os exercícios de programação destinados a ensinar os elementos de computação e Q# programação Quantum ao mesmo tempo.

## <a name="learning-by-doing"></a>Aprender fazendo

Os tutoriais e os exercícios coletados neste projeto destacam o aprender fazendo: eles oferecem tarefas de programação que abordam determinados tópicos que avançam desde muito simples a bastante desafiadores. Cada tarefa solicita que você preencha alguns códigos: a primeira delas pode exigir apenas uma linha e a última pode exigir um fragmento de código dimensionável.

O mais importante é que o Katas inclui estruturas de teste que configuram, executam e validam as soluções para as tarefas. Com isso, você receberá comentários imediatos sobre sua solução e reconsiderará sua abordagem se ela estiver incorreta.

Você pode usar o Katas para aprender em seu ambiente de sua escolha:

* Jupyter Notebooks online no ambiente do Binder
* Jupyter Notebooks em execução no computador local
* Visual Studio
* Visual Studio Code

## <a name="what-can-i-learn-with-the-quantum-katas"></a>O que eu posso aprender com o Quantum Katas?

Explore os conceitos básicos e os conceitos básicos da computação Quantum ou Aprofunde-se nos algoritmos e protocolos Quantum. Recomendamos que você siga este roteiro de aprendizagem no começo para ter a certeza de que você tem uma noção sólida sobre os conceitos fundamentais da computação quântica. É claro que você pode ignorar os tópicos com os quais está familiarizado, como aritmética complexa, e aprender os algoritmos em qualquer ordem que desejar.

### <a name="introduction-to-quantum-computing-concepts"></a>Introdução aos conceitos de computação quântica

| Kata | Descrição |
|:-----|-------------|
|[Aritmética complexa](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ComplexArithmetic)|Este tutorial explica alguns dos planos de fundo matemáticos necessários para trabalhar com a computação Quantum, como números imaginários e complexos.|
|[Álgebra linear](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/LinearAlgebra)|A Algebra linear é usada para representar os Estados de Quantum e as operações na computação Quantum. Este tutorial aborda as noções básicas, incluindo matrizes e vetores.|
|[O conceito de um qubit](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/Qubit)|Saiba mais sobre o qubits-um dos principais conceitos da computação Quantum. |
|[Portões quânticos de qubit único](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/SingleQubitGates)|Este tutorial apresenta Gates de Quantum de qubit único, que atuam como os blocos de construção de algoritmos de Quantum e que transformam Estados de qubit Quantum de várias maneiras.|
|[Sistemas com vários qubits](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/MultiQubitSystems)|Este tutorial apresenta sistemas qubit, sua representação em notação matemática e em Q# código e o conceito de Entanglement.|
|[Gates de Quantum qubit](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/MultiQubitGates)|Este tutorial segue o tutorial de [Gates de Quantum de qubit único](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/SingleQubitGates) e se concentra em aplicar Gates de Quantum a sistemas qubit.|

### <a name="quantum-computing-fundamentals"></a>Conceitos sobre computação quântica

| Kata | Descrição |
|:-----|-------------|
|[Reconhecer portões quânticos](https://github.com/microsoft/QuantumKatas/tree/main/BasicGates)|Uma série de exercícios projetados para familiarizar-se com as Gates básicas da Quantum no Q# . Inclui exercícios para Gates básico de qubit único e qubit, Gates e entradas controladas e como usar Gates para modificar o estado de um qubit.|
|[Criar uma sobreposição quântica](https://github.com/microsoft/QuantumKatas/tree/main/Superposition)|Use esses exercícios para se familiarizar com o conceito de superposição e programação no Q# . Inclui exercícios para os Gates básico de qubit e qubit, superposição e controle de fluxo e recursão no Q# .|
|[Diferenciar estados quânticos usando medidas](https://github.com/microsoft/QuantumKatas/tree/main/Measurements)|Resolva esses exercícios enquanto aprende sobre a medição Quantum e os Estados ortogonal e não ortogonal. |
|[Medidas conjuntas](https://github.com/microsoft/QuantumKatas/tree/main/JointMeasurements)|Saiba mais sobre as medidas de paridade conjuntas e como usar a operação de [medida](xref:microsoft.quantum.intrinsic.measure) para distinguir os Estados da Quantum.|

### <a name="algorithms"></a>Algoritmos

| Kata | Descrição |
|:-----|-------------|
|[Portabilidade quântica](https://github.com/microsoft/QuantumKatas/tree/main/Teleportation)|Este Kata explora a teleportação Quantum, um protocolo que permite a comunicação de um estado Quantum usando apenas a comunicação clássica e a Entanglement Quantum anteriormente compartilhada.|
|[Codificação superdensa](https://github.com/microsoft/QuantumKatas/tree/main/SuperdenseCoding)|A codificação superdensa é um protocolo que permite a transmissão de dois bits de informações clássicas enviando apenas um qubit usando Entanglement Quantum compartilhado anteriormente.  |
|[Algoritmo Deutsch-Jozsa](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ExploringDeutschJozsaAlgorithm)|Esse algoritmo é famoso para ser um dos primeiros exemplos de um algoritmo Quantum que é exponencialmente mais rápido do que qualquer algoritmo clássico determinístico.|
|[Explorar propriedades de alto nível do algoritmo de pesquisa de Grover](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ExploringGroversAlgorithm)|Uma introdução de alto nível para um dos algoritmos mais famosos na computação Quantum. Ele resolve o problema de localizar uma entrada para uma caixa preta (Oracle) que produz uma saída específica. |
|[Implementar o algoritmo de pesquisa de Grover](https://github.com/microsoft/QuantumKatas/tree/main/GroversAlgorithm)|Essa Kata se aprofunda no algoritmo de pesquisa do Grover e aborda a escrita de Oracle, a execução de etapas do algoritmo e, finalmente, a colocação em todos.|
|[Resolvendo problemas reais usando o algoritmo do Grover: problemas de SAT](https://github.com/microsoft/QuantumKatas/tree/main/SolveSATWithGrover)|Uma série de exercícios que usa o algoritmo do Grover para resolver problemas realistas, usando [problemas de satisfazbilidade booliano](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem) (SAT) como exemplo.  |
|[Resolvendo problemas reais usando o algoritmo do Grover: problemas de cores do grafo](https://github.com/microsoft/QuantumKatas/tree/main/GraphColoring)| Esse Kata explora ainda mais o algoritmo do Grover, desta vez para resolver [problemas de satisfação de restrição](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem), usando um problema de coloração de grafo como um exemplo. |

### <a name="protocols-and-libraries"></a>Protocolos e bibliotecas

| Kata | Descrição |
|:-----|-------------|
|[Protocolo BB84 para distribuição de chave quântica](https://github.com/microsoft/QuantumKatas/tree/main/KeyDistribution_BB84)|Saiba mais e implemente um protocolo Quantum de distribuição de chaves, [BB84](https://en.wikipedia.org/wiki/BB84), usando qubits para trocar chaves de criptografia. |
|[Bit-inverter código de correção de erro](https://github.com/microsoft/QuantumKatas/tree/main/QEC_BitFlipCode)|Explore a correção de erro do Quantum com o mais simples dos códigos de correção de erro Quantum (QEC)-o código de inversão de bit três qubit.|
|[Estimativa de fase](https://github.com/microsoft/QuantumKatas/blob/main/PhaseEstimation)|Os algoritmos de estimativa de fase são alguns dos blocos de construção mais fundamentais da computação Quantum. Saiba mais sobre a estimativa de fase com esses exercícios que abrangem a estimativa da fase Quantum e como preparar e executar rotinas de estimativa de fase no Q# .|
|[Aritmética de Quantum: Compilando o ondulador-transportar somas](https://github.com/microsoft/QuantumKatas/blob/main/RippleCarryAdder)|Uma série detalhada de exercícios que explora a adição da [ondulação](https://en.wikipedia.org/wiki/Adder_(electronics)#Ripple-carry_adder) em um computador Quantum. Crie um adicionador de Quantum no local, expanda-o com um algoritmo diferente e, por fim, crie um subtrator de Quantum in-loco.   |

### <a name="entanglement-games"></a>Jogos de entrelaçamento

| Kata | Descrição |
|:-----|-------------|
|[Jogo CHSH](https://github.com/microsoft/QuantumKatas/tree/main/CHSHGame)|Explore o Quantum Entanglement com uma implementação do jogo [chsh](https://en.wikipedia.org/wiki/CHSH_inequality) . Esse jogo não [local](https://en.wikipedia.org/wiki/Quantum_refereed_game) mostra como o Quantum Entanglement pode ser usado para aumentar a chance do jogador de ganhar além do que seria possível com uma estratégia puramente clássica.|
|[Jogo GHZ](https://github.com/microsoft/QuantumKatas/tree/main/GHZGame)|O jogo de GHZ é outro jogo não local, mas envolve três jogadores.|
|[Jogo do quadrado mágico Mermin-Peres](https://github.com/microsoft/QuantumKatas/tree/main/MagicSquareGame)|Uma série de exercícios que explora o [pseudo-telecaminho da Quantum](https://en.wikipedia.org/wiki/Quantum_pseudo-telepathy#The_Mermin%E2%80%93Peres_magic_square_game) para resolver um jogo quadrado mágico.  |

## <a name="resources"></a>Recursos

Confira a série completa do [Quantum Katas](https://github.com/microsoft/QuantumKatas)

[Executar o katas online](https://aka.ms/try-quantum-katas)
