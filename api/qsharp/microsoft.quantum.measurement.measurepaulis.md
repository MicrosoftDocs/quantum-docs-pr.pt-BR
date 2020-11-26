---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Operação MeasurePaulis
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 4faaf78f24fa28ae5e4f701b80d9297c910b975e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194212"
---
# <a name="measurepaulis-operation"></a>Operação MeasurePaulis

Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz de operadores qubit Pauli, mede cada um deles usando um gadget de medida especificado e, em seguida, retorna a matriz de resultados.

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a>Entrada

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Matriz de operadores qubit Pauli para medir.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registre-se para medir os operadores fornecidos.


### <a name="gadget--pauliqubit--__invalidresult__"></a>gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __inválido <Result>__ 

Operação que executa a medição de um determinado operador qubit.



## <a name="output--__invalidresult__"></a>Saída: __inválido <Result>__[]

A matriz de resultados obtidos na medição de cada elemento de `paulis` on `target` .