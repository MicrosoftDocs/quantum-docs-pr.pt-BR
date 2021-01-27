---
uid: Microsoft.Quantum.Intrinsic.I
title: Operação I
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: I
qsharp.summary: Performs the identity operation (no-op) on a single qubit.
ms.openlocfilehash: 0af14a9aff20da493e95c7feba6afbb907d3d69f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849400"
---
# <a name="i-operation"></a>Operação I

Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Executa a operação de identidade (não op) em um único qubit.

```qsharp
operation I (target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Isso é não operacional. Ela é fornecida para fins de integridade e, às vezes, é útil chamar a identidade em um algoritmo ou passá-la como um parâmetro.