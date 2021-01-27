---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Operação ApplyToEachA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: da901db2bb3c70186bfe0c8812b5710198d1dff3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844611"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="e1d1b-102">Operação ApplyToEachA</span><span class="sxs-lookup"><span data-stu-id="e1d1b-102">ApplyToEachA operation</span></span>

<span data-ttu-id="e1d1b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e1d1b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e1d1b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e1d1b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e1d1b-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="e1d1b-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="e1d1b-106">O modificador `A` indica que a operação single-qubit é o adjointable.</span><span class="sxs-lookup"><span data-stu-id="e1d1b-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="e1d1b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e1d1b-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj"></a><span data-ttu-id="e1d1b-108">singleElementOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="e1d1b-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e1d1b-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="e1d1b-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="e1d1b-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="e1d1b-110">register : 'T[]</span></span>

<span data-ttu-id="e1d1b-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="e1d1b-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e1d1b-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e1d1b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e1d1b-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e1d1b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e1d1b-114">T'</span><span class="sxs-lookup"><span data-stu-id="e1d1b-114">'T</span></span>

<span data-ttu-id="e1d1b-115">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="e1d1b-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="e1d1b-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e1d1b-116">Example</span></span>

<span data-ttu-id="e1d1b-117">Preparar um estado de três qubit $ \ket{+} $:</span><span class="sxs-lookup"><span data-stu-id="e1d1b-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="e1d1b-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e1d1b-118">See Also</span></span>

- [<span data-ttu-id="e1d1b-119">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="e1d1b-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)