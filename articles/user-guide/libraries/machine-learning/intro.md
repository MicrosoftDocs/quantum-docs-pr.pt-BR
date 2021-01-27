---
title: Biblioteca de aprendizado de máquina quântico
description: Saiba como o Machine Learning é usado em sistemas Quantum
author: alexeib2
ms.author: alexeib
ms.date: 11/22/2019
ms.topic: conceptual
uid: microsoft.quantum.libraries.machine-learning.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: e2f4a4a63eef40474856426b3b29652b5d3053b2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854026"
---
# <a name="introduction-to-quantum-machine-learning"></a>Introdução ao Quantum Machine Learning

## <a name="framework-and-goals"></a>Estrutura e metas

A codificação de Quantum e o processamento de informações são uma alternativa poderosa para classificadores de Quantum do Machine Learning clássico. Em particular, ele nos permite codificar dados em registros Quantum que são concisos em relação ao número de recursos, empregando sistematicamente o Quantum Entanglement como recurso computacional e empregando a medição Quantum para a inferência de classes.
O classificador de Quantum centrado em circuito é uma solução Quantum relativamente simples que combina a codificação de dados com um circuito Quantum Entangling/Descomplicando a rápido seguido por medida para inferir rótulos de classe de exemplos de dados.
O objetivo é garantir a caracterização clássica e o armazenamento de circuitos de entidades, bem como treinamento híbrido/clássico de os parâmetros de circuito, mesmo para espaços de recursos muito grandes.

## <a name="classifier-architecture"></a>Arquitetura do classificador

A classificação é uma tarefa de aprendizado de máquina supervisionada, em que o objetivo é inferir rótulos de classe $ \{ y_1, y_2, \ldots, y_d \} $ de determinados exemplos de dados. O "conjunto de dados de treinamento" é uma coleção de exemplos $ \mathcal{D} = \{ (x, y)} $ com rótulos previamente atribuídos conhecidos. Aqui $x $ é um exemplo de dados e $y $ é seu rótulo conhecido chamado "rótulo de treinamento".
De um modo semelhante aos métodos tradicionais, a classificação Quantum consiste em três etapas:
- codificação de dados
- preparação de um estado de classificador
- medida devido à natureza probabilística da medida, essas três etapas devem ser repetidas várias vezes. A codificação e a computação do estado do classificador são feitas por meio de *circuitos Quantum*. Embora o circuito de codificação seja geralmente controlado por dados e sem parâmetros, o circuito do classificador contém um conjunto suficiente de parâmetros de aprendizado. 

Na solução proposta, o circuito do classificador é composto por rotações de qubit único e rotações controladas de dois qubit. Os parâmetros mais aprendiveis aqui são os ângulos de rotação. A rotação e as Gates de rotação controlada são conhecidas como *universais* para computação Quantum, o que significa que qualquer matriz de peso unitário pode ser decomposta em um circuito suficientemente longo que consiste em tais Gates.

Na versão proposta, há suporte para apenas um circuito seguido por uma única estimativa de frequência.
Portanto, a solução é uma analogia da Quantum de um computador de vetor de suporte com um kernel polinomial de baixo grau.

![Perceptron multicamada versus classificador centrado em circuito](~/media/DLvsQCC.png)

Um design de classificador Quantum simples pode ser comparado a uma solução de SVM (máquina de vetor de suporte tradicional). A inferência para um exemplo de dados $x $ no caso de SVM é feita usando uma forma de kernel ideal $ \sum \ alpha_j k (x_j, x) $, em que $k $ é uma determinada função de kernel.

Por outro lado, um classificador Quantum usa o $p de previsão (y │ x, U (\theta)) = 〈 U (\theta) x | M | U (\theta) x 〉 $, que é semelhante em espírito, mas tecnicamente muito diferente. Assim, quando uma codificação de amplitude simples é usada, $p (y │ x, U (\theta)) $ é uma forma quadrática nas amplitudes de $x $, mas os coeficientes desse formulário não são mais aprendidos de forma independente; em vez disso, eles são agregados dos elementos de matriz do circuito $U (\theta) $, que normalmente tem um número significativamente menor de parâmetros aprendiveis $ \theta $ que a dimensão do vetor $x $. O grau polinomial de $p (y │ x, U (\theta)) $ nos recursos originais pode ser aumentado para US $2 ^ l $ usando uma codificação de produto Quantum em $l $ cópias de $x $.

Nossa arquitetura explora circuitos relativamente superficiais, que, portanto, devem ser *rapidamente entanglingdos* para capturar todas as correlações entre os recursos de dados em todos os intervalos. Um exemplo do componente de circuito de Entangling rápido mais útil é mostrado na figura abaixo. Embora um circuito com essa geometria seja composto por apenas $3 n + 1 $ Gates, a matriz de peso unitário que ele calcula garante uma conversa cruzada significativa entre os recursos de $2 ^ n $.

