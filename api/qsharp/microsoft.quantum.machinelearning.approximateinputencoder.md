---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Função ApproximateInputEncoder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 035c353c34362aa3486a7df9e7bb1bc95a6f63be
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856171"
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