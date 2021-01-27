---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Operação AllowAtMostNCallsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: bb6ba2615b571b0d9d056b93f8e36d2dec0c4a21
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853529"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="ef397-102">Operação AllowAtMostNCallsCA</span><span class="sxs-lookup"><span data-stu-id="ef397-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="ef397-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="ef397-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="ef397-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef397-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef397-105">Entre uma chamada para essa operação e seu adjacente, o declara que uma determinada operação é chamada no máximo um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="ef397-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="ef397-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ef397-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="ef397-107">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ef397-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ef397-108">O número máximo de vezes que `op` pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="ef397-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput--is-adj--ctl"></a><span data-ttu-id="ef397-109">op: ' TInput => ' TOutput é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="ef397-109">op : 'TInput => 'TOutput  is Adj + Ctl</span></span>

<span data-ttu-id="ef397-110">Uma operação cujas chamadas devem ser restritas.</span><span class="sxs-lookup"><span data-stu-id="ef397-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="ef397-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="ef397-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="ef397-112">Uma mensagem a ser exibida após a falha.</span><span class="sxs-lookup"><span data-stu-id="ef397-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ef397-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef397-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ef397-114">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="ef397-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="ef397-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="ef397-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="ef397-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="ef397-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="ef397-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ef397-117">Example</span></span>

<span data-ttu-id="ef397-118">O trecho a seguir falhará quando executado em computadores que dão suporte a este diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="ef397-118">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
using (register = Qubit[4]) {
    within {
        AllowAtMostNCallsCA(3, H, "Too many calls to H.");
    } apply {
        // Fails since this calls H four times, rather than the
        // allowed maximum of three.
        ApplyToEach(H, register);
    }
}
```

## <a name="remarks"></a><span data-ttu-id="ef397-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef397-119">Remarks</span></span>

<span data-ttu-id="ef397-120">Esta operação pode ser substituída por um não op em destinos que não dão suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="ef397-120">This operation may be replaced by a no-op on targets which do not support it.</span></span>