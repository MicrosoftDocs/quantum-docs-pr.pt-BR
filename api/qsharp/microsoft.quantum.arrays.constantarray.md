---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Função ConstantArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: a3ad8a18856888a0ca6f9dd691242156b0c044d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846244"
---
# <a name="constantarray-function"></a><span data-ttu-id="fe808-102">Função ConstantArray</span><span class="sxs-lookup"><span data-stu-id="fe808-102">ConstantArray function</span></span>

<span data-ttu-id="fe808-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fe808-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fe808-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fe808-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fe808-105">Cria uma matriz de comprimento determinado com todos os elementos iguais ao valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="fe808-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="fe808-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe808-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="fe808-107">comprimento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fe808-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fe808-108">Comprimento da nova matriz.</span><span class="sxs-lookup"><span data-stu-id="fe808-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="fe808-109">valor: ' t</span><span class="sxs-lookup"><span data-stu-id="fe808-109">value : 'T</span></span>

<span data-ttu-id="fe808-110">O valor de cada elemento da nova matriz.</span><span class="sxs-lookup"><span data-stu-id="fe808-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="fe808-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="fe808-111">Output : 'T[]</span></span>

<span data-ttu-id="fe808-112">Uma nova matriz de comprimento `length` , de modo que cada elemento é `value` .</span><span class="sxs-lookup"><span data-stu-id="fe808-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fe808-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="fe808-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fe808-114">T'</span><span class="sxs-lookup"><span data-stu-id="fe808-114">'T</span></span>



## <a name="example"></a><span data-ttu-id="fe808-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fe808-115">Example</span></span>

<span data-ttu-id="fe808-116">O código a seguir cria uma matriz de 3 valores Boolianos, cada um igual a `true` :</span><span class="sxs-lookup"><span data-stu-id="fe808-116">The following code creates an array of 3 Boolean values, each equal to `true`:</span></span>

```qsharp
let array = ConstantArray(3, true);
```