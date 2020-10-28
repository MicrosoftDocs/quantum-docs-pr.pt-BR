---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Operação ApplyPermutationUsingDecompositionWithVariableOrder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 1edbc0a2948fdf3ae67f14b3c552676feaa7f498
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697065"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a>Operação ApplyPermutationUsingDecompositionWithVariableOrder

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Agrupa [](https://nuget.org/packages/)


Permuta as amplitudes em um estado Quantum, considerando uma permuta usando a síntese baseada em decomposição.

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Descrição

Esta operação é uma versão mais geral do @"microsoft.quantum.synthesis.applypermutationusingdecomposition" na qual a ordem variável pode ser especificada. Uma ordem variável diferente altera a sequência de decomposição e as tabelas da verdade usadas para as @"microsoft.quantum.intrinsic.x" Gates controladas.  Portanto, alterar a ordem da variável altera o número de Gates gerais usadas para concretizar a permutação.

## <a name="input"></a>Entrada

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma permutação de $2 ^ n $ elementos começando em 0.


### <a name="variableorder--int"></a>variableOrder: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma permutação de elementos $n $ começando em 0.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Uma lista de $n $ qubits à qual a permutação é aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. síntese. ApplyPermutationUsingDecomposition](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [Microsoft. Quantum. síntese. ApplyPermutationUsingTransformation](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)