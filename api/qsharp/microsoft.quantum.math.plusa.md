---
uid: Microsoft.Quantum.Math.PlusA
title: Função PlusA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 0c6fdcf7c59dc5d89bf83e285339046b5ad5a57e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693070"
---
# <a name="plusa-function"></a><span data-ttu-id="4df1a-102">Função PlusA</span><span class="sxs-lookup"><span data-stu-id="4df1a-102">PlusA function</span></span>

<span data-ttu-id="4df1a-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4df1a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4df1a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4df1a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4df1a-105">Retorna a soma (concatenação) de duas entradas.</span><span class="sxs-lookup"><span data-stu-id="4df1a-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="4df1a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4df1a-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="4df1a-107">a: ' element []</span><span class="sxs-lookup"><span data-stu-id="4df1a-107">a : 'Element[]</span></span>

<span data-ttu-id="4df1a-108">A primeira entrada $a $ a ser somada.</span><span class="sxs-lookup"><span data-stu-id="4df1a-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="4df1a-109">b: ' element []</span><span class="sxs-lookup"><span data-stu-id="4df1a-109">b : 'Element[]</span></span>

<span data-ttu-id="4df1a-110">A segunda entrada $b $ a ser somada.</span><span class="sxs-lookup"><span data-stu-id="4df1a-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="4df1a-111">Saída: ' element []</span><span class="sxs-lookup"><span data-stu-id="4df1a-111">Output : 'Element[]</span></span>

<span data-ttu-id="4df1a-112">A soma $a + b $.</span><span class="sxs-lookup"><span data-stu-id="4df1a-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4df1a-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4df1a-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="4df1a-114">' Element</span><span class="sxs-lookup"><span data-stu-id="4df1a-114">'Element</span></span>

<span data-ttu-id="4df1a-115">O tipo de cada elemento em cada uma das duas matrizes de entrada.</span><span class="sxs-lookup"><span data-stu-id="4df1a-115">The type of each element in each of the two input arrays.</span></span>