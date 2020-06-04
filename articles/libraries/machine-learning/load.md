---
title: Carregando dados clássicos
description: Saiba como carregar seu próprio conjunto de informações para treinar um modelo de classificação com o Microsoft Quantum Development Kit (QDK).
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.load
ms.openlocfilehash: efa4a65a489446cbef48507d0b02a932da74c71c
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327655"
---
# <a name="load-and-classify-your-own-datasets"></a>Carregar e classificar seus próprios conjuntos de valores

Neste breve tutorial, vamos aprender como carregar seu próprio conjunto de informações para treinar um modelo classificador com o kit de desenvolvimento Quantum (QDK).

É altamente recomendável o uso de um formato de serialização padronizado, como [arquivos JSON](https://en.wikipedia.org/wiki/JSON) , para armazenar seus dados.
Esses formatos oferecem alta compatibilidade com estruturas diferentes, como Python e o ecossistema .NET.
Em particular, é recomendável usar nosso modelo para carregar os dados, para que você possa copiar e colar o código diretamente dos exemplos.

## <a name="template-for-loading-your-datasets"></a>Modelo para carregar seus conjuntos de valores

Suponha que tenhamos um conjunto de recursos de treinamento $ (x, y) $ de Size $N = $2, em que cada instância $x _i $ of $x $ tem três recursos: $x _ {I1} $, $x _ {I2} $ e $x _ {i3} $.
O conjunto de dados de validação tem a mesma estrutura.
Esses conjuntos podem ser representados por um `data.json` arquivo semelhante ao seguinte:

```json
{
    "TrainingData": {
        "Features": [
            [
                x_11,
                x_12,
                x_13
            ],
            [
                x_21,
                x_22,
                x_23
            ]
        ],
        "Labels": [
            y_1,
            y_2
        ]
    },
    "ValidationData": {
        "Features": [
            [
                xv_11,
                xv_12,
                xv_13
            ],
            [
                xv_11,
                xv_12,
                xv_13
            ]
        ],
        "Labels": [
            yv_1,
            yv_2
        ]
    }
}
```

### <a name="example-using-the-template"></a>Exemplo usando o modelo

Suponha que tenhamos um pequeno conjunto de pequenos com as alturas e os pesos de diferentes gatos e cachorros. Esse conjunto de espaço de os é muito pequeno para treinar um modelo, mas será suficiente para mostrar o processo de carregamento de um conjunto de um DataSet.

| Altura (m) | Peso (kg) | Animal |
|-----------|------------|--------|
| 0,54      | 30         | Auto    |
| 0,30      | 8          | Cat    |
| 0.91      | 44         | Auto    |
| 0.86      | 31          | Auto    |
| 0,32      | 5         | Cat    |
| 0.25      | 4          | Cat    |

O processo é:

- Primeiro, precisamos separar o DataSet em treinamento e validação. Nesse caso, podemos apenas usar os três primeiros exemplos para treinamento e o restante dos exemplos para validação. Em geral, é uma boa prática para fazer amostras aleatoriamente do conjunto de dados de treinamento e validação para evitar dipolaridades indesejadas no dado de treinamento.
- Em segundo lugar, precisamos atribuir um rótulo numérico a cada classe. Observe que, por enquanto, a biblioteca QML admite apenas problemas de classificação binária. Portanto, atribuíremos o rótulo 0 à classe `Dog` e o número 1 à classe `Cat` .
- Por fim, preenchemos o modelo usando os dados do nosso conjunto. Observe que, para conjuntos de grandes DataSets, você deve criar um pequeno script para gerar automaticamente o modelo de seu conjunto de informações específico. Esse script dependerá do formato original do conjunto de seus conjuntos de seus.

Para nosso conjunto de nossos, o `data.json` arquivo é:

```json
{
    "TrainingData": {
        "Features": [
            [
                0.54,
                30
            ],
            [
                0.30,
                8
            ],
            [
                0.91,
                44
            ]
        ],
        "Labels": [
            0,
            1,
            0
        ]
    },
    "ValidationData": {
        "Features": [
            [
                0.86,
                31
            ],
            [
                0.32,
                5
            ]
            [
                0.25,
                4
            ]
        ],
        "Labels": [
            0,
            1,
            1
        ]
    }
}

```

## <a name="loading-the-data"></a>Carregando os dados

Depois que os dados forem serializados como um arquivo JSON, você poderá carregá-los usando as bibliotecas JSON fornecidas com o idioma do host escolhido.

### <a name="python"></a>[Python](#tab/tabid-python)

O Python fornece o [ `json` pacote interno](https://docs.python.org/3.7/library/json.html) para trabalhar com dados serializados em JSON:

:::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="4-5,20-22":::

### <a name="c"></a>[C#](#tab/tabid-csharp)

A plataforma .NET Core fornece o [ `System.Text.Json` pacote](https://www.nuget.org/packages/System.Text.Json) para trabalhar com dados serializados em JSON:

:::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="10,64-82":::

***

## <a name="next-steps"></a>Próximas etapas

Agora você está pronto para começar a executar seus próprios experimentos com seus próprios conjuntos de valores. Experimente classificadores e conjuntos de resultados diferentes e contribua para a Comunidade que está compartilhando seu resultado!
