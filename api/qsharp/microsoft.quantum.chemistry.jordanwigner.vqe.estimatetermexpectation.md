---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Operação EstimateTermExpectation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 7df4c1ea859140a669698434c6f8a786ea3bc2ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835662"
---
# <a name="estimatetermexpectation-operation"></a>Operação EstimateTermExpectation

Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Computa a energia associada a um determinado Jordan-Wigner termo Hamiltonian

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a>Descrição

Esta operação estima o valor de expectativa associado a cada operador de medida e o multiplica pelo coeficiente correspondente, usando a amostragem.
Os resultados são agregados em uma variável que contém a energia do termo de Jordan-Wigner.

## <a name="input"></a>Entrada

### <a name="inputstateunitary--qubit--unit--is-adj"></a>inputStateUnitary: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj

O unitário usado para preparação do estado.


### <a name="ops--pauli"></a>Ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Os operadores de medida do termo de Jordan-Wigner.


### <a name="coeffs--double"></a>coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]

Os coeficientes do termo de Jordan-Wigner.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits necessárias para simular o sistema molecular.


### <a name="nsamples--int"></a>nSamples: [int](xref:microsoft.quantum.lang-ref.int)

O número de amostras a serem usadas para a estimativa da expectativa de termo.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)

A energia associada ao termo de Jordan-Wigner.