---
uid: Microsoft.Quantum.Intrinsic.I
title: Operação I
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: I
qsharp.summary: Performs the identity operation (no-op) on a single qubit.
ms.openlocfilehash: 5aae7a5e3b5b441829de8f10f4df539ffc374954
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198938"
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