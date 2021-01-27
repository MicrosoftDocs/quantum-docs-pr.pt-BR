---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Função MeasurementOperators
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 204ae621b77559a894f0bce14e494824d58e4ad6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835392"
---
# <a name="measurementoperators-function"></a>Função MeasurementOperators

Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Computa todos os operadores de medida necessários para computar a expectativa de um termo de Jordan-Wigner.

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a>Entrada

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits necessárias para simular o sistema molecular.


### <a name="indices--int"></a>índices: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz que contém os índices do qubit cada operador Pauli é aplicado a.


### <a name="termtype--int"></a>termtype: [int](xref:microsoft.quantum.lang-ref.int)

O tipo do termo de Jordan-Wigner.



## <a name="output--pauli"></a>Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Uma matriz de operadores de medida (cada um sendo uma matriz de Pauli).