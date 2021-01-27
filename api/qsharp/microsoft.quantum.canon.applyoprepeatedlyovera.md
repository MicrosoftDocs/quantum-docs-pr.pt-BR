---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverA
title: Operação ApplyOpRepeatedlyOverA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 30e91d8a0292c7389ad83f14e1b7d4a8248cbb96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841614"
---
# <a name="applyoprepeatedlyovera-operation"></a><span data-ttu-id="7ab5f-102">Operação ApplyOpRepeatedlyOverA</span><span class="sxs-lookup"><span data-stu-id="7ab5f-102">ApplyOpRepeatedlyOverA operation</span></span>

<span data-ttu-id="7ab5f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7ab5f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7ab5f-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7ab5f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7ab5f-105">Aplica o mesmo op em um registro qubit várias vezes.</span><span class="sxs-lookup"><span data-stu-id="7ab5f-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverA (op : (Qubit[] => Unit is Adj), targets : Int[][], register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="7ab5f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7ab5f-106">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="7ab5f-107">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="7ab5f-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="7ab5f-108">Uma operação a ser aplicada várias vezes no registro qubit</span><span class="sxs-lookup"><span data-stu-id="7ab5f-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="7ab5f-109">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="7ab5f-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="7ab5f-110">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="7ab5f-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="7ab5f-111">Cada matriz deve conter uma lista de ints que descreve o qubits a ser usado.</span><span class="sxs-lookup"><span data-stu-id="7ab5f-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="7ab5f-112">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7ab5f-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7ab5f-113">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="7ab5f-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7ab5f-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7ab5f-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="7ab5f-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7ab5f-115">See Also</span></span>

- [<span data-ttu-id="7ab5f-116">Microsoft. Quantum. Canon. ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="7ab5f-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)