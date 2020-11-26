---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: Operação ApplyPermutationUsingTransformation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: a05b433eae2612bbf5c87522c4ef251976184aa8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192053"
---
# <a name="applypermutationusingtransformation-operation"></a>Operação ApplyPermutationUsingTransformation

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Permuta as amplitudes em um estado Quantum, considerando uma permuta usando a síntese baseada em transformação.

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Este procedimento implementa a abordagem de síntese baseada em transformação unidirecional.  A entrada é uma permutação $ \pi $ sobre $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, que representa uma função booliana $n $-Variable reversível.
O algoritmo executa iterativamente as seguintes etapas:

1. Localize o menor $x $ de forma que $x \ne \pi (x) = y $.
2. Encontre operações Toffoli com vários controle, que se aplicam às saídas, tornam $ \pi (x) = x $ e não alteram $ \pi (x ') $ para todos os $x ' < x $

## <a name="input"></a>Entrada

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma permutação de $2 ^ n $ elementos começando em 0.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Uma lista de $n $ qubits à qual a permutação é aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referências

- [*D. Michael Miller*, *Dmitri Maslov*, *Gerhard W. Dueck*, proc. Dac 2003, IEEE, pp. 318-323, 2003](https://doi.org/10.1145/775832.775915)
- [*Mathias Soeken*, *Gerhard W. Dueck*, *D. Michael Miller*, proc. rc 2016, Springer, pp. 307-321, 2016](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. síntese. ApplyPermutationUsingDecomposition](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)