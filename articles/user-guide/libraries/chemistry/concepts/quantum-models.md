---
title: Modelos de Quantum para sistemas eletrônicos
description: Saiba como os sistemas eletrônicos do molecular são simulados usando a modelagem Quantum.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.quantummodels
no-loc:
- Q#
- $$v
ms.openlocfilehash: f6b652ef3e315ded5b4e39fd65a2f6be7070d7fa
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869470"
---
# <a name="quantum-models-for-electronic-systems"></a>Modelos de Quantum para sistemas eletrônicos

Para simular sistemas eletrônicos, precisamos primeiro começar especificando o Hamiltonian, que pode ser encontrado pelo procedimento de quantificação canônica descrito acima.
Especificamente, para $N _e $ elétrons com o nuclei de tempo $p _i $ (em três dimensões) e em massa $m _E $ e os vetores de posição $x _i $ juntamente com com encargos $Z _k e $ em posições $y _k $, o operador Hamiltonian lê \begin{Equation} \hat{H} = \sum \_ {i = 1} ^ {N \_ e} \frac{\hat{p} \_ i ^ 2} {2m \_ e} + \frac {1} {2} \sum \_ {i\ne j} \frac{e ^ 2} {| \hat{x} \_ i-\hat{x} \_ j |}-\sum \_ {i, k} \frac{Z \_ ke ^ 2} {| \hat{x} \_ i-{y} \_ k |} + \frac {1} {2} \ sum_ {k\ne k '} \frac{Z \_ KZ \_ {k '} e ^ 2} {| y \_ k-y \_ k ' |}. \label{EQ: Ham} \end{Equation} os operadores de tempo $ \hat{p} \_ i ^ 2 $ podem ser exibidos em espaço real como operadores laplaciana, ou seja, $ \hat{p} \_ i ^ 2 =-\partial \_ {x \_ i} ^ 2-\partial \_ {y \_ i} ^ 2-\partial \_ {z \_ i} ^ 2 $.
Aqui, fizemos a suposição de simplificação de que os nuclei estão em repouso para o molécula.
Isso é conhecido como a aproximação de Oppenheimer e tende a ser válido para o espectro de energia de baixa energia de $ \hat{H} $, já que a massa de US $1/1836 $ é a massa de um Proton.
Esse operador Hamiltonian pode ser facilmente encontrado escrevendo a energia de um sistema de $N \_ e $ elétrons e aplicando o processo de quantificação canônica descrito no [Quantum Dynamics](xref:microsoft.quantum.chemistry.concepts.quantumdynamics).

Para construir a representação de matriz unitário para $e ^ {-i\hat {H} t} $, precisamos representar o operador $ \hat{H} $ como uma matriz.
Para isso, precisamos escolher um sistema de coordenadas ou base para representar o problema no.
Por exemplo, se $ \ psi_j $ são um conjunto de funções de base ortogonal para a $N _e $ elétrons, podemos definir a matriz

\begin{Equation} H \_ {i, j} = \int \_ {-\infty} ^ \infty\int \_ {-\infty} ^ \infty \psi ^ { \* } \_ i (x \_ 1) \hat{H} \psi \_ j (x \_ 2) \dd ^ 3x \_ 1 \dd ^ 3x \_ 2. \ Label {EQ: discreteHam} \end{Equation}

Embora, em princípio, o operador $ \hat{H} $ seja desassociado e não atue em um espaço dimensional finito, a matriz com elementos $H \_ \{ i, j \} $ acima.
Isso significa que os erros são incorridos por meio da escolha de um conjunto de base muito pequeno; no entanto, escolher uma base grande pode tornar a simulação do dinâmica de química impraticável.
Por esse motivo, escolher uma base que possa representar de forma concisa o problema é vital para resolver o problema da estrutura eletrônica.

Há muitas bases apropriadas que podem ser usadas e a escolha de uma boa base para se ajustar ao problema é grande parte da arte do quantum química.
Talvez os conjuntos de base mais simples sejam ARM (Slater-tipo-órbitas), que são soluções (ortogonaled) para a equação Schrödinger (ou seja, eigenfunctions de $ \hat{H} $) para Atoms semelhantes a Hydrogen.
Outros conjuntos de base, como planos-ondas ou órbitas de espaço real, podem ser usados e, para obter mais detalhes, nos referimos ao leitor curioso ao texto padrão [' molecular Electronic-Structure teoria '](https://onlinelibrary.wiley.com/doi/book/10.1002/9781119019572) por Helgaker.

Embora os Estados usados no modelo acima possam parecer arbitrários, as restrições de locais da Quantum quântico nos Estados que podem ser encontrados por natureza.
Em particular, todos os Estados de Quantum eletrônico válidos devem ser antisimétrico em troca de rótulos de emails eletrônicos.
Isso significa que, se $ \psi (x_1, x_2) $ fosse a função de onda para o estado de Quantum conjunta de dois elétrons, deve haver $ $ \psi (x_1, x_2) =-\psi (x_2, x_1).
$ $ O princípio de exclusão de Pauli que proíbe que dois elétrons estejam no mesmo estado de Quantum é, fascinantemente, uma consequência direta dessa lei, pois pode ser Intuit do fato de que se trocarmos duas elétrons localizadas na mesma posição $ \psi (x_1, x_1) \mapsto \psi (x_1, x_1) \ne-\psi (x_1, x_1) $ a menos que $ \psi (x_1 , x_1) = 0 $.
Portanto, os Estados iniciais devem ser escolhidos para obedecer a essa propriedade antisimetria e, por sua vez, nunca têm dois elétrons no mesmo estado ao mesmo tempo.
Isso é crucial para a estrutura eletrônica porque ele proíbe que vários elétrons estejam no mesmo estado e, por sua vez, permite que os computadores Quantum usem um único bit de Quantum para armazenar o número de elétrons em um determinado estado de Quantum.

Embora a mecânica quantum possa ser simulada em um computador Quantum por discretização esses Estados, a maior parte do trabalho no campo tem eschewed essa abordagem porque ela requer muitas qubits para armazenar os Estados e precisa de um procedimento de preparação de estado complicado para preparar um estado inicial antisimétrico.
Felizmente, no entanto, esses problemas podem ser sidesteppeddos exibindo o problema de simulação de uma perspectiva diferente.
