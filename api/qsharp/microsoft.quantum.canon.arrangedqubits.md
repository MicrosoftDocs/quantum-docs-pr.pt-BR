---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Função ArrangedQubits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 07a4ed5fe99dedb333246f7161d157dcd01a01da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841069"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="53ff4-102">Função ArrangedQubits</span><span class="sxs-lookup"><span data-stu-id="53ff4-102">ArrangedQubits function</span></span>

<span data-ttu-id="53ff4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="53ff4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="53ff4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="53ff4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="53ff4-105">Organizar qubits de controle, destino e auxiliar de acordo com um índice</span><span class="sxs-lookup"><span data-stu-id="53ff4-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="53ff4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="53ff4-106">Description</span></span>

<span data-ttu-id="53ff4-107">Retorna uma matriz qubit com destino no índice 0 e Control i no índice 2 ^ i.</span><span class="sxs-lookup"><span data-stu-id="53ff4-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="53ff4-108">Os qubits auxiliares são inseridos em todas as outras posições na matriz.</span><span class="sxs-lookup"><span data-stu-id="53ff4-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="53ff4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="53ff4-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="53ff4-110">controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="53ff4-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="53ff4-111">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="53ff4-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="53ff4-112">auxiliar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="53ff4-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="53ff4-113">Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="53ff4-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

