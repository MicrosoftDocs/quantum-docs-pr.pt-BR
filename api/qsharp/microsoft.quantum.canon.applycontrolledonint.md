---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Operação ApplyControlledOnInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: c8ea76946143967de4b6ac65986a1c4407ecb633
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694323"
---
# <a name="applycontrolledonint-operation"></a><span data-ttu-id="f802f-102">Operação ApplyControlledOnInt</span><span class="sxs-lookup"><span data-stu-id="f802f-102">ApplyControlledOnInt operation</span></span>

<span data-ttu-id="f802f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f802f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f802f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f802f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f802f-105">Aplica uma operação unitário no registro de destino se o estado de registro de controle corresponder a um número inteiro positivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f802f-105">Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="f802f-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f802f-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="f802f-107">número de série: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f802f-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f802f-108">Um inteiro não negativo no qual a operação `oracle` deve ser controlada.</span><span class="sxs-lookup"><span data-stu-id="f802f-108">A nonnegative integer on which the operation `oracle` should be controlled.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="f802f-109">Oracle: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="f802f-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="f802f-110">Uma operação unitário a ser controlada.</span><span class="sxs-lookup"><span data-stu-id="f802f-110">A unitary operation to be controlled.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="f802f-111">controlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f802f-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f802f-112">Um registro do Quantum que controla a aplicação do `oracle` .</span><span class="sxs-lookup"><span data-stu-id="f802f-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="f802f-113">targetRegister: ' t</span><span class="sxs-lookup"><span data-stu-id="f802f-113">targetRegister : 'T</span></span>

<span data-ttu-id="f802f-114">Um registro no qual aplicar `oracle` .</span><span class="sxs-lookup"><span data-stu-id="f802f-114">A register on which to apply `oracle`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f802f-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f802f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f802f-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f802f-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f802f-117">T'</span><span class="sxs-lookup"><span data-stu-id="f802f-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="f802f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f802f-118">Remarks</span></span>

<span data-ttu-id="f802f-119">O valor de `numberState` é interpretado usando uma codificação little-endian.</span><span class="sxs-lookup"><span data-stu-id="f802f-119">The value of `numberState` is interpreted using a little-endian encoding.</span></span>

<span data-ttu-id="f802f-120">`numberState` deve ser no máximo $2 ^ \texttt{Length (controlRegister)}-$1.</span><span class="sxs-lookup"><span data-stu-id="f802f-120">`numberState` must be at most $2^\texttt{Length(controlRegister)} - 1$.</span></span>
<span data-ttu-id="f802f-121">Por exemplo, `numberState = 537` significa que `oracle` será aplicado se e somente se `controlRegister` estiver no estado $ \ket {537} $.</span><span class="sxs-lookup"><span data-stu-id="f802f-121">For example, `numberState = 537` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{537}$.</span></span>