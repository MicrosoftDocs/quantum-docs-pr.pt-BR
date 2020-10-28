---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Função ArrangedQubits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f5cce3429b72f0ff6e00c2079241272881512da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694090"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="a04ed-102">Função ArrangedQubits</span><span class="sxs-lookup"><span data-stu-id="a04ed-102">ArrangedQubits function</span></span>

<span data-ttu-id="a04ed-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a04ed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a04ed-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a04ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a04ed-105">Organizar qubits de controle, destino e auxiliar de acordo com um índice</span><span class="sxs-lookup"><span data-stu-id="a04ed-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="a04ed-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a04ed-106">Description</span></span>

<span data-ttu-id="a04ed-107">Retorna uma matriz qubit com destino no índice 0 e Control i no índice 2 ^ i.</span><span class="sxs-lookup"><span data-stu-id="a04ed-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="a04ed-108">Os qubits auxiliares são inseridos em todas as outras posições na matriz.</span><span class="sxs-lookup"><span data-stu-id="a04ed-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="a04ed-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a04ed-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="a04ed-110">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a04ed-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="a04ed-111">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a04ed-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="a04ed-112">auxiliar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a04ed-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="a04ed-113">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a04ed-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

