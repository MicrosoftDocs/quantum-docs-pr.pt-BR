---
uid: Microsoft.Quantum.Canon.Bound
title: Função associada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 041f654c14f6e926d60038fee698b2b829fab8b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841062"
---
# <a name="bound-function"></a><span data-ttu-id="5f2ae-102">Função associada</span><span class="sxs-lookup"><span data-stu-id="5f2ae-102">Bound function</span></span>

<span data-ttu-id="5f2ae-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5f2ae-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5f2ae-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f2ae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f2ae-105">Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.</span><span class="sxs-lookup"><span data-stu-id="5f2ae-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="5f2ae-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f2ae-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="5f2ae-107">operações: não => [unidade](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="5f2ae-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="5f2ae-108">Uma sequência de operações a ser executada em uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="5f2ae-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="5f2ae-109">Saída: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="5f2ae-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5f2ae-110">Uma nova operação que executa cada operação específica em sequência em sua entrada.</span><span class="sxs-lookup"><span data-stu-id="5f2ae-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5f2ae-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="5f2ae-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5f2ae-112">T'</span><span class="sxs-lookup"><span data-stu-id="5f2ae-112">'T</span></span>

<span data-ttu-id="5f2ae-113">O destino no qual cada uma das operações na matriz atua.</span><span class="sxs-lookup"><span data-stu-id="5f2ae-113">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="5f2ae-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5f2ae-114">Example</span></span>

<span data-ttu-id="5f2ae-115">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="5f2ae-115">The following are equivalent:</span></span>

```qsharp
let bound = Bound([U, V]);
bound(x);
```

<span data-ttu-id="5f2ae-116">e</span><span class="sxs-lookup"><span data-stu-id="5f2ae-116">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="5f2ae-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5f2ae-117">See Also</span></span>

- [<span data-ttu-id="5f2ae-118">Microsoft. Quantum. Canon. BoundC</span><span class="sxs-lookup"><span data-stu-id="5f2ae-118">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="5f2ae-119">Microsoft. Quantum. Canon. Bounda</span><span class="sxs-lookup"><span data-stu-id="5f2ae-119">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="5f2ae-120">Microsoft. Quantum. Canon. BoundCA</span><span class="sxs-lookup"><span data-stu-id="5f2ae-120">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)