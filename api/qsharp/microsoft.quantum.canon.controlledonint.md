---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Função ControlledOnInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 4c48f3257f91fc50040d02cae7c2f7bdf87ea7c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694043"
---
# <a name="controlledonint-function"></a><span data-ttu-id="06067-102">Função ControlledOnInt</span><span class="sxs-lookup"><span data-stu-id="06067-102">ControlledOnInt function</span></span>

<span data-ttu-id="06067-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="06067-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="06067-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06067-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06067-105">Retorna um operador unitário que aplica um Oracle no registro de destino se o estado de registro de controle corresponder a um número inteiro positivo especificado.</span><span class="sxs-lookup"><span data-stu-id="06067-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="06067-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="06067-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="06067-107">número de série: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="06067-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="06067-108">Inteiro positivo.</span><span class="sxs-lookup"><span data-stu-id="06067-108">Positive integer.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="06067-109">Oracle: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="06067-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="06067-110">Operador unitário.</span><span class="sxs-lookup"><span data-stu-id="06067-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit-adj--ctl"></a><span data-ttu-id="06067-111">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[], t) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="06067-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="06067-112">Um operador unitário que se aplica ao `oracle` registro de destino se o estado de registro de controle corresponder ao estado de número `numberState` .</span><span class="sxs-lookup"><span data-stu-id="06067-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="06067-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="06067-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="06067-114">T'</span><span class="sxs-lookup"><span data-stu-id="06067-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="06067-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="06067-115">Remarks</span></span>

<span data-ttu-id="06067-116">O valor de `numberState` é interpretado usando uma codificação little-endian.</span><span class="sxs-lookup"><span data-stu-id="06067-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>