---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Tipo definido pelo usuário UnivariateOptimizationResult
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: cc54c0035796aac86482e8a3a6896ceb197c7cfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854580"
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