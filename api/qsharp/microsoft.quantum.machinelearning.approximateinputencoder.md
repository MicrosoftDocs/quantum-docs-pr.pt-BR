---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Função ApproximateInputEncoder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 2e39318cfaf3321c33b08f742bb25a9276b7e660
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196592"
---
# <a name="approximateinputencoder-function"></a>Função ApproximateInputEncoder

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Dado um conjunto de coeficientes e uma tolerância, retorna uma operação de preparação de estado que prepara cada coeficiente como a amplitude correspondente de um estado de base computacional, até a tolerância determinada.

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a>Entrada

### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

A tolerância de aproximação a ser usada na codificação dos coeficientes fornecidos em um estado de entrada.


### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Os coeficientes a serem codificados em um estado de entrada.



## <a name="output--stategenerator"></a>Saída: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Uma operação de preparação de estado que prepara os coeficientes fornecidos como um estado de entrada em um determinado registro.