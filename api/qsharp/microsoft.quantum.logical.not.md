---
uid: Microsoft.Quantum.Logical.Not
title: Não função
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693107"
---
# <a name="not-function"></a><span data-ttu-id="14936-102">Não função</span><span class="sxs-lookup"><span data-stu-id="14936-102">Not function</span></span>

<span data-ttu-id="14936-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="14936-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="14936-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="14936-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="14936-105">Retorna a negação booliana de um valor.</span><span class="sxs-lookup"><span data-stu-id="14936-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="14936-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="14936-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="14936-107">valor: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="14936-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="14936-108">O valor a ser negado.</span><span class="sxs-lookup"><span data-stu-id="14936-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="14936-109">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="14936-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="14936-110">`true` se e somente se `value` for `false` .</span><span class="sxs-lookup"><span data-stu-id="14936-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="14936-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="14936-111">Remarks</span></span>

<span data-ttu-id="14936-112">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="14936-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```