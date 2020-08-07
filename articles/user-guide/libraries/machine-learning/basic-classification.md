---
title: Classificação básica com a biblioteca de Machine Learning Quantum
description: Saiba como executar um classificador sequencial Quantum escrito em Q# usando a biblioteca de Machine Learning Quantum do Microsoft QDK.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: f9c3e7ab85c0f0d1a6063e593607d35c5cb76936
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868960"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a>Classificação básica: classificar dados com o QDK

Neste guia de início rápido, você aprenderá a executar um classificador sequencial Quantum escrito em Q# usando a biblioteca de Machine Learning Quantum do QDK. 

Neste guia, usaremos o conjunto de dados de meia lua, usando uma estrutura de classificador definida em Q# .

## <a name="prerequisites"></a>Pré-requisitos

- O Microsoft [Quantum development kit](xref:microsoft.quantum.install).
- Crie um Q# projeto para um [programa de host Python](xref:microsoft.quantum.install.python) ou para um [programa de host C#](xref:microsoft.quantum.install.cs).

## <a name="host-program"></a>Programa de host

O programa de host consiste em três partes:

- Carregue o conjunto de e escolha um conjunto de parâmetros iniciais para seu modelo.
- Execute o treinamento para determinar os parâmetros e a diferença do modelo.
- Validar o modelo para determinar sua exatidão

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python com Visual Studio Code ou a linha de comando](#tab/tabid-python)

    Para executar você é o Q# classificador do Python, salve o código a seguir como `host.py` . Lembre-se de que você também precisa do Q# arquivo `Training.qs` explicado posteriormente neste tutorial.

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    Em seguida, execute o programa host do Python na linha de comando:

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# com Visual Studio Code ou a linha de comando](#tab/tabid-csharp)

    Para executar você é o Q# classificador do C#, salve o código a seguir como `Host.cs` . Lembre-se de que você também precisa do Q# arquivo `Training.qs` explicado posteriormente neste tutorial.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Em seguida, execute o programa host do C# na linha de comando:

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[C# com Visual Studio 2019](#tab/tabid-vs2019)

    Para executar o novo Q# programa do C# no Visual Studio, modifique `Host.cs` para incluir o código C# a seguir. Lembre-se de que você também precisa do Q# arquivo `Training.qs` explicado posteriormente neste tutorial.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Em seguida, pressione F5. O programa iniciará a execução e uma nova janela será exibida com os seguintes resultados: 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a>\#Código do classificador Q

Agora, vejamos como as operações invocadas pelo programa de host estão definidas em Q# .
Salvamos o código a seguir em um arquivo chamado `Training.qs` .

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

As funções e operações mais importantes definidas no código acima são:

- `ClassifierStructure() : ControlledRotation[]`: nessa função, definimos a estrutura do nosso modelo de circuito adicionando as camadas das Gates controladas que consideramos. Esta etapa é análoga à declaração de camadas de neurônios em um modelo de aprendizado profundo sequencial.
- `TrainHalfMoonModel() : (Double[], Double)`: essa operação é a parte principal do código e define o treinamento. Aqui, carregamos os exemplos do conjunto de conjuntos incluído na biblioteca, definimos os parâmetros do Hyper e os parâmetros iniciais para o treinamento e iniciamos o treinamento chamando a operação `TrainSequentialClassifier` incluída na biblioteca. Ele gera os parâmetros e a tendência que determinam o classificador.
- `ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: essa operação define o processo de validação para avaliar o modelo. Aqui, carregamos os exemplos para validação, o número de medições por amostra e a tolerância. Ele gera o número de classificações incorretas no lote escolhido de amostras para validação.

## <a name="next-steps"></a>Próximas etapas

Primeiro, você pode brincar com o código e tentar alterar alguns parâmetros para ver como ele afeta o treinamento. Em seguida, no próximo tutorial, [crie seu próprio classificador](xref:microsoft.quantum.libraries.machine-learning.design), você aprenderá a definir a estrutura do classificador.
