---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Operação MeasureAllZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: cb3c7cab33efb612bbf5da3b51d2df5d1b8ba1df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854666"
---
# <a name="measureallz-operation"></a>Operação MeasureAllZ

Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Mede em conjunto um registro de qubits na base do Pauli Z.

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a>Descrição

Mede um registro de qubits no $Z \otimes Z \otimes \cdots \otimes Z $, representando a paridade de todo o registro.

## <a name="input"></a>Entrada

### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

O registro a ser medido.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

O resultado da medição de $Z \otimes Z \otimes \cdots \otimes Z $.