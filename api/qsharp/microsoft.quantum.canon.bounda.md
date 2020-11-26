---
uid: Microsoft.Quantum.Canon.BoundA
title: Função bounda
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3132bf198e98dd1a2b433f36b000060e7e721865
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216941"
---
# <a name="bounda-function"></a><span data-ttu-id="0f18b-102">Função bounda</span><span class="sxs-lookup"><span data-stu-id="0f18b-102">BoundA function</span></span>

<span data-ttu-id="0f18b-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0f18b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0f18b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0f18b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0f18b-105">Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.</span><span class="sxs-lookup"><span data-stu-id="0f18b-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="0f18b-106">O modificador `A` indica que todas as operações na matriz são adjointable.</span><span class="sxs-lookup"><span data-stu-id="0f18b-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="0f18b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f18b-107">Input</span></span>

### <a name="operations--t--unit--is-adj"></a><span data-ttu-id="0f18b-108">operações: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj []</span><span class="sxs-lookup"><span data-stu-id="0f18b-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="0f18b-109">Uma sequência de operações a ser executada em uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="0f18b-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="0f18b-110">Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="0f18b-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="0f18b-111">Uma nova operação que executa cada operação específica em sequência em sua entrada.</span><span class="sxs-lookup"><span data-stu-id="0f18b-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0f18b-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="0f18b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0f18b-113">T'</span><span class="sxs-lookup"><span data-stu-id="0f18b-113">'T</span></span>

<span data-ttu-id="0f18b-114">O destino no qual cada uma das operações na matriz atua.</span><span class="sxs-lookup"><span data-stu-id="0f18b-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f18b-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0f18b-115">See Also</span></span>

- [<span data-ttu-id="0f18b-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="0f18b-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)