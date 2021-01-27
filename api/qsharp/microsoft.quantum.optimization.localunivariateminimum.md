---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: Função LocalUnivariateMinimum
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: c2d094a6d0e0c7cecb249cd517995e11dff3d3b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854605"
---
# <a name="localunivariateminimum-function"></a>Função LocalUnivariateMinimum

Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna o mínimo local para uma função monovariável em um intervalo limitado, usando uma pesquisa de intervalo dourado.

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a>Entrada

### <a name="fn--double---double"></a>FN: [duplo](xref:microsoft.quantum.lang-ref.double) -> [duplo](xref:microsoft.quantum.lang-ref.double)

A função monovariável a ser minimizada.


### <a name="bounds--doubledouble"></a>limites: ([duplo](xref:microsoft.quantum.lang-ref.double),[duplo](xref:microsoft.quantum.lang-ref.double))

O intervalo no qual o mínimo local deve ser encontrado.


### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

A precisão na entrada da função a ser tolerada.
A pesquisa para optima locais continuará até que o intervalo seja menor na largura que essa tolerância.



## <a name="output--univariateoptimizationresult"></a>Saída: [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)

Um optima local da função fornecida, localizado dentro dos limites fornecidos.