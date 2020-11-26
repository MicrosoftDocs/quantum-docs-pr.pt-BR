---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Operação MeasureIdentity
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 4a169355d0669c67f0eb14c80e8554b2f24b035a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216108"
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