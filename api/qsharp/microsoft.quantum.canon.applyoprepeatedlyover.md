---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver
title: Operação ApplyOpRepeatedlyOver
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOver
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 09f54be33a7b5c58a317a949290f5cd6d54fe841
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694248"
---
# <a name="applyoprepeatedlyover-operation"></a><span data-ttu-id="0de8c-102">Operação ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="0de8c-102">ApplyOpRepeatedlyOver operation</span></span>

<span data-ttu-id="0de8c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0de8c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0de8c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0de8c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0de8c-105">Aplica o mesmo op em um registro qubit várias vezes.</span><span class="sxs-lookup"><span data-stu-id="0de8c-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOver (op : (Qubit[] => Unit), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0de8c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0de8c-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="0de8c-107">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="0de8c-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0de8c-108">Uma operação a ser aplicada várias vezes no registro qubit</span><span class="sxs-lookup"><span data-stu-id="0de8c-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="0de8c-109">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="0de8c-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="0de8c-110">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="0de8c-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="0de8c-111">Cada matriz deve conter uma lista de ints que descreve o qubits a ser usado.</span><span class="sxs-lookup"><span data-stu-id="0de8c-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="0de8c-112">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0de8c-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0de8c-113">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="0de8c-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0de8c-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0de8c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0de8c-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0de8c-115">See Also</span></span>

- [<span data-ttu-id="0de8c-116">Microsoft. Quantum. Canon. ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="0de8c-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)