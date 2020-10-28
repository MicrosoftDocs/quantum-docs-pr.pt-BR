---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Operação MeasureStabilizerGenerators
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: a3f48ff24a39d13a57f7a144e21d4e41bb8a8b49
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693450"
---
# <a name="measurestabilizergenerators-operation"></a>Operação MeasureStabilizerGenerators

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Agrupa [](https://nuget.org/packages/)


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


### <a name="gadget--pauliqubit--__invalidresult__"></a>gadget: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __inválido <Result>__ 

Uma operação que especifica como medir um operador multiqubit Pauli.



## <a name="output--syndrome"></a>Saída: [síndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

O resultado de medições.

## <a name="remarks"></a>Comentários

Isso não verifica se o conjunto determinado de geradores está em comutação.
Se não estiverem em comutação, o resultado das medições poderá ser arbitrário.