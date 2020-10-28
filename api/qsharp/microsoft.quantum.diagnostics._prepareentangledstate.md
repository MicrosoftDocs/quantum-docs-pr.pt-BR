---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState operação
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 384dad5905cec50b500028e1bc352a742122b299
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693574"
---
# <a name="_prepareentangledstate-operation"></a>_prepareEntangledState operação

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Agrupa [](https://nuget.org/packages/)


Dadas dois registros, o prepara o estado de confusas máximo entre cada par de qubits nos respectivos registros.
Todos os qubits devem iniciar no estado | 0 ⟩.

O resultado é que os pares correspondentes de qubits de cada registro estão no $ \bra{\ beta_ {00} } \ket{\ beta_ {00} } $.

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="left--qubit"></a>esquerda: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Uma matriz qubit no estado $ \ket{0\cdots 0} $


### <a name="right--qubit"></a>direita: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Uma matriz qubit no estado $ \ket{0\cdots 0} $



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

