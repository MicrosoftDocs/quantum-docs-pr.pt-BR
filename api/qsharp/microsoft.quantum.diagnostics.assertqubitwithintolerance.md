---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Operação AssertQubitWithinTolerance
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 56b7f93f33ae18146c1fb13d404fc1d119eee72e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202185"
---
# <a name="assertqubitwithintolerance-operation"></a>Operação AssertQubitWithinTolerance

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Declara que o qubit `q` está no eigenstate esperado do operador Z Pauli até uma determinada tolerância.

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>Entrada

### <a name="expected--__invalidresult__"></a>esperado: __inválido <Result>__

Em que estado o qubit deve estar: `Zero` ou `One` .


### <a name="q--qubit"></a>p: [qubit](xref:microsoft.quantum.lang-ref.qubit)

O qubit cujo estado é declarado.


### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

Tolerância na probabilidade de uma medida do qubit que retorna o resultado esperado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> permite declarar Estados qubit arbitrários em vez de apenas $Z $ eigenstates.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Diagnostics. AssertQubitIsInStateWithinTolerance](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)