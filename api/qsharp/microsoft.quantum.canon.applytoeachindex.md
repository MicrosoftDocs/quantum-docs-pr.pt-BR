---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Operação ApplyToEachIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 8b34dc24580a3df7ae2c13ef87a6fa10c7afd3f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844586"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="4f0df-102">Operação ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="4f0df-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="4f0df-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4f0df-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4f0df-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4f0df-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4f0df-105">Aplica uma operação single-qubit para cada elemento indexado em um registro.</span><span class="sxs-lookup"><span data-stu-id="4f0df-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4f0df-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f0df-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="4f0df-107">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), t) = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="4f0df-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4f0df-108">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="4f0df-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="4f0df-109">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="4f0df-109">register : 'T[]</span></span>

<span data-ttu-id="4f0df-110">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="4f0df-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4f0df-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4f0df-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4f0df-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4f0df-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4f0df-113">T'</span><span class="sxs-lookup"><span data-stu-id="4f0df-113">'T</span></span>

<span data-ttu-id="4f0df-114">O destino no qual cada uma das operações atua.</span><span class="sxs-lookup"><span data-stu-id="4f0df-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f0df-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4f0df-115">See Also</span></span>

- [<span data-ttu-id="4f0df-116">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="4f0df-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="4f0df-117">Microsoft. Quantum. Canon. ApplyToEachIndexA</span><span class="sxs-lookup"><span data-stu-id="4f0df-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="4f0df-118">Microsoft. Quantum. Canon. ApplyToEachIndexC</span><span class="sxs-lookup"><span data-stu-id="4f0df-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="4f0df-119">Microsoft. Quantum. Canon. ApplyToEachIndexCA</span><span class="sxs-lookup"><span data-stu-id="4f0df-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)