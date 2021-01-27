---
uid: Microsoft.Quantum.Canon.BoundCA
title: Função BoundCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 391183829a3cc8b7aa8051767dcfc6bec9638223
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844525"
---
# <a name="boundca-function"></a><span data-ttu-id="9e885-102">Função BoundCA</span><span class="sxs-lookup"><span data-stu-id="9e885-102">BoundCA function</span></span>

<span data-ttu-id="9e885-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9e885-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9e885-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e885-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e885-105">Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.</span><span class="sxs-lookup"><span data-stu-id="9e885-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="9e885-106">O modificador `CA` indica que todas as operações na matriz são de adjointable e controláveis.</span><span class="sxs-lookup"><span data-stu-id="9e885-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9e885-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9e885-107">Input</span></span>

### <a name="operations--t--unit--is-adj--ctl"></a><span data-ttu-id="9e885-108">operações: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL []</span><span class="sxs-lookup"><span data-stu-id="9e885-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="9e885-109">Uma sequência de operações a ser executada em uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="9e885-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="9e885-110">Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="9e885-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="9e885-111">Uma nova operação que executa cada operação específica em sequência em sua entrada.</span><span class="sxs-lookup"><span data-stu-id="9e885-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9e885-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="9e885-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9e885-113">T'</span><span class="sxs-lookup"><span data-stu-id="9e885-113">'T</span></span>

<span data-ttu-id="9e885-114">O destino no qual cada uma das operações na matriz atua.</span><span class="sxs-lookup"><span data-stu-id="9e885-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="9e885-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9e885-115">Example</span></span>

<span data-ttu-id="9e885-116">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="9e885-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundCA([U, V]);
bound(x);
```

<span data-ttu-id="9e885-117">e</span><span class="sxs-lookup"><span data-stu-id="9e885-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="9e885-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9e885-118">See Also</span></span>

- [<span data-ttu-id="9e885-119">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="9e885-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)