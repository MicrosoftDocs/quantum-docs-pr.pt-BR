---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedGeneratorSystem
title: Função JWOptimizedGeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 321b58ba4a458ad53579d2480258a92ba48de169
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225696"
---
# <a name="jwoptimizedgeneratorsystem-function"></a>Função JWOptimizedGeneratorSystem

Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)

Pacote: [Microsoft. Quantum. Research. química](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Converte um Hamiltonian descrito por `JWOptimizedHTerms` para um `GeneratorSystem` expresso em termos da `GeneratorIndex` Convenção definida neste arquivo.

```qsharp
function JWOptimizedGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Entrada

### <a name="data--jwoptimizedhterms"></a>dados: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)

Descrição de Hamiltonian no `JWOptimizedHTerms` formato.



## <a name="output--generatorsystem"></a>Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Representação de Hamiltonian como `GeneratorSystem` .