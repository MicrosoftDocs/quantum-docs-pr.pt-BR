---
uid: Microsoft.Quantum.Measurement.MultiM
title: Operação de vários locais
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: 36de9dbdfc96f6e1698ee4537405f7cb74e44262
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693275"
---
# <a name="multim-operation"></a><span data-ttu-id="6192e-102">Operação de vários locais</span><span class="sxs-lookup"><span data-stu-id="6192e-102">MultiM operation</span></span>

<span data-ttu-id="6192e-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="6192e-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="6192e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6192e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6192e-105">Mede cada qubit em uma determinada matriz na base padrão.</span><span class="sxs-lookup"><span data-stu-id="6192e-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="6192e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6192e-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="6192e-107">destinos: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6192e-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6192e-108">Uma matriz de qubits a ser medida.</span><span class="sxs-lookup"><span data-stu-id="6192e-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="6192e-109">Saída: __inválido <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="6192e-109">Output : __invalid<Result>__ []</span></span>

<span data-ttu-id="6192e-110">Uma matriz de resultados de medida.</span><span class="sxs-lookup"><span data-stu-id="6192e-110">An array of measurement results.</span></span>