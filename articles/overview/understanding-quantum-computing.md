---
title: Noções básicas sobre a computação quântica
description: O que são computadores quânticos e como eles usam os princípios da mecânica quântica?
author: bradben
ms.author: v-benbra
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.understanding
no-loc:
- Q#
- $$v
ms.openlocfilehash: 332afb4ea7de01da5d8f22fee6517032ed4f9fc1
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834985"
---
# <a name="understanding-quantum-computing"></a>Noções básicas sobre a computação quântica

A computação quântica usa os princípios da mecânica quântica para processar informações. Por isso, a computação quântica exige uma abordagem diferente da computação clássica. Um exemplo dessa diferença é o processador usado em computadores quânticos. Enquanto os computadores clássicos usam chips conhecidos à base de silício, os computadores quânticos usam sistemas quânticos, como átomos, íons, fótons ou elétrons. Eles usam suas respectivas propriedades quânticas para representar bits que podem ser preparados em diferentes superposições quânticas de 1 e 0.  

O material quântico se comporta de acordo com as leis da mecânica quântica, utilizando conceitos como computação probabilística, superposição e emaranhamento. Esses conceitos fornecem a base para algoritmos quânticos que aproveitam o poder da computação quântica para resolver problemas complexos. Este artigo descreve alguns dos conceitos essenciais da mecânica quântica na qual se baseia a computação quântica.

## <a name="a-birds-eye-view-of-quantum-mechanics"></a>Uma visão geral da mecânica quântica

A mecânica quântica, também chamada de teoria quântica, é uma ramificação da física que lida com partículas nos níveis atômico e subatômico. No entanto, no nível quântico, muitas das leis da mecânica amplamente aceitas não se aplicam. Superposição, medida quântica e emaranhamento são três fenômenos que são fundamentais para a computação quântica.  

### <a name="superposition-vs-binary-computing"></a>Superposição vs. computação binária

Imagine que você esteja fazendo exercícios físicos na sua sala de estar. Você gira todo o corpo para a esquerda e, em seguida, para a direita. Agora, você gira para a esquerda e para a direita ao mesmo tempo. Você não pode fazer isso (sem se dividir em dois, pelo menos).  Obviamente, você não pode estar nesses dois estados ao mesmo tempo; não é possível estar voltado para a esquerda e para a direita ao mesmo tempo.

No entanto, se você for uma partícula quântica, poderá haver uma certa probabilidade de estar *voltado para a esquerda* E uma certa probabilidade de estar *voltado para a direita*, devido a um fenômeno conhecido como **superposição** (também conhecido como **coerência**).

Uma partícula quântica, como um elétron, tem as próprias propriedades “voltadas para a esquerda ou para a direita”, por exemplo, o **giro**, conhecido como para cima ou para baixo, ou para tornar isso mais relacionável à computação binária clássica, digamos apenas 1 ou 0. Quando uma partícula quântica está em um estado de superposição, ela é uma combinação linear de um número infinito de estados entre 1 e 0, mas você não sabe em qual deles ela estará até que realmente a examine, o que apresenta o nosso próximo fenômeno, a **medida quântica**.

### <a name="quantum-measurement"></a>Medida quântica

Agora, digamos que o seu amigo venha até a sua casa e queira tirar uma foto de você se exercitando. É muito provável que ele obtenha uma imagem desfocada sua girando em algum ponto para a esquerda e para a direita.

Mas se você for uma partícula quântica, acontecerá uma coisa interessante. Não importa onde você esteja quando ele tirar a foto, a foto sempre mostrará você voltado para a esquerda ou para a direita (em nenhum ponto intermediário).

Isso ocorre porque o ato de observar ou de medir uma partícula quântica causa um **colapso** no estado de superposição (também conhecido como **decoerência**), e a partícula assume um estado binário clássico de 1 ou 0.

