---
uid: Microsoft.Quantum.Canon.Bound
title: Função associada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 34ca2b79d0ee09bd3b5b5b3f0c0b20420d5b3882
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694084"
---
# <a name="bound-function"></a><span data-ttu-id="dcd9a-102">Função associada</span><span class="sxs-lookup"><span data-stu-id="dcd9a-102">Bound function</span></span>

<span data-ttu-id="dcd9a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dcd9a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dcd9a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dcd9a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dcd9a-105">Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="dcd9a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="dcd9a-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="dcd9a-107">operações: não => [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="dcd9a-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="dcd9a-108">Uma sequência de operações a ser executada em uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="dcd9a-109">Saída: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="dcd9a-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="dcd9a-110">Uma nova operação que executa cada operação específica em sequência em sua entrada.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dcd9a-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="dcd9a-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dcd9a-112">T'</span><span class="sxs-lookup"><span data-stu-id="dcd9a-112">'T</span></span>

<span data-ttu-id="dcd9a-113">O destino no qual cada uma das operações na matriz atua.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-113">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="dcd9a-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="dcd9a-114">See Also</span></span>

- [<span data-ttu-id="dcd9a-115">Microsoft. Quantum. Canon. BoundC</span><span class="sxs-lookup"><span data-stu-id="dcd9a-115">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="dcd9a-116">Microsoft. Quantum. Canon. Bounda</span><span class="sxs-lookup"><span data-stu-id="dcd9a-116">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="dcd9a-117">Microsoft. Quantum. Canon. BoundCA</span><span class="sxs-lookup"><span data-stu-id="dcd9a-117">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)