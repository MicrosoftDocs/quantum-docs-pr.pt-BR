---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Função MeasurementOperators
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 24d752c4f198764b6e7c6ea6c49669c020c1a502
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693652"
---
# <a name="measurementoperators-function"></a>Função MeasurementOperators

Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Agrupa [](https://nuget.org/packages/)


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