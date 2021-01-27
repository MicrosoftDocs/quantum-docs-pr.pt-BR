---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Operação ApplyPauliFromBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: e0edd8420127339116e525421ba23e246dcf0a45
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841585"
---
# <a name="applypaulifrombitstring-operation"></a>Operação ApplyPauliFromBitString

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica um operador Pauli em cada qubit em uma matriz se o bit correspondente de uma matriz booliana corresponde a uma determinada entrada.

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Operador Pauli a ser aplicado a `qubits[idx]` Where `bitsApply == bits[idx]`


### <a name="bitapply--bool"></a>bitApply: [bool](xref:microsoft.quantum.lang-ref.bool)

aplicar Pauli se bit for esse valor


### <a name="bits--bool"></a>bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Registro booliano que especifica quais qubit correspondentes no `qubits` devem ser operados em


### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Quantum registra-se para aplicar seletivamente o operador Pauli especificado



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

A matriz booliana e o registro do Quantum devem ser de comprimento igual.