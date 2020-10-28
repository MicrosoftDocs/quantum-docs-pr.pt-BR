---
uid: Microsoft.Quantum.Canon.BoundC
title: Função BoundC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 04dca4ff317bf3cee053f7c3903112f4e05a3973
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694079"
---
# <a name="boundc-function"></a><span data-ttu-id="fd28b-102">Função BoundC</span><span class="sxs-lookup"><span data-stu-id="fd28b-102">BoundC function</span></span>

<span data-ttu-id="fd28b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fd28b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fd28b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fd28b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fd28b-105">Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.</span><span class="sxs-lookup"><span data-stu-id="fd28b-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="fd28b-106">O modificador `C` indica que todas as operações na matriz são controláveis.</span><span class="sxs-lookup"><span data-stu-id="fd28b-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="fd28b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd28b-107">Input</span></span>

### <a name="operations--t--unit-ctl"></a><span data-ttu-id="fd28b-108">operações: não => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="fd28b-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl[]</span></span>

<span data-ttu-id="fd28b-109">Uma sequência de operações a ser executada em uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="fd28b-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="fd28b-110">Saída: t => CTL de [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fd28b-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="fd28b-111">Uma nova operação que executa cada operação específica em sequência em sua entrada.</span><span class="sxs-lookup"><span data-stu-id="fd28b-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fd28b-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="fd28b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fd28b-113">T'</span><span class="sxs-lookup"><span data-stu-id="fd28b-113">'T</span></span>

<span data-ttu-id="fd28b-114">O destino no qual cada uma das operações na matriz atua.</span><span class="sxs-lookup"><span data-stu-id="fd28b-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd28b-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fd28b-115">See Also</span></span>

- [<span data-ttu-id="fd28b-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="fd28b-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)