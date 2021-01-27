---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Operação ApplyToEachIndexA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: fb278f217ac450ab48aa37b0035cd1bdd295d3e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850838"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="d710b-102">Operação ApplyToEachIndexA</span><span class="sxs-lookup"><span data-stu-id="d710b-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="d710b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d710b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d710b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d710b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d710b-105">Aplica uma operação single-qubit para cada elemento indexado em um registro.</span><span class="sxs-lookup"><span data-stu-id="d710b-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="d710b-106">O modificador `A` indica que a operação single-qubit é o adjointable.</span><span class="sxs-lookup"><span data-stu-id="d710b-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="d710b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d710b-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj"></a><span data-ttu-id="d710b-108">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj</span><span class="sxs-lookup"><span data-stu-id="d710b-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d710b-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="d710b-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="d710b-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="d710b-110">register : 'T[]</span></span>

<span data-ttu-id="d710b-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="d710b-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d710b-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d710b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d710b-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="d710b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d710b-114">T'</span><span class="sxs-lookup"><span data-stu-id="d710b-114">'T</span></span>

<span data-ttu-id="d710b-115">O destino no qual cada uma das operações atua.</span><span class="sxs-lookup"><span data-stu-id="d710b-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="d710b-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d710b-116">See Also</span></span>

- [<span data-ttu-id="d710b-117">Microsoft. Quantum. Canon. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="d710b-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)