---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Função ControlledOnInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 6c7f46c44f2a2427f702e463195f26660cb4fca1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840781"
---
# <a name="controlledonint-function"></a><span data-ttu-id="8b7d8-102">Função ControlledOnInt</span><span class="sxs-lookup"><span data-stu-id="8b7d8-102">ControlledOnInt function</span></span>

<span data-ttu-id="8b7d8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8b7d8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8b7d8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b7d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b7d8-105">Retorna um operador unitário que aplica um Oracle no registro de destino se o estado de registro de controle corresponder a um número inteiro positivo especificado.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="8b7d8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b7d8-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="8b7d8-107">número de série: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8b7d8-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8b7d8-108">Inteiro positivo.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-108">Positive integer.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="8b7d8-109">Oracle: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="8b7d8-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8b7d8-110">Operador unitário.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="8b7d8-111">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[], t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="8b7d8-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8b7d8-112">Um operador unitário que se aplica ao `oracle` registro de destino se o estado de registro de controle corresponder ao estado de número `numberState` .</span><span class="sxs-lookup"><span data-stu-id="8b7d8-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8b7d8-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="8b7d8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8b7d8-114">T'</span><span class="sxs-lookup"><span data-stu-id="8b7d8-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="8b7d8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b7d8-115">Remarks</span></span>

<span data-ttu-id="8b7d8-116">O valor de `numberState` é interpretado usando uma codificação little-endian.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>