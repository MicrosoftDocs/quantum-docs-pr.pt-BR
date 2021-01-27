---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Operação AssertMeasurementProbability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830833"
---
# <a name="assertmeasurementprobability-operation"></a>Operação AssertMeasurementProbability

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


As declarações que medem o qubits determinado na base de Pauli especificada terão o resultado fornecido com a probabilidade determinada, dentro de certa tolerância.

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
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



## <a name="example"></a>Exemplo

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a>Comentários

Observe que as versões adjacente e controladas dessa operação não verificarão a condição.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Diagnostics. AssertMeasurement](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)