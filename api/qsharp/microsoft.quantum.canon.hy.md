---
uid: Microsoft.Quantum.Canon.HY
title: Operação hipótese
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: HY
qsharp.summary: >-
  Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.

  The Y Hadamard transformation $H_Y = S H$ on a single qubit is:

  \begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}. \end{align}
ms.openlocfilehash: bc3417ff948b718be5b96513f30f3e2714b9e20c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694004"
---
# <a name="hy-operation"></a><span data-ttu-id="12de2-102">Operação hipótese</span><span class="sxs-lookup"><span data-stu-id="12de2-102">HY operation</span></span>

<span data-ttu-id="12de2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="12de2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="12de2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12de2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12de2-105">Aplica o analógico Y à transformação Hadamard que troca os eixos Z e Y.</span><span class="sxs-lookup"><span data-stu-id="12de2-105">Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.</span></span>

<span data-ttu-id="12de2-106">A transformação Y Hadamard $H _Y = S H $ em um único qubit é:</span><span class="sxs-lookup"><span data-stu-id="12de2-106">The Y Hadamard transformation $H_Y = S H$ on a single qubit is:</span></span>

<span data-ttu-id="12de2-107">\begin{align} H_Y \mathrel{: =} \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ i &-i \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="12de2-107">\begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}.</span></span>
<span data-ttu-id="12de2-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="12de2-108">\end{align}</span></span>

```qsharp
operation HY (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="12de2-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="12de2-109">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="12de2-110">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="12de2-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="12de2-111">Qubit ao qual a portão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="12de2-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12de2-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12de2-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="12de2-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="12de2-113">See Also</span></span>

- [<span data-ttu-id="12de2-114">Microsoft. Quantum. intrínseca. H</span><span class="sxs-lookup"><span data-stu-id="12de2-114">Microsoft.Quantum.Intrinsic.H</span></span>](xref:Microsoft.Quantum.Intrinsic.H)