---
uid: Microsoft.Quantum.Measurement.MultiM
title: Operação de vários locais
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: c39601f3e8b272b9341f1789b4c8e7230cb4182c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226988"
---
# <a name="multim-operation"></a><span data-ttu-id="961e8-102">Operação de vários locais</span><span class="sxs-lookup"><span data-stu-id="961e8-102">MultiM operation</span></span>

<span data-ttu-id="961e8-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="961e8-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="961e8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="961e8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="961e8-105">Mede cada qubit em uma determinada matriz na base padrão.</span><span class="sxs-lookup"><span data-stu-id="961e8-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="961e8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="961e8-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="961e8-107">destinos: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="961e8-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="961e8-108">Uma matriz de qubits a ser medida.</span><span class="sxs-lookup"><span data-stu-id="961e8-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="961e8-109">Saída: __inválido <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="961e8-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="961e8-110">Uma matriz de resultados de medida.</span><span class="sxs-lookup"><span data-stu-id="961e8-110">An array of measurement results.</span></span>