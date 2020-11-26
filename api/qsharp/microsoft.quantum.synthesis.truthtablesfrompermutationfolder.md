---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: Função TruthTablesFromPermutationFolder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 86e112782825303805029b2f9f6cfd9d6ce9e8b6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231017"
---
# <a name="truthtablesfrompermutationfolder-function"></a>Função TruthTablesFromPermutationFolder

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Lógica de decomposição para um único índice de variável

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a>Descrição

Isso usa o estado atual e gera uma permuta atualizada e, possivelmente, adiciona novas funções para Gates controladas.

## <a name="input"></a>Entrada

### <a name="numvars--int"></a>numVars: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="state--decompositionstate"></a>Estado: [decomposiçãostate](xref:Microsoft.Quantum.Synthesis.DecompositionState)




### <a name="index--int"></a>índice: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--decompositionstate"></a>Saída: [decomposiçãostate](xref:Microsoft.Quantum.Synthesis.DecompositionState)

