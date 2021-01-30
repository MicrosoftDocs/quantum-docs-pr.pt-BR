---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Operação ApplyControlledOnInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 499a25104742b2d03886065baad4d535ea92e83b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845110"
---
# <a name="applycontrolledonint-operation"></a><span data-ttu-id="6dc22-102">Operação ApplyControlledOnInt</span><span class="sxs-lookup"><span data-stu-id="6dc22-102">ApplyControlledOnInt operation</span></span>

<span data-ttu-id="6dc22-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6dc22-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6dc22-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6dc22-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6dc22-105">Aplica uma operação unitário no registro de destino se o estado de registro de controle corresponder a um número inteiro positivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6dc22-105">Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6dc22-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6dc22-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="6dc22-107">número de série: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6dc22-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6dc22-108">Um inteiro não negativo no qual a operação `oracle` deve ser controlada.</span><span class="sxs-lookup"><span data-stu-id="6dc22-108">A nonnegative integer on which the operation `oracle` should be controlled.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="6dc22-109">Oracle: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="6dc22-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="6dc22-110">Uma operação unitário a ser controlada.</span><span class="sxs-lookup"><span data-stu-id="6dc22-110">A unitary operation to be controlled.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="6dc22-111">controlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6dc22-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6dc22-112">Um registro do Quantum que controla a aplicação do `oracle` .</span><span class="sxs-lookup"><span data-stu-id="6dc22-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="6dc22-113">targetRegister: ' t</span><span class="sxs-lookup"><span data-stu-id="6dc22-113">targetRegister : 'T</span></span>

<span data-ttu-id="6dc22-114">Um registro no qual aplicar `oracle` .</span><span class="sxs-lookup"><span data-stu-id="6dc22-114">A register on which to apply `oracle`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6dc22-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6dc22-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6dc22-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="6dc22-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6dc22-117">T'</span><span class="sxs-lookup"><span data-stu-id="6dc22-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="6dc22-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dc22-118">Remarks</span></span>

<span data-ttu-id="6dc22-119">O valor de `numberState` é interpretado usando uma codificação little-endian.</span><span class="sxs-lookup"><span data-stu-id="6dc22-119">The value of `numberState` is interpreted using a little-endian encoding.</span></span>

<span data-ttu-id="6dc22-120">`numberState` deve ser no máximo $2 ^ \texttt{Length (controlRegister)}-$1.</span><span class="sxs-lookup"><span data-stu-id="6dc22-120">`numberState` must be at most $2^\texttt{Length(controlRegister)} - 1$.</span></span>
<span data-ttu-id="6dc22-121">Por exemplo, `numberState = 537` significa que `oracle` será aplicado se e somente se `controlRegister` estiver no estado $ \ket {537} $.</span><span class="sxs-lookup"><span data-stu-id="6dc22-121">For example, `numberState = 537` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{537}$.</span></span>