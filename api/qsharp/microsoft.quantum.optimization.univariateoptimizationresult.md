---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Tipo definido pelo usuário UnivariateOptimizationResult
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194025"
---
# <a name="univariateoptimizationresult-user-defined-type"></a>Tipo definido pelo usuário UnivariateOptimizationResult

Namespace: [Microsoft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa o resultado da otimização de uma função monovariável.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>Itens nomeados

### <a name="coordinate--double"></a>Coordenada: [dupla](xref:microsoft.quantum.lang-ref.double)

Entrada na qual foi encontrado um ideal.
### <a name="value--double"></a>Valor: [duplo](xref:microsoft.quantum.lang-ref.double)

Valor retornado pela função em seu ideal.