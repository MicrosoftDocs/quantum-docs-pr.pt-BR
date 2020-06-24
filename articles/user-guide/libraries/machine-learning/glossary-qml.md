---
title: Biblioteca de aprendizado de máquina quântico
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 2/27/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.training
ms.openlocfilehash: f9b33a607a892179795d0700ba3080f9a24ab94a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274340"
---
# <a name="quantum-machine-learning-glossary"></a>Glossário de Machine Learning Quantum

O treinamento de um classificador de Quantum centrado em circuito é um processo com muitas partes móveis que exigem a mesma quantidade (ou um pouco maior) de calibragem por avaliação e erro como treinamento de classificadores tradicionais. Aqui, definimos os principais conceitos e ingredientes deste processo de treinamento.

## <a name="trainingtesting-schedules"></a>Agendamentos/testes de treinamento

No contexto do treinamento do classificador, uma *agenda* descreve um subconjunto de exemplos de dados em um conjunto de treinamento ou teste geral. Uma agenda geralmente é definida como uma coleção de índices de exemplo.

## <a name="parameterbias-scores"></a>Resultados de parâmetro/diferença

Dado um vetor de parâmetro candidato e uma diferença de classificador, sua *Pontuação de validação* é medida em relação a uma agenda de validação escolhida S e é expressa por um número de classificações incorretas contadas em todos os exemplos na agenda s.

## <a name="hyperparameters"></a>Hiperparâmetros

O processo de treinamento do modelo é regido por determinados valores predefinidos chamados *hiperparâmetros*:

### <a name="learning-rate"></a>Taxa de aprendizado

É um dos hiperparâmetros de chave. Ele define a quantidade atual de estimativas de gradiente estocástico impacta a atualização do parâmetro. O tamanho do Delta de atualização de parâmetro é proporcional à taxa de aprendizado. Os valores menores de taxa de aprendizagem levam à redução mais lenta de parâmetros e à convergência mais lenta, mas valores excessivamente grandes de LR podem quebrar a convergência completamente, pois o gradiente descendente nunca se compromete com um mínimo local específico. Embora a taxa de aprendizado seja ajustada adaptativamente pelo algoritmo de treinamento até certo ponto, é importante selecionar um bom valor inicial para ele. Um valor inicial padrão comum para a taxa de aprendizado é 0,1. A seleção do melhor valor da taxa de aprendizado é uma arte fina (consulte, por exemplo, a seção 4,3 de Goodfellow et al., "aprendizado profundo", MIT Press, 2017).

### <a name="minibatch-size"></a>Tamanho do minilote

Define quantas amostras de dados são usadas para uma única estimativa de gradiente estocástico. Valores maiores de tamanho de minilote geralmente levam a uma convergência mais robusta e monotônico, mas podem retardar o processo de treinamento, pois o custo de qualquer estimativa de gradiente é proporcional ao tamanho do minimatch. Um valor padrão usual para o tamanho de minilote é 10.

### <a name="training-epochs-tolerance-gridlocks"></a>Épocas de treinamento, tolerância, gridlocks

"Época" significa uma passagem completa dos dados de treinamento agendados.
O número máximo de épocas por um thread de treinamento (veja abaixo) deve ser limitado. O thread de treinamento é definido para terminar (com os melhores parâmetros candidatos conhecidos) quando o número máximo de épocas é executado. No entanto, esse treinamento será encerrado anteriormente quando a taxa de classificação insignificante na agenda de validação cair abaixo de uma tolerância escolhida. Suponha, por exemplo, que a tolerância de classificação incorreta seja 0, 1 (1%); se estiver no conjunto de validação de exemplos de 2000, estamos vendo menos de 20 classificações incorretas, o nível de tolerância foi atingido. Um thread de treinamento também será encerrado prematuramente se a pontuação de validação do modelo candidato não tiver mostrado nenhuma melhoria em várias épocas consecutivas (um engarrafamentos). A lógica para o encerramento de engarrafamentos é codificada no momento.

### <a name="measurements-count"></a>Contagem de medidas

Estimar as pontuações de treinamento/validação e os componentes do gradiente estocástico em valores de dispositivos Quantum para estimar sobreposições de estado de Quantum que exigem várias medidas das observáveis apropriadas. O número de medições deve ser dimensionado como $O (1/\ Épsilon ^ 2) $, em que $ \epsilon $ é o erro de estimativa desejado.
Como regra geral, a contagem de medidas inicial pode ser de aproximadamente US $1/\ mbox {tolerância} ^ 2 $ (consulte definição de tolerância no parágrafo anterior). Uma delas precisaria revisar a contagem de medidas para cima se o gradiente descendente parecer estar muito irregular e a convergência muito difícil de ser atingida.

### <a name="training-threads"></a>Threads de treinamento

A função de probabilidade, que é o utilitário de treinamento para o classificador, raramente é convexa, o que significa que ele geralmente tem uma infinidade de optima locais no espaço de parâmetro que pode diferir significativamente por qualidade. Como o processo SGD pode convergir para apenas um ideal, é importante explorar vários vetores de parâmetro de início. A prática comum no aprendizado de máquina é inicializar aleatoriamente esses vetores iniciais. A API de treinamento do Q # aceita uma matriz arbitrária de tais vetores de início, mas o código subjacente os explora em sequência. Em um computador de vários núcleos ou na verdade, em qualquer arquitetura de computação paralela, é aconselhável executar várias chamadas para a API de treinamento Q # em paralelo com inicializações de parâmetro diferentes nas chamadas.

#### <a name="how-to-modify-the-hyperparameters"></a>Como modificar os hiperparâmetros

Na biblioteca QML, a melhor maneira de modificar os hiperparâmetros é substituindo os valores padrão de UDT [`TrainingOptions`](xref:microsoft.quantum.machinelearning.trainingoptions) . Para fazer isso, chamamos isso de função [`DefaultTrainingOptions`](xref:microsoft.quantum.machinelearning.defaulttrainingoptions) e aplicamos o operador `w/` para substituir os valores padrão. Por exemplo, para usar medidas de 100.000 e uma taxa de aprendizagem de 0, 1:
 ```qsharp
let options = DefaultTrainingOptions()
w/ LearningRate <- 0.01
w/ NMeasurements <- 100000;
 ```
