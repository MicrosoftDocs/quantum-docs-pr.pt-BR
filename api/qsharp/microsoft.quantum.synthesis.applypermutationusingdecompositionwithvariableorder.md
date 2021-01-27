---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Operação ApplyPermutationUsingDecompositionWithVariableOrder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: f33d2980ff1775b1ae8d2e2e7a4fa1e5cbe7d5ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858875"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a>Operação ApplyPermutationUsingDecompositionWithVariableOrder

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Permuta as amplitudes em um estado Quantum, considerando uma permuta usando a síntese baseada em decomposição.

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
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



## <a name="example"></a>Exemplo

Para sintetizar uma `SWAP` operação:

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingDecompositionWithVariableOrder([0, 2, 1, 3], [1, 0], LittleEndian(qubits));
}
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. síntese. ApplyPermutationUsingDecomposition](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [Microsoft. Quantum. síntese. ApplyPermutationUsingTransformation](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)