---
title: Computadores e simuladores quantum
description: Saiba mais sobre hardware quântico, simuladores quânticos e como funcionam as operações quânticas.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.simulators
no-loc:
- Q#
- $$v
ms.openlocfilehash: 299baea75865a4f0ece6b490cef3301dd2a672ac
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867702"
---
# <a name="quantum-computers-and-quantum-simulators"></a>Computadores e simuladores quantum

Os computadores quânticos ainda estão no início do desenvolvimento. O hardware e a manutenção são caros e a maioria dos sistemas está localizada em universidades e laboratórios de pesquisa. No entanto, a tecnologia está avançando e o acesso público limitado a alguns sistemas está disponível.

Os simuladores quânticos são programas de software executados em computadores clássicos e possibilitam executar e testar programas quânticos em um ambiente que prevê como os qubits reagirão a diferentes operações.

## <a name="quantum-hardware"></a>Hardware quântico

Um computador quântico é formado por três partes principais: uma área que hospeda os qubits, um método para transferir sinais para os qubits e um computador clássico para executar um programa e enviar instruções.

- O material quântico usado para os qubits é frágil e altamente sensível a interferências ambientais. Para alguns métodos de armazenamento de qubits, a unidade que hospeda os qubits é mantida em uma temperatura logo acima de zero absoluto para maximizar a coerência. Outros tipos de hospedagem de qubits usam uma câmara de vácuo para ajudar a minimizar as vibrações e estabilizar os qubits.  
- Os sinais podem ser enviados para os qubits por meio de uma variedade de métodos, incluindo micro-ondas, laser e voltagem.

Os computadores quânticos enfrentam uma infinidade de desafios para funcionarem corretamente. A correção de erros em computadores quânticos é um problema significativo e o dimensionamento (adição de mais qubits) aumenta a taxa de erros. Devido a essas limitações, um computador quântico da área de trabalho está distante no futuro, mas um computador quântico comercialmente viável baseado em laboratório está mais próximo.

## <a name="quantum-simulators"></a>Simuladores quânticos

Simuladores quânticos executados em computadores clássicos permitem simular a execução de algoritmos quânticos em um sistema quântico.  O QDK (Quantum Development Kit) da Microsoft inclui um simulador de vetor de estado completo junto com outros simuladores quânticos especializados.

## <a name="topological-qubit"></a>Qubit topológico

A Microsoft está desenvolvendo um computador quântico baseado em qubits topológicos. Um qubit topológico será menos afetado pelas alterações no ambiente, reduzindo, portanto, o grau de correção externa de erros necessário.

O recurso de qubits topológicos aumentou a estabilidade e a resistência ao ruído ambiental, o que significa que eles podem ser dimensionados com mais facilidade e permanecer confiáveis por mais tempo.

## <a name="microsoft-and-quantum-hardware-partnerships"></a>Parcerias da Microsoft com fabricantes de hardware quântico

A Microsoft está fazendo uma parceria com os fabricantes de hardware quântico IonQ, Honeywell e QCI para tornar os computadores quânticos acessíveis aos desenvolvedores no futuro. Com a plataforma Azure Quantum, os desenvolvedores poderão usar o QDK (Quantum Development Kit) da Microsoft e o Q# para escrever programas quânticos e executá-los remotamente.

## <a name="quantum-computations"></a>Cálculos quânticos

A execução de cálculos em um computador quântico ou um simulador quântico segue um processo básico:

- Acessar os qubits
- Inicializar os qubits no estado desejado
- Executar operações para transformar os estados dos qubits
- Medir os novos estados dos qubits

A inicialização e a transformação de qubits são feitas por meio de **operações quânticas** (às vezes chamadas de portas quânticas). As operações quânticas são semelhantes às operações lógicas na computação clássica, como AND, OR, NOT e XOR. Uma operação pode ser tão básica quanto a inversão de um estado de qubit de 1 para 0 ou o emaranhamento um par de qubits e tão complexa quanto o uso de várias operações em série para afetar a probabilidade de colapso de um qubit superposto de uma forma ou de outra.

> [!NOTE] 
> As bibliotecas [Q#](xref:microsoft.quantum.libraries) fornecem operações internas que definem combinações complexas de operações quânticas de nível inferior. Use as operações da biblioteca para transformar qubits e criar operações mais complexas definidas pelo usuário.  

A medição do resultado do cálculo nos informa uma resposta, mas em alguns algoritmos quânticos, não necessariamente a resposta correta. Como o resultado de alguns algoritmos quânticos é baseado na probabilidade que foi configurada pelas operações quânticas, esses cálculos são executados várias vezes para obter uma distribuição de probabilidade e refinar a precisão dos resultados.  A garantia de que uma operação retornou uma resposta correta é conhecida como verificação quântica e é um desafio significativo na computação quântica.

## <a name="summary"></a>Resumo

A computação quântica compartilha alguns dos mesmos conceitos da computação clássica, mas adiciona alguns novos ajustes. Estas são algumas das principais considerações:

- O hardware quântico é caro e frágil para o trabalho e, portanto, os simuladores quânticos são usados para escrever e testar programas.
- Os computadores clássicos e quânticos usam operações lógicas (ou portas) para preparar cálculos.
- Os cálculos quânticos retornam probabilidades.

Os avanços em técnicas e hardware quânticos estão mudando rapidamente o campo. Estes são apenas alguns dos [desenvolvimento atuais](https://phys.org/search/?search=quantum+computer&s=0).

## <a name="next-steps"></a>Próximas etapas

[O que são a linguagem de programação Q# e o QDK?](xref:microsoft.quantum.overview.q-sharp)
