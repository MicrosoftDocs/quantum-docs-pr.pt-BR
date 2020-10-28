---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverA
title: Operação ApplyOpRepeatedlyOverA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 2e8ef7e943cfd2c0634f16566a018f386aad659f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694247"
---
# <a name="applyoprepeatedlyovera-operation"></a><span data-ttu-id="0f1d6-102">Operação ApplyOpRepeatedlyOverA</span><span class="sxs-lookup"><span data-stu-id="0f1d6-102">ApplyOpRepeatedlyOverA operation</span></span>

<span data-ttu-id="0f1d6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0f1d6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0f1d6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0f1d6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0f1d6-105">Aplica o mesmo op em um registro qubit várias vezes.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverA (op : (Qubit[] => Unit is Adj), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0f1d6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f1d6-106">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="0f1d6-107">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0f1d6-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="0f1d6-108">Uma operação a ser aplicada várias vezes no registro qubit</span><span class="sxs-lookup"><span data-stu-id="0f1d6-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="0f1d6-109">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="0f1d6-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="0f1d6-110">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="0f1d6-111">Cada matriz deve conter uma lista de ints que descreve o qubits a ser usado.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="0f1d6-112">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0f1d6-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0f1d6-113">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0f1d6-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0f1d6-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0f1d6-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0f1d6-115">See Also</span></span>

- [<span data-ttu-id="0f1d6-116">Microsoft. Quantum. Canon. ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="0f1d6-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)