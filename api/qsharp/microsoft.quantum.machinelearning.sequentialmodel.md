---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Tipo definido pelo usuário SequentialModel
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: 3afdb8dafe0179535fe5d8c3dff668f1f3de2f7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196167"
---
# <a name="sequentialmodel-user-defined-type"></a>Tipo definido pelo usuário SequentialModel

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Descreve um modelo de classificador Quantum composto por uma sequência de rotações parametrizadas e controladas, uma atribuição de ângulos de rotação e uma tendência entre as duas classes reconhecidas pelo modelo.

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a>Itens nomeados

### <a name="structure--controlledrotation"></a>Estrutura: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

A sequência de rotações controladas usadas para classificar entradas.
### <a name="parameters--double"></a>Parâmetros: [Double](xref:microsoft.quantum.lang-ref.double)[]

Uma atribuição de ângulos de rotação para a estrutura de classificação fornecida.
### <a name="bias--double"></a>Tendência: [duplo](xref:microsoft.quantum.lang-ref.double)

A tendência entre as duas classes reconhecidas por este classificador.

## <a name="references"></a>Referências

- [arXiv:1804.00633](https://arxiv.org/abs/1804.00633)