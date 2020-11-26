---
uid: Microsoft.Quantum.Canon.BoundC
title: Função BoundC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 02e9b6a9676cdd1996d3a2413b2a6383e3a4e90e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207574"
---
# <a name="boundc-function"></a><span data-ttu-id="17950-102">Função BoundC</span><span class="sxs-lookup"><span data-stu-id="17950-102">BoundC function</span></span>

<span data-ttu-id="17950-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="17950-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="17950-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="17950-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="17950-105">Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.</span><span class="sxs-lookup"><span data-stu-id="17950-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="17950-106">O modificador `C` indica que todas as operações na matriz são controláveis.</span><span class="sxs-lookup"><span data-stu-id="17950-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="17950-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="17950-107">Input</span></span>

### <a name="operations--t--unit--is-ctl"></a><span data-ttu-id="17950-108">operações: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL []</span><span class="sxs-lookup"><span data-stu-id="17950-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="17950-109">Uma sequência de operações a ser executada em uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="17950-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="17950-110">Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL</span><span class="sxs-lookup"><span data-stu-id="17950-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="17950-111">Uma nova operação que executa cada operação específica em sequência em sua entrada.</span><span class="sxs-lookup"><span data-stu-id="17950-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="17950-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="17950-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="17950-113">T'</span><span class="sxs-lookup"><span data-stu-id="17950-113">'T</span></span>

<span data-ttu-id="17950-114">O destino no qual cada uma das operações na matriz atua.</span><span class="sxs-lookup"><span data-stu-id="17950-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="17950-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="17950-115">See Also</span></span>

- [<span data-ttu-id="17950-116">Microsoft. Quantum. Canon. Bound</span><span class="sxs-lookup"><span data-stu-id="17950-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)