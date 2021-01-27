---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Operação MeasureWithScratch
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 4173aa9daac08a3febdfcbf12dc236f797685436
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854651"
---
# <a name="measurewithscratch-operation"></a>Operação MeasureWithScratch

Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Mede o operador Pauli fornecido usando um qubit de rascunho explícito para executar a medição.

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a>Entrada

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Um operador qubit Pauli especificado como uma matriz de operadores de Pauli de qubit único.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit o registro a ser medido.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

O resultado da medição do operador Pauli fornecido no `target` registro.