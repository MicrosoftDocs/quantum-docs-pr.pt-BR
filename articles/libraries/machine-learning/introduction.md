---
title: Biblioteca de aprendizado de máquina Quantum
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 11/22/2019
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.introduction
ms.openlocfilehash: 4c42612fee3a58e15368677bb2c77a70c5680f45
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909782"
---
# <a name="introduction-to-quantum-machine-learning"></a>Introdução ao Quantum Machine Learning

## <a name="framework-and-goals"></a>Estrutura e metas

A codificação de Quantum e o processamento de informações são uma alternativa poderosa para classificadores de Quantum do Machine Learning clássico, em particular, codificar dados em registros Quantum que são concisos em relação ao número de recursos, empregando sistematicamente o Quantum Entanglement como recurso computacional e emprega a medição Quantum para a inferência de classes.
O classificador de Quantum centrado em circuito é uma solução Quantum relativamente simples que combina a codificação de dados com um circuito Quantum Entangling/Descomplicando a rápido seguido por medida para inferir rótulos de classe de exemplos de dados.
O objetivo é garantir a caracterização clássica e o armazenamento de circuitos de entidades, bem como treinamento híbrido/clássico de os parâmetros de circuito, mesmo para espaços de recursos muito grandes.

## <a name="classifier-architecture"></a>Arquitetura do classificador

A classificação é uma tarefa de aprendizado de máquina supervisionada, em que o objetivo é inferir rótulos de classe $\{y_1, y_2, \ldots, y_d\}$ de determinados exemplos de dados. O "conjunto de dados de treinamento" é uma coleção de exemplos $ \mathcal{D} =\{(x, y)} $ com rótulos previamente atribuídos conhecidos. Aqui $x $ é um exemplo de dados e $y $ é seu rótulo conhecido chamado "rótulo de treinamento".
De um modo semelhante aos métodos tradicionais, a classificação Quantum consiste em três etapas:
- codificação de dados
- preparação de um estado de classificador
- medida devido à natureza probabilística da medida, essas três etapas devem ser repetidas várias vezes. A medida pode ser exibida como um equivalente quântico de ativação não linear.
A codificação e a computação do estado do classificador são feitas por meio de *circuitos Quantum*. Embora o circuito de codificação seja geralmente controlado por dados e sem parâmetros, o circuito do classificador contém um conjunto suficiente de parâmetros de aprendizado. 

Na solução proposta, o circuito do classificador é composto por rotações de qubit único e rotações controladas de dois qubit. Os parâmetros mais aprendiveis aqui são os ângulos de rotação. A rotação e as Gates de rotação controlada são conhecidas como *universais* para computação Quantum, o que significa que qualquer matriz de peso unitário pode ser decomposta em um circuito suficientemente longo que consiste em tais Gates.

![Perceptron multicamada versus classificador centrado em circuito](~/media/DLvsQCC.png)

Podemos comparar esse modelo com um perceptron de várias camadas para entender melhor a estrutura básica. No Perceptron, a $p de previsão (y | x, \theta) $ é parametrizadas pelo conjunto de pesos $ \theta $ que determinam as funções lineares que conectam as funções de ativação não linear (neurônios). Esses parâmetros podem ser treinados para criar o modelo. Na camada de saída, podemos obter a probabilidade de um exemplo que pertence a uma classe usando funções de ativação não linear, como softmax. No classificador centrado no circuito, o pregnóstico é parametrizadas pelos ângulos de rotação das rotações de qubit e de dois qubit controladas do circuito de modelo. De maneira semelhante, esses parâmetros podem ser treinados por uma versão híbrida do Quantum/clássico do algoritmo descendente do gradiente. Para calcular a saída, em vez de usar funções de ativação não linear, a probabilidade da classe é obtida com a leitura de medidas repetidas em um qubit específico após as rotações controladas. Para codificar os dados clássicos em um estado Quantum, usamos um circuito de codificação controlável para preparação de estado.

Nossa arquitetura explora circuitos relativamente superficiais, que, portanto, devem ser *rapidamente entanglingdos* para capturar todas as correlações entre os recursos de dados em todos os intervalos. Um exemplo do componente de circuito de Entangling rápido mais útil é mostrado na figura abaixo. Embora um circuito com essa geometria seja composto por apenas $3 n + 1 $ Gates, a matriz de peso unitário que ele calcula garante uma conversa cruzada significativa entre os recursos de $2 ^ n $.

