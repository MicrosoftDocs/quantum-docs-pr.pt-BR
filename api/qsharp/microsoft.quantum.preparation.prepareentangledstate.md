---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Operação PrepareEntangledState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 299d586f7581acdecf22da2f6bbfbb8d45f372f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694949"
---
# <a name="prepareentangledstate-operation"></a>Operação PrepareEntangledState

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Agrupa [](https://nuget.org/packages/)


Entangles emparelhar dois registros de qubit.

Ou seja, dadas dois registros, o prepara o estado máximo de confusas $ \frac {1} {\sqrt {2} } \left (\ket {00} + \ket {11} \right) $ entre cada par de qubits nos respectivos registros, supondo que cada registro seja iniciado no estado $ \ket{0\cdots 0} $.

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="left--qubit"></a>esquerda: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Uma matriz qubit no estado $ \ket{0\cdots 0} $


### <a name="right--qubit"></a>direita: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Uma matriz qubit no estado $ \ket{0\cdots 0} $



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

