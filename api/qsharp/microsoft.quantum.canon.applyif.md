---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Operação ApplyIf
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: 109a5c4748d183f199e420b4b1aef687613d220c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841883"
---
# <a name="applyif-operation"></a><span data-ttu-id="fdb62-102">Operação ApplyIf</span><span class="sxs-lookup"><span data-stu-id="fdb62-102">ApplyIf operation</span></span>

<span data-ttu-id="fdb62-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fdb62-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fdb62-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fdb62-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fdb62-105">Aplica uma operação com condição em um bit clássico.</span><span class="sxs-lookup"><span data-stu-id="fdb62-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="fdb62-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdb62-106">Description</span></span>

<span data-ttu-id="fdb62-107">Dada uma operação `op` e um valor de bit `bit` , aplica- `op` `target` se ao If `bit` is `true` .</span><span class="sxs-lookup"><span data-stu-id="fdb62-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="fdb62-108">Se `false` nada acontecer com o `target` .</span><span class="sxs-lookup"><span data-stu-id="fdb62-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="fdb62-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdb62-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="fdb62-110">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="fdb62-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="fdb62-111">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="fdb62-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="fdb62-112">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fdb62-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fdb62-113">um booliano que controla se op é aplicado ou não.</span><span class="sxs-lookup"><span data-stu-id="fdb62-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="fdb62-114">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="fdb62-114">target : 'T</span></span>

<span data-ttu-id="fdb62-115">A entrada à qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="fdb62-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fdb62-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fdb62-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="fdb62-117">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="fdb62-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fdb62-118">T'</span><span class="sxs-lookup"><span data-stu-id="fdb62-118">'T</span></span>

<span data-ttu-id="fdb62-119">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="fdb62-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="fdb62-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fdb62-120">Example</span></span>

<span data-ttu-id="fdb62-121">O seguinte prepara um registro de qubits para um estado de base computacional representado por uma cadeia de caracteres de bits clássicas fornecida como uma matriz de `Bool` valores:</span><span class="sxs-lookup"><span data-stu-id="fdb62-121">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="fdb62-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fdb62-122">See Also</span></span>

- [<span data-ttu-id="fdb62-123">Microsoft. Quantum. Canon. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="fdb62-123">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="fdb62-124">Microsoft. Quantum. Canon. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="fdb62-124">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="fdb62-125">Microsoft. Quantum. Canon. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="fdb62-125">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)