---
uid: Microsoft.Quantum.Simulation.Unitary
title: Tipo definido pelo usuário unitário
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: Unitary
qsharp.summary: Represents evolution under a unitary operator.
ms.openlocfilehash: c34d84fb5f319c285356b284bd1f1c18ec64ef46
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192138"
---
# <a name="unitary-user-defined-type"></a><span data-ttu-id="eb44c-102">Tipo definido pelo usuário unitário</span><span class="sxs-lookup"><span data-stu-id="eb44c-102">Unitary user defined type</span></span>

<span data-ttu-id="eb44c-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="eb44c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="eb44c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eb44c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eb44c-105">Representa a evolução em um operador unitário.</span><span class="sxs-lookup"><span data-stu-id="eb44c-105">Represents evolution under a unitary operator.</span></span>

```qsharp

newtype Unitary = ((Qubit[] => Unit is Adj + Ctl));
```