Esse estado binário é útil para nós, pois, na computação, você pode fazer muitas coisas com 1 e 0. No entanto, depois que uma partícula quântica é medida e entra em colapso, ela permanece nesse estado para sempre (assim como a sua imagem) e sempre será um 1 ou um 0. Como você verá mais adiante, na computação quântica, há operações que podem “restaurar” uma partícula para um estado de superposição, de modo que ela possa ser usada em cálculos quânticos novamente.

### <a name="entanglement"></a>Emaranhamento

Possivelmente, o fenômeno mais interessante da mecânica quântica é a capacidade de duas ou mais partículas quânticas se **emaranharem**. Quando as partículas se emaranham, elas formam um só sistema, de tal modo que o estado quântico de qualquer partícula não possa ser descrito de maneira independente do estado quântico das outras partículas. Isso significa que qualquer operação ou processo que você aplicar a uma partícula correlacionará às outras partículas também.

Além dessa interdependência, as partículas podem manter essa conexão mesmo quando estão separadas por distâncias incrivelmente grandes, até mesmo em anos-luz. Os efeitos da medida quântica também se aplicam a partículas emaranhadas, de tal modo que quando uma partícula é medida e entra em colapso, a outra partícula também entra em colapso. Como há uma correlação entre os qubits emaranhados, a medição do estado de um qubit fornece informações sobre o estado do outro qubit; essa propriedade específica é muito útil na computação quântica.

### <a name="qubits-and-probability"></a>Qubits e probabilidade

Os computadores clássicos armazenam e processam informações em bits, que podem ter um estado igual a 1 ou 0, mas nunca os dois. O equivalente na computação quântica é o **qubit**, que representa o estado de uma partícula quântica. Devido à superposição, os qubits podem ser 1 ou 0 ou qualquer valor entre os dois. Dependendo da configuração dele, um qubit tem uma certa *probabilidade* de sofrer um colapso para 1 ou 0. A probabilidade de o qubit sofrer um colapso para uma forma ou outra é determinada pela **interferência quântica**. 

Lembra-se daquele amigo que estava tirando uma foto sua? Suponha que ele tenha filtros especiais na câmera chamados filtros de *interferência*. Se ele selecionar o filtro *70/30* e começar a tirar fotos, em 70% delas, você estará voltado para a esquerda e, em 30%, estará voltado para a direita. O filtro interferiu no estado normal da câmera para influenciar a probabilidade do comportamento dela.

Da mesma forma, a interferência quântica afeta o estado de um qubit para influenciar a probabilidade de determinado resultado durante a medição. Esse estado probabilístico é o aspecto no qual se destaca a eficiência da computação quântica.

Por exemplo, com dois bits em um computador clássico, cada bit pode armazenar 1 ou 0 e, portanto, juntos, você pode armazenar quatro valores possíveis, **00**, **01**, **10** e **11**, mas apenas um deles de cada vez. Com dois qubits em superposição, no entanto, cada qubit pode ser 1 ou 0 ou *ambos*, de modo que você possa representar os mesmos quatro valores simultaneamente. Com três qubits, você pode representar oito valores; com quatro qubits, você pode representar 16 valores etc.

## <a name="summary"></a>Resumo

Esses conceitos simplesmente são a superfície da mecânica quântica, mas são conceitos fundamentalmente importantes a saber para a computação quântica.

- **Superposição**: a capacidade de as partículas quânticas serem uma combinação de todos os estados possíveis.
- **Medida quântica**: o ato de observar uma partícula quântica em superposição e resultar em um dos estados possíveis.
- **Emaranhamento**: a capacidade de as partículas quânticas correlacionarem os respectivos resultados de medição entre si.
- **Qubit**: a unidade básica de informações na computação quântica. Um qubit representa uma partícula quântica na superposição de todos os estados possíveis.
- **Interferência**: comportamento intrínseco de um qubit devido à superposição para influenciar a probabilidade de que ele entre em colapso para uma forma ou outra.

## <a name="next-steps"></a>Próximas etapas

[Computadores e simuladores quânticos](xref:microsoft.quantum.overview.simulators)