![Entangling rapidamente o circuito Quantum em 5 qubits (com duas camadas cíclicas).](~/media/5-qubit-qccc.png)

O circuito no exemplo acima consiste em 6 Gates de qubit único $ (G_1, \ldots, G_5; G_{16}) $ e 10 2-qubits Gates $ (G_6, \ldots, G_{15}) $. Supondo que cada uma das Gates seja definida com um parâmetro que pode ser aprendiz, temos 16 parâmetros de aprendizado, enquanto a dimensão do espaço Hilbert de 5 qubit é 32. Essa geometria de circuito pode ser facilmente generalizada para qualquer registro $n $-qubit, quando $n $ é ímpar, produzindo circuitos com $3 n + 1 $ parâmetros para o espaço de recurso de $2 ^ n $-dimensional.

## <a name="classifier-training-as-a-supervised-learning-task"></a>Treinamento de classificador como uma tarefa de aprendizado supervisionada

O treinamento de um modelo classificador envolve encontrar valores ideais de seus parâmetros operacionais, de modo que eles maximizem a probabilidade média de inferir os rótulos de treinamento corretos em todos os exemplos de treinamento.
Aqui, nos preocupamos com apenas a classificação de dois níveis, ou seja, o caso de $d = $2 e apenas duas classes com os rótulos $y _1, y_2 $.

> [!NOTE]
> Uma maneira de generalizar nossos métodos para o número arbitrário de classes é substituir qubits por qudits, ou seja, unidades Quantum por Estados de base $d $ e a medida bidirecional com $d medida de $ Way.

### <a name="likelihood-as-the-training-goal"></a>Probabilidade da meta de treinamento

Dado um circuito de Quantum mais aprendente $U (\theta) $, em que $ \theta $ é um vetor de parâmetros e denotando a medida final por $M $, a probabilidade média da inferência de rótulo correta é $ $ \begin{align} \mathcal{L} (\theta) = \frac{1}{| \mathcal{D} |} \left (\ sum_ {(x, y_1) \in\mathcal{D}} P (M = y_1 | U (\theta) x) + \ sum_ {(x, y_2) \in\mathcal{D}} P (M = y_2 | U (\theta) x) \right) \end{align} $ $ em que $P (M = y | z) $ é a probabilidade de medir $y $ no estado Quantum $z $.
Aqui, é suficiente entender que a função de probabilidade $ \mathcal{L} (\theta) $ é tranqüila em $ \theta $ e seu derivativo em qualquer $ \ theta_j $ pode ser computado, essencialmente, o mesmo protocolo Quantum usado para computar a própria função de probabilidade. Isso permite otimizar os descendentes de $ \mathcal{L} (\theta) $ por gradiente.

### <a name="classifier-bias-and-training-score"></a>Tendência do classificador e pontuação de treinamento

Dado alguns valores intermediários (ou finais) dos parâmetros em $ \theta $, precisamos identificar um único valor real $b $ conhecido como polar de *classificador* para fazer a inferência. A regra de inferência de rótulo funciona da seguinte maneira: 
- Um $x de exemplo $ recebe o rótulo $y _2 $ If e somente se $P (M = y_2 | U (\theta) x) + b > $0.05 (RULE1) (caso contrário, é atribuído o rótulo $y _1 $)

Claramente $b $ deve estar no intervalo de $ (-0,5, + 0,5) $ para ser significativo.

Um caso de treinamento $ (x, y) na \mathcal{D} $ é considerado uma *classificação* inadequado, considerando a tendência $b $ se o rótulo inferido para $x $ de acordo com RULE1 for realmente diferente do $y $. O número total de classificações incorretas é a *Pontuação de treinamento* do classificador de acordo com o $b de tendência $. A tendência de classificação *ideal* $b $ minimiza a pontuação de treinamento. É fácil ver que, considerando as estimativas de probabilidade preputadas $\{ P (M = y_2 | U (\theta) x) | (x, *) \in\mathcal{D} \}$, a tendência de classificador ideal pode ser encontrada pela pesquisa binária no intervalo $ (-0,5, + 0,5) $ fazendo no máximo $ \ log_2 (| \mathcal{D} |) $ Steps.

### <a name="reference"></a>Referência

Essas informações devem ser suficientes para começar a brincar com o código. No entanto, se você quiser saber mais sobre esse modelo, leia a proposta original: [ *' classificadores de Quantum centrado em circuitos ', Maria Schuld, Alex Bocharov, Krysta Svore e Nathan Wiebe*](https://arxiv.org/abs/1804.00633)
