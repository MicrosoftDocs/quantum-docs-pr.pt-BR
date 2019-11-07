---
title: O que é computação quântica?
description: Saiba o que é computação quântica e o que um computador quântico pode fazer
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.what
ms.openlocfilehash: 2f3b64b00a0a9552e52e34cb1e3652810b266eab
ms.sourcegitcommit: edcf15044d7bdf4f8b21fb8f6af4bde475eb13a0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2019
ms.locfileid: "73529925"
---
# <a name="what-is-quantum-computing"></a>O que é computação quântica?

Há alguns problemas tão difíceis e extremamente extensos, que mesmo que todos os supercomputadores do mundo trabalhassem no problema em conjunto, ainda levaria mais tempo do que o tempo de vida do universo para que ele fosse resolvido.

Os computadores quânticos prometem resolver alguns dos principais desafios do nosso planeta, como nas áreas de meio ambiente, agricultura, saúde, energia, clima, ciência de materiais, além daqueles que ainda nem imaginamos. O impacto dos computadores quânticos será imenso e tão grande quanto a criação do transistor em 1947, que abriu o caminho para a economia digital de hoje.

A computação quântica aproveita o comportamento exclusivo da física quântica para oferecer um modelo de computação novo e altamente eficiente. A teoria da física quântica postula que a matéria, em um nível quântico, pode estar em uma superposição de vários estados clássicos. E esses muitos estados interferem uns com os outros, como as ondas em uma poça de maré.  O estado da matéria depois que uma medida "sucumbe" a um dos estados clássicos. 

Depois disso, repetir a mesma medida produzirá o mesmo resultado clássico.  O entrelaçamento quântico ocorre quando as partículas interagem de tal maneira que o estado quântico de cada uma não pode ser descrito independentemente das outras, mesmo quando elas estão fisicamente distantes.  

A computação quântica armazena informações em estados quânticos de matéria e usa sua natureza quântica de sobreposição e entrelaçamento para realizar operações quânticas que computam essas informações, aproveitando e aprendendo a programar a interferência quântica.

A computação quântica pode parecer assustadora, mas com os recursos certos, você pode começar hoje mesmo a criar aplicativos quânticos.

## <a name="the-qubit"></a>O qubit

A computação quântica define os conceitos de computação que refletem o comportamento quântico.  A computação quântica começa com a noção de um qubit.  Em computação quântica, um bit quântico – **qubit** – é uma unidade de informações quânticas, como um bit clássico. Quando bits clássicos armazenam um único valor binário como 0 ou 1, o estado de um qubit pode estar em uma **sobreposição** de 0 e 1 simultaneamente.  

O ato de medir um qubit altera o estado de um qubit. Com a medição, o qubit passa de estar em sobreposição para um dos estados clássicos.  

Vários qubits também podem ser **entrelaçados**. Quando fazemos uma medição de um qubit entrelaçado, nosso conhecimento do estado dos outros é atualizado também.

## <a name="quantum-algorithms"></a>Algoritmos quantum

Os algoritmos quânticos foram criados para aproveitar a natureza e o comportamento quânticos para acelerar os algoritmos clássicos ou fornecer maneiras totalmente novas de modelar sistemas físicos.  Esses algoritmos exploram a maneira em que os qubits codificam informações e a natureza paralela da operação em vários qubits entrelaçados em sobreposição.  

Os computadores clássicos codificam informações em bits. Cada bit codifica dois valores possíveis, 0 ou 1.  Um qubit codifica dois valores simultaneamente, 0 e 1.  Dois bits clássicos codificam um dos quatro valores possíveis (00, 01, 10, 11), enquanto dois qubits codificam qualquer sobreposição desses quatro estados simultaneamente, embora somente um desses valores possa ser obtido durante a medição. Quatro qubits codificam qualquer sobreposição de 16 valores simultaneamente e assim por diante, exponencialmente.  100 qubits podem codificar mais informações do que o disponível nos maiores sistemas de computador atualmente.  

