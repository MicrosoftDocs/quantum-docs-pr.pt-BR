---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Operação MeasureIdentity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: f8cf5975ac9407e8c532ace08455a41d3c08d6f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851819"
---
# <a name="measureidentity-operation"></a>Operação MeasureIdentity

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Mede o operador de identidade em um registro de qubits.

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a>Entrada

### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

O registro a ser medido.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

O valor do resultado `Zero` .

## <a name="remarks"></a>Comentários

Como $ \boldone $ tem apenas o eigenvalue $1 $ e não tem um eigenvalue negativo, essa operação sempre retorna `Zero` , correspondendo a eigenvalue $ + 1 = (-1) ^ 0 $ e não causa um recolhimento do estado de `register` .

Por si só, essa operação não é útil, mas é útil no contexto do processo tomography, pois fornece informações sobre a preservação de rastreamento de um processo Quantum.
Em particular, um computador de destino com medição de perdas deve substituir essa operação por uma medida real de $ \boldone $.