---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: Operação ApplyIfA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: 8bdca1bf286d564dfbb540bc9d63c035d2196f00
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845030"
---
# <a name="applyifa-operation"></a><span data-ttu-id="247d4-102">Operação ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="247d4-102">ApplyIfA operation</span></span>

<span data-ttu-id="247d4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="247d4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="247d4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="247d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="247d4-105">Aplica uma operação de adjointable condicionalmente em um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="247d4-105">Applies a adjointable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="247d4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="247d4-106">Description</span></span>

<span data-ttu-id="247d4-107">Dada uma operação `op` e um valor de bit `bit` , aplica- `op` `target` se ao If `bit` is `true` .</span><span class="sxs-lookup"><span data-stu-id="247d4-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="247d4-108">Se `false` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="247d4-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="247d4-109">O sufixo `A` indica que a operação a ser aplicada é adjointable.</span><span class="sxs-lookup"><span data-stu-id="247d4-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="247d4-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="247d4-110">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="247d4-111">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="247d4-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="247d4-112">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="247d4-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="247d4-113">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="247d4-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="247d4-114">um booliano que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="247d4-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="247d4-115">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="247d4-115">target : 'T</span></span>

<span data-ttu-id="247d4-116">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="247d4-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="247d4-117">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="247d4-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="247d4-118">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="247d4-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="247d4-119">T'</span><span class="sxs-lookup"><span data-stu-id="247d4-119">'T</span></span>

<span data-ttu-id="247d4-120">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="247d4-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="247d4-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="247d4-121">Example</span></span>

<span data-ttu-id="247d4-122">O seguinte prepara um registro de qubits para um estado de base computacional representado por uma cadeia de caracteres de bits clássicas fornecida como uma matriz de `Bool` valores:</span><span class="sxs-lookup"><span data-stu-id="247d4-122">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="247d4-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="247d4-123">See Also</span></span>

- [<span data-ttu-id="247d4-124">Microsoft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="247d4-124">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="247d4-125">Microsoft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="247d4-125">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="247d4-126">Microsoft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="247d4-126">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)