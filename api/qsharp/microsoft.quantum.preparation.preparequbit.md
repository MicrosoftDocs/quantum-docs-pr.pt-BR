---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Operação PrepareQubit
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  > [!WARNING]

  > PrepareQubit has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.


  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: e6a88ccf4c01b2f0a7344e3823b2748790cf9650
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854331"
---
# <a name="preparequbit-operation"></a>Operação PrepareQubit

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> PrepareQubit foi preterido. Use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> em seu lugar.

Prepara um qubit no eigenstate + 1 ( `Zero` ) do operador Pauli fornecido.
Se o operador Identity for fornecido, o qubit será preparado no estado de forma máxima mista.

Se o qubit estava inicialmente no estado $ \ket {0} $, essa operação prepara o qubit na eigenstate $ + $1 de um determinado operador Pauli, ou, para `PauliI` , no estado máximo misto em vez disso (consulte <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).

Se o qubit estava em um estado diferente de $ \ket {0} $, essa operação aplica os seguintes Gates: $H $ para `PauliX` , $HS $ para `PauliY` , $I $ para `PauliZ` e <xref:microsoft.quantum.preparation.preparesinglequbitidentity> para `PauliI` .

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a>Entrada

### <a name="basis--pauli"></a>base: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Um operador Pauli $P $.


### <a name="qubit--qubit"></a>qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um qubit a ser preparado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

