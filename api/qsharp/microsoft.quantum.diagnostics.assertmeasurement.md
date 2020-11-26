---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Operação AssertMeasurement
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 3fbe000202abbd8a206b0c83dfa35f4546ea91cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202440"
---
# <a name="assertmeasurement-operation"></a>Operação AssertMeasurement

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


As declarações que medem o qubits determinado na base de Pauli especificada sempre terão o resultado especificado.

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="bases--pauli"></a>bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Um efeito de medida para declarar a probabilidade de, expresso como um operador qubit Pauli.


### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro no qual fazer a asserção.


### <a name="result--__invalidresult__"></a>resultado: __inválido <Result>__

O resultado esperado de `Measure(bases, qubits)` .


### <a name="msg--string"></a>msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Uma mensagem a ser relatada se a asserção falhar.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Observe que as versões adjacente e controladas dessa operação não verificarão a condição.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Diagnostics. AssertMeasurementProbability](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)