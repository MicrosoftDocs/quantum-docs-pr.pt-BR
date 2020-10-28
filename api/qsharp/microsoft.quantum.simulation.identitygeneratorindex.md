---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Função IdentityGeneratorIndex
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: d2af2dafaf75a68546cb3f16c04cf4c7ee50c6ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696957"
---
# <a name="identitygeneratorindex-function"></a>Função IdentityGeneratorIndex

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Agrupa [](https://nuget.org/packages/)


Retorna um índice de gerador consistente com o zero Hamiltonian, `H = 0` , que corresponde à operação de evolução da identidade.

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Entrada

### <a name="idxterm--int"></a>idxTerm: [int](xref:microsoft.quantum.lang-ref.int)

Essa entrada é ignorada e é definida para consistência com o <xref:microsoft.quantum.simulation.generatorsystem> tipo definido pelo usuário.



## <a name="output--generatorindex"></a>Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Um índice de gerador que representa a evolução sob o Hamiltonian $H = $0.