---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: Função QuantumROMQubitCount
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: >-
  > [!WARNING]

  > QuantumROMQubitCount has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.


  Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 0ec1e042b9f675505f73bfcdcc6706d0bc0367df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210396"
---
# <a name="quantumromqubitcount-function"></a>Função QuantumROMQubitCount

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> QuantumROMQubitCount foi preterido. Use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> em seu lugar.

Retorna o número total de qubits que devem ser alocados para a operação retornada por `QuantumROM` .

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a>Entrada

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

O erro de destino $ \epsilon $.


### <a name="ncoeffs--int"></a>nCoeffs: [int](xref:microsoft.quantum.lang-ref.int)

Número de coeficientes especificado em `QuantumROM` .



## <a name="output--intintint"></a>Saída: ([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))

## <a name="first-parameter"></a>Primeiro parâmetro

Uma tupla `(x,(y,z))` em que `x = y + z` é o número total de qubits alocadas, `y` é o número de qubits para o `LittleEndian` registro e `z` é o número de qubits de lixo.