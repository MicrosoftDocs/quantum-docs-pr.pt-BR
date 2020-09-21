---
title: Criar seu próprio classificador com o QDK
description: Conheça os conceitos básicos da criação de modelos de circuito para o classificador de circuito do Quantum.
author: geduardo
ms.author: v-edsanc
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3515279dd4d03b2a512035af0b13e084dd91f9dc
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835699"
---
# <a name="design-your-own-classifier"></a>Criar seu classificador

Neste guia, você aprenderá os conceitos básicos por trás do design de modelos de circuito para o classificador centrado no circuito Quantum.

Como no aprendizado profundo clássico, não há nenhuma regra geral para escolher uma arquitetura específica. Dependendo do problema, algumas arquiteturas terão um desempenho melhor do que outras. Mas, há alguns conceitos que podem ser úteis ao criar o circuito:

- Um grande número de parâmetros implica um modelo mais flexível, que pode ser adequado para desenhar limites de classificação complicados, mas que também podem ser mais suscetíveis a sobreajuste.

- Entangling Gates entre qubits são essenciais para capturar as correlações entre os recursos do Quantum.

## <a name="how-to-build-a-classifier-with-q"></a>Como criar um classificador com Q\#

Para criar um classificador, vamos concatenar as rotações controladas pelo parametrizadas em nosso modelo de circuito. Para fazer isso, podemos usar o tipo [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) definido na biblioteca de Machine Learning Quantum. Esse tipo aceita quatro argumentos que determinam: o índice do qubit de destino, a matriz de índices do controle qubits, o eixo de rotação e o índice do parâmetro associado na matriz de parâmetros que definem o modelo.

Vejamos um exemplo de classificador. No [exemplo de meia lua](https://github.com/microsoft/Quantum/tree/main/samples/machine-learning/half-moons), podemos encontrar o classificador a seguir definido no arquivo `Training.qs` .

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

O que estamos definindo aqui é uma função que retorna uma matriz de `ControlledRotation` elementos, que junto com uma matriz de parâmetros e uma tendência definirão nosso [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel) . Esse tipo é fundamental na biblioteca de Machine Learning Quantum e define o classificador. O circuito definido na função acima faz parte de um classificador no qual cada amostra do conjunto de um contém dois recursos. Portanto, precisamos apenas de dois qubits. A representação gráfica do circuito é:

 ![Exemplo de modelo de circuito](~/media/circuit_model_1.PNG)

Observe que, por padrão, as operações da biblioteca Quantum Machine Learning medem a última qubit do registro para estimar as probabilidades de classificação. Você deve ter em mente esse fato ao projetar seu circuito.

## <a name="use-the-library-functions-to-write-layers-of-gates"></a>Usar as funções de biblioteca para gravar camadas de Gates

Suponha que tenhamos um DataSet com 784 recursos por instância, por exemplo, imagens de 28 × 28 pixels, como o conjunto de MNIST. Nesse caso, a largura do circuito se torna grande o suficiente para que a gravação manual de cada portão se torne uma tarefa possível, mas impraticável. É por isso que a biblioteca de Machine Learning Quantum fornece um conjunto de ferramentas para gerar automaticamente camadas de rotações de parametrizadas. Por exemplo, a função [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) retorna uma matriz de rotações de qubit simples não controladas ao longo de um determinado eixo, com uma rotação para cada qubit no registro, cada parametrizadas por um parâmetro de modelo diferente. Por exemplo, `LocalRotationsLayer(4, X)` retorna o seguinte conjunto de Gates:

 ![Camada de rotações locais](~/media/local_rotations_layer.PNG)

Recomendamos que você explore a [referência de API da biblioteca de Machine Learning Quantum](xref:microsoft.quantum.machinelearning) para descobrir todas as ferramentas disponíveis para simplificar o design do circuito.

## <a name="next-steps"></a>Próximas etapas

 Experimente estruturas diferentes nos exemplos fornecidos pelos exemplos. Você vê as alterações no desempenho do modelo? No próximo tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load) você aprenderá a carregar conjuntos de valores para experimentar e explorar novas arquiteturas de classificadores.
