---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: Operação ApplyPermutationUsingDecomposition
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 40b51807da155c57c3fa8d740eff28ceef0a0ffc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697068"
---
# <a name="applypermutationusingdecomposition-operation"></a>Operação ApplyPermutationUsingDecomposition

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Agrupa [](https://nuget.org/packages/)


Permuta as amplitudes em um estado Quantum, considerando uma permuta usando a síntese baseada em decomposição.

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Descrição

Esse procedimento implementa a abordagem de síntese baseada em decomposição.  A entrada é uma permutação $ \pi $ sobre $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, que representa uma função booliana $n $-Variable reversível.
O algoritmo executa iterativamente as seguintes etapas para cada índice variável $i $:

1. Compute $ ((\ pi_l, \ pi_r), \pi ') $ de forma que as imagens de $ \ pi_l $ e $ \ pi_r $ não alterem bits em seus elementos em índices diferentes de $i $ e imagens de $ \pi ' $ não alterar bit $i $ em seus elementos.
2. Defina $ \pi \leftarrow \pi ' $ ' e derive as tabelas da verdade de $ \ pi_l $ e $ \ pi_r $ com base em elementos que não são pontos fixos.

Depois de aplicar essas etapas para todos os índices de variáveis, a permutação restante $ \pi $ será a identidade e, com base nas tabelas e índices da verdade coletados, uma poderá aplicar as operações controladas de verdade @"microsoft.quantum.intrinsic.x" da tabela usando a @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" operação.

A ordem da variável é $0, \dots, n-$1.  Uma ordem de variável personalizada pode ser especificada na operação @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .

## <a name="input"></a>Entrada

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma permutação de $2 ^ n $ elementos começando em 0.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Uma lista de $n $ qubits à qual a permutação é aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referências

- [*Alexis de vos* , *Yvan Van Rentergem* , avçd. in Math. de comm. 2 (2), 2008, pp. 183--200](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [*Mathias Soeken* , *Laura Tague* , *Gerhard W. Dueck* , *Rolf Drechsler* , diário de computação simbólica 73 (2016), pp. 1--26](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. síntese. ApplyPermutationUsingDecompositionWithVariableOrder](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [Microsoft. Quantum. síntese. ApplyPermutationUsingTransformation](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)