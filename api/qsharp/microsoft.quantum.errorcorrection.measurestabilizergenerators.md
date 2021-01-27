---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Operação MeasureStabilizerGenerators
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: d7c8df079e49b2ce0a5106e430ef4060df85cdc4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825767"
---
# <a name="measurestabilizergenerators-operation"></a>Operação MeasureStabilizerGenerators

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Mede o conjunto determinado de geradores de um grupo de estabilizador.

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a>Entrada

### <a name="stabilizergroup--pauli"></a>stabilizerGroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Uma matriz de operadores multiqubit Pauli.
Por exemplo, `stabilizerGroup[0]` é uma lista de matrizes de Pauli de qubit único, o produto tensor do qual é um gerador de estabilizador.


### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Uma matriz de qubits onde o código de estabilizador é definido.


### <a name="gadget--pauliqubit--__invalidresult__"></a>gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __inválido <Result>__ 

Uma operação que especifica como medir um operador multiqubit Pauli.



## <a name="output--syndrome"></a>Saída: [síndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

O resultado de medições.

## <a name="remarks"></a>Comentários

Isso não verifica se o conjunto determinado de geradores está em comutação.
Se não estiverem em comutação, o resultado das medições poderá ser arbitrário.