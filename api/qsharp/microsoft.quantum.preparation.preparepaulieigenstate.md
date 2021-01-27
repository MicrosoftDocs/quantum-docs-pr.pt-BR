---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: Operação PreparePauliEigenstate
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: 473bb2fa4429a14f69bcae4573354aad87dc37df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854349"
---
# <a name="preparepaulieigenstate-operation"></a>Operação PreparePauliEigenstate

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Prepara um qubit no eigenstate positivo de um determinado operador Pauli.
Se o operador Identity for fornecido, o qubit será preparado no estado de forma máxima mista.

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a>Descrição

Se o qubit estava inicialmente no estado $ \ket {0} $, essa operação prepara o qubit na eigenstate $ + $1 de um determinado operador Pauli, ou, para `PauliI` , no estado máximo misto em vez disso (consulte <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).

Se o qubit estava em um estado diferente de $ \ket {0} $, essa operação aplica os seguintes Gates: $H $ para `PauliX` , $HS $ para `PauliY` , $I $ para `PauliZ` e <xref:microsoft.quantum.preparation.preparesinglequbitidentity> para `PauliI` .

## <a name="input"></a>Entrada

### <a name="basis--pauli"></a>base: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Um operador Pauli $P $.


### <a name="qubit--qubit"></a>qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um qubit a ser preparado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Exemplo

Para preparar um qubit no estado $ \ket{+} $:

```qsharp
using (q = Qubit()) {
    PreparePauliEigenstate(PauliX, qubit);
    // ...
}
```