![Entangling rapidamente o circuito Quantum em 5 qubits (com duas camadas cíclicas).](~/media/5-qubit-qccc.png)

O circuito no exemplo acima consiste em 6 Gates de qubit único $ (G_1, \ldots, G_5; G_ {16} ) $ e 10 2-qubits Gates $ (G_6, \ldots, G_ {15} ) $. Supondo que cada uma das Gates seja definida com um parâmetro que pode ser aprendiz, temos 16 parâmetros de aprendizado, enquanto a dimensão do espaço Hilbert de 5 qubit é 32. Essa geometria de circuito pode ser facilmente generalizada para qualquer registro $n $-qubit, quando $n $ é ímpar, produzindo circuitos com $3 n + 1 $ parâmetros para o espaço de recurso de $2 ^ n $-dimensional.

## <a name="classifier-training-as-a-supervised-learning-task"></a>Treinamento de classificador como uma tarefa de aprendizado supervisionada

O treinamento de um modelo classificador envolve encontrar valores ideais de seus parâmetros operacionais, de modo que eles maximizem a probabilidade média de inferir os rótulos de treinamento corretos em todos os exemplos de treinamento.
Aqui, nos preocupamos com apenas a classificação de dois níveis, ou seja, o caso de $d = $2 e apenas duas classes com os rótulos $y _1, y_2 $.

> [!NOTE]
> Uma maneira de generalizar nossos métodos para o número arbitrário de classes é substituir qubits por qudits, ou seja, unidades Quantum por Estados de base $d $ e a medida bidirecional com $d medida de $ Way.

### <a name="likelihood-as-the-training-goal"></a>Probabilidade da meta de treinamento

Dado um circuito de Quantum mais aprendiz $U (\theta) $, em que $ \theta $ é um vetor de parâmetros e denotando a medida final por $M $, a probabilidade média da inferência de rótulo correta é $ $ \begin{align} \mathcal{L} (\theta) = \frac {1} {| \mathcal{D} |} \left (\ sum_ {(x, y_1) \In\mathcal{D}} P (M = y_1 | U (\theta) x) + \ sum_ {(x, y_2) \in\mathcal{D}} P (M = y_2 | U (\theta) x) \right) \end{align} $ $ em que $P (M = y | z) $ é a probabilidade de medir $y $ no estado Quantum $z $.
Aqui, é suficiente entender que a função de probabilidade $ \mathcal{L} (\theta) $ é tranqüila em $ \theta $ e seu derivativo em qualquer $ \ theta_j $ pode ser computado, essencialmente, o mesmo protocolo Quantum usado para computar a própria função de probabilidade. Isso permite otimizar os descendentes de $ \mathcal{L} (\theta) $ por gradiente.

### <a name="classifier-bias-and-training-score"></a>Tendência do classificador e pontuação de treinamento

Dado alguns valores intermediários (ou finais) dos parâmetros em $ \theta $, precisamos identificar um único valor real $b $ conhecido como polar de *classificador* para fazer a inferência. A regra de inferência de rótulo funciona da seguinte maneira: 
- Um $x de exemplo $ recebe o rótulo $y _2 $ If e somente se $P (M = y_2 | U (\theta) x) + b > $0.05 (RULE1) (caso contrário, é atribuído o rótulo $y _1 $)

Claramente $b $ deve estar no intervalo de $ (-0,5, + 0,5) $ para ser significativo.

Um caso de treinamento $ (x, y) na \mathcal{D} $ é considerado uma *classificação* inadequado, considerando a tendência $b $ se o rótulo inferido para $x $ de acordo com RULE1 for realmente diferente do $y $. O número total de classificações incorretas é a *Pontuação de treinamento* do classificador de acordo com o $b de tendência $. A tendência de classificação *ideal* $b $ minimiza a pontuação de treinamento. É fácil ver que, considerando as estimativas de probabilidade preputadas $ \{ P (M = y_2 | U (\theta) x) | (x, *) \in\mathcal{D} \} $, a tendência de classificador ideal pode ser encontrada pela pesquisa binária no intervalo $ (-0,5, + 0,5) $ fazendo no máximo $ \ Log_2 (| \mathcal{D} |) $ Steps.

### <a name="reference"></a>Referência

Essas informações devem ser suficientes para começar a brincar com o código. No entanto, se você quiser saber mais sobre esse modelo, leia a proposta original: [ *' classificadores de Quantum centrado em circuitos ', Maria Schuld, Alex Bocharov, Krysta Svore e Nathan Wiebe*](https://arxiv.org/abs/1804.00633)

Além do exemplo de código que você verá nas próximas etapas, você também pode começar a explorar a classificação Quantum neste [tutorial](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/QuantumClassification) 
