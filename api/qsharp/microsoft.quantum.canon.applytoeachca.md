---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Operação ApplyToEachCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: c85b33760eba8d10d9650be2f8306e4afdd1f307
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841482"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="3f89c-102">Operação ApplyToEachCA</span><span class="sxs-lookup"><span data-stu-id="3f89c-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="3f89c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3f89c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3f89c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3f89c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3f89c-105">Aplica uma operação de qubit único a cada elemento em um registro.</span><span class="sxs-lookup"><span data-stu-id="3f89c-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="3f89c-106">O modificador `CA` indica que a operação single-qubit é controlável e adjointable.</span><span class="sxs-lookup"><span data-stu-id="3f89c-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3f89c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f89c-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a><span data-ttu-id="3f89c-108">singleElementOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3f89c-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3f89c-109">Operação a ser aplicada a cada qubit.</span><span class="sxs-lookup"><span data-stu-id="3f89c-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="3f89c-110">registrar: t []</span><span class="sxs-lookup"><span data-stu-id="3f89c-110">register : 'T[]</span></span>

<span data-ttu-id="3f89c-111">Matriz de qubits na qual aplicar a operação especificada.</span><span class="sxs-lookup"><span data-stu-id="3f89c-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3f89c-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3f89c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3f89c-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3f89c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3f89c-114">T'</span><span class="sxs-lookup"><span data-stu-id="3f89c-114">'T</span></span>

<span data-ttu-id="3f89c-115">O destino no qual a operação atua.</span><span class="sxs-lookup"><span data-stu-id="3f89c-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="3f89c-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3f89c-116">Example</span></span>

<span data-ttu-id="3f89c-117">Preparar um estado de três qubit $ \ket{+} $:</span><span class="sxs-lookup"><span data-stu-id="3f89c-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="3f89c-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3f89c-118">See Also</span></span>

- [<span data-ttu-id="3f89c-119">Microsoft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="3f89c-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)