---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverC
title: Operação ApplyOpRepeatedlyOverC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverC
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: effd61e6c012dcf81a83383c3fd43cf745d18117
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694245"
---
# <a name="applyoprepeatedlyoverc-operation"></a><span data-ttu-id="32724-102">Operação ApplyOpRepeatedlyOverC</span><span class="sxs-lookup"><span data-stu-id="32724-102">ApplyOpRepeatedlyOverC operation</span></span>

<span data-ttu-id="32724-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="32724-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="32724-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="32724-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="32724-105">Aplica o mesmo op em um registro qubit várias vezes.</span><span class="sxs-lookup"><span data-stu-id="32724-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverC (op : (Qubit[] => Unit is Ctl), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="32724-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="32724-106">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="32724-107">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="32724-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="32724-108">Uma operação a ser aplicada várias vezes no registro qubit</span><span class="sxs-lookup"><span data-stu-id="32724-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="32724-109">destinos: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="32724-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="32724-110">Matrizes aninhadas que descrevem os destinos da operação.</span><span class="sxs-lookup"><span data-stu-id="32724-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="32724-111">Cada matriz deve conter uma lista de ints que descreve o qubits a ser usado.</span><span class="sxs-lookup"><span data-stu-id="32724-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="32724-112">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="32724-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="32724-113">Qubit registrar-se para ser tratado.</span><span class="sxs-lookup"><span data-stu-id="32724-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="32724-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="32724-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="32724-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="32724-115">See Also</span></span>

- [<span data-ttu-id="32724-116">Microsoft. Quantum. Canon. ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="32724-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)