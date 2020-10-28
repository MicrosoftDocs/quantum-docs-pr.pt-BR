---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Operação AssertMeasurementProbability
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: ff0419706d825442492f82e564f1cce86f1b112f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693552"
---
# <a name="assertmeasurementprobability-operation"></a>Operação AssertMeasurementProbability

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Agrupa [](https://nuget.org/packages/)


As declarações que medem o qubits determinado na base de Pauli especificada terão o resultado fornecido com a probabilidade determinada, dentro de certa tolerância.

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit
```


## <a name="input"></a>Entrada

### <a name="bases--pauli"></a>bases: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Um efeito de medida para declarar a probabilidade de, expresso como um operador qubit Pauli.


### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro no qual fazer a asserção.


### <a name="result--__invalidresult__"></a>resultado: __inválido <Result>__

Um resultado esperado de `Measure(bases, qubits)` .


### <a name="prob--double"></a>prob: [duplo](xref:microsoft.quantum.lang-ref.double)

A probabilidade com a qual o resultado especificado é esperado.


### <a name="msg--string"></a>msg: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Uma mensagem a ser relatada se a asserção falhar.


### <a name="tol--double"></a>a: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Observe que as versões adjacente e controladas dessa operação não verificarão a condição.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Diagnostics. AssertMeasurement](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)