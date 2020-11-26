---
uid: Microsoft.Quantum.Math.PlusA
title: Função PlusA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: fe19c5d2e075624516376a5d5fa49014acb295ec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194824"
---
# <a name="plusa-function"></a><span data-ttu-id="04276-102">Função PlusA</span><span class="sxs-lookup"><span data-stu-id="04276-102">PlusA function</span></span>

<span data-ttu-id="04276-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="04276-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="04276-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="04276-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="04276-105">Retorna a soma (concatenação) de duas entradas.</span><span class="sxs-lookup"><span data-stu-id="04276-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="04276-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="04276-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="04276-107">a: ' element []</span><span class="sxs-lookup"><span data-stu-id="04276-107">a : 'Element[]</span></span>

<span data-ttu-id="04276-108">A primeira entrada $a $ a ser somada.</span><span class="sxs-lookup"><span data-stu-id="04276-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="04276-109">b: ' element []</span><span class="sxs-lookup"><span data-stu-id="04276-109">b : 'Element[]</span></span>

<span data-ttu-id="04276-110">A segunda entrada $b $ a ser somada.</span><span class="sxs-lookup"><span data-stu-id="04276-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="04276-111">Saída: ' element []</span><span class="sxs-lookup"><span data-stu-id="04276-111">Output : 'Element[]</span></span>

<span data-ttu-id="04276-112">A soma $a + b $.</span><span class="sxs-lookup"><span data-stu-id="04276-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="04276-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="04276-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="04276-114">' Element</span><span class="sxs-lookup"><span data-stu-id="04276-114">'Element</span></span>

<span data-ttu-id="04276-115">O tipo de cada elemento em cada uma das duas matrizes de entrada.</span><span class="sxs-lookup"><span data-stu-id="04276-115">The type of each element in each of the two input arrays.</span></span>