Além disso, quando vários qubits entrelaçados atuam de forma coerente, eles podem processar várias opções simultaneamente. Os qubits entrelaçados podem processar informações em uma fração do tempo que até mesmo os sistemas não quânticos mais rápidos levariam.

O aproveitamento desses atributos quânticos tem sido a busca de várias décadas de pesquisa sobre algoritmos quânticos, e há muitas técnicas inovadoras que resolvem problemas em uma fração do tempo que leva para a resolução clássica.  

Um dos algoritmos quânticos mais famosos é o _algoritmo de Shor_ para fatoração, o que torna o problema classicamente intratável de fatoração de um número grande em dois números primos rápido o suficiente para o desafio da criptografia tradicional.

No lado mais construtivo, os algoritmos para distribuição de chaves de criptografia seguras são possibilitados por superposição, entrelaçamento quântico e a propriedade de **não clonagem** de qubits, o que indica a incapacidade dos qubits de serem copiados sem detecção.

O _algoritmo de Grover_ realça uma técnica de algoritmo quântico que fornece uma velocidade quadrática para pesquisar dados não estruturados.

## <a name="quantum-hardware"></a>Hardware quântico

Em computadores clássicos, os bits correspondem aos níveis de voltagem nos circuitos de silício. O hardware de computação quântica pode ser implementado por várias realizações físicas diferentes de qubits: íons presos, supercondutividade, átomos neutros, spin eletrônico, polarização da luz e qubits topológicos. O hardware quântico é uma tecnologia emergente. Os qubits são frágeis por natureza e se tornam menos coerentes conforme interagem com o ambiente. É necessário balancear a fidelidade com a escalabilidade do sistema. Quanto maior a escala (ou seja, o número de qubits), maior a taxa de erros.

A Microsoft está desenvolvendo um computador quântico baseado em qubits topológicos. Acreditamos que um qubit topológico será menos afetado pelas alterações no ambiente, reduzindo, portanto, o grau de correção externa de erros. O recurso de qubits topológicos aumentou a estabilidade e a resistência ao ruído ambiental, o que significa que eles podem ser dimensionados com mais facilidade e permanecer confiáveis por mais tempo.

## <a name="quantum-computing--a-full-hardware-and-software-stack"></a>Computação quântica – uma pilha completa de hardware e software

O programa quântico da Microsoft é único pois nos focamos no dimensionamento de cada componente do sistema para oferecer impacto quântico real. Essa abordagem abrangente envolve:

* a criação de um computador quântico usando qubits topológicos confiáveis, escalonáveis e tolerantes a falhas, 
* o projeto de um painel de controle criogênico exclusivo com potência baixa e dissipação de calor, 
* desenvolver uma pilha de software completa para habilitar a programação do computador quântico e controlar o sistema em escala.

O QDK (Quantum Development Kit) de software livre foi introduzido para facilitar o acesso à programação quântica e ao desenvolvimento de algoritmos quânticos. Nossa linguagem de programação de alto nível, Q#, aborda os desafios de programação quântica.  Criamos o Q# como uma linguagem de programação de alto nível com foco em quantum voltada para o desenvolvimento de algoritmos e aplicativos. O compilador Q# é integrado em uma pilha de software que permite que um algoritmo quântico seja compilado até as operações primitivas de um computador quântico.  Até determinada escala (número de qubits), a computação quântica pode ser simulada em um computador clássico. Usando a simulação, você pode começar a escrever programas quânticos hoje para execução no hardware quântico amanhã.  Também emparelhamos o Q# com exemplos, bibliotecas e exercícios de aprendizado para que você comece a programação quântica com facilidade hoje mesmo. 

## <a name="next-steps"></a>Próximas etapas

* [O que os computadores quânticos fazem?](xref:microsoft.quantum.overview.computers)
* [Introdução ao Microsoft Quantum development kit](xref:microsoft.quantum.welcome)
* Leia mais sobre os [conceitos da computação quântica](xref:microsoft.quantum.concepts.intro)
