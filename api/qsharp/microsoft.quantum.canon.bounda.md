---
uid: Microsoft.Quantum.Canon.BoundA
title: Função bounda
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 40c112d0572dc4eebfc284c9ef29f43706e20c64
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694082"
---
# <a name="bounda-function"></a><span data-ttu-id="a706c-102">Função bounda</span><span class="sxs-lookup"><span data-stu-id="a706c-102">BoundA function</span></span>

<span data-ttu-id="a706c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a706c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a706c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a706c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a706c-105">Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.</span><span class="sxs-lookup"><span data-stu-id="a706c-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="a706c-106">O modificador `A` indica que todas as operações na matriz são adjointable.</span><span class="sxs-lookup"><span data-stu-id="a706c-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="a706c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a706c-107">Input</span></span>

### <a name="operations--t--unit-adj"></a><span data-ttu-id="a706c-108">operações: t => adj da [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="a706c-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj[]</span></span>

<span data-ttu-id="a706c-109">Uma sequência de operações a ser executada em uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="a706c-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-adj"></a><span data-ttu-id="a706c-110">Saída: t => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a706c-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="a706c-111">Uma nova operação que executa cada operação específica em sequência em sua entrada.</span><span class="sxs-lookup"><span data-stu-id="a706c-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a706c-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="a706c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a706c-113">T'</span><span class="sxs-lookup"><span data-stu-id="a706c-113">'T</span></span>

<span data-ttu-id="a706c-114">O destino no qual cada uma das operações na matriz atua.</span><span class="sxs-lookup"><span data-stu-id="a706c-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="a706c-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a706c-115">See Also</span></span>

- [<span data-ttu-id="a706c-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="a706c-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)