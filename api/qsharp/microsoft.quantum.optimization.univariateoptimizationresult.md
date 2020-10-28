---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Tipo definido pelo usuário UnivariateOptimizationResult
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: c8aa91bbdc9e9e9bb4d110b470ff2041f9460a38
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696926"
---
# <a name="univariateoptimizationresult-user-defined-type"></a>Tipo definido pelo usuário UnivariateOptimizationResult

Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Agrupa [](https://nuget.org/packages/)


Representa o resultado da otimização de uma função monovariável.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>Itens nomeados

### <a name="coordinate--double"></a>Coordenada: [dupla](xref:microsoft.quantum.lang-ref.double)

Entrada na qual foi encontrado um ideal.
### <a name="value--double"></a>Valor: [duplo](xref:microsoft.quantum.lang-ref.double)

Valor retornado pela função em seu ideal.