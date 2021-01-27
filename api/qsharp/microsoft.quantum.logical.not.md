---
uid: Microsoft.Quantum.Logical.Not
title: Não função
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: bf09cac8d126371df6218b7e92d68a881b732dc8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849083"
---
# <a name="not-function"></a><span data-ttu-id="1448e-102">Não função</span><span class="sxs-lookup"><span data-stu-id="1448e-102">Not function</span></span>

<span data-ttu-id="1448e-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="1448e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="1448e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1448e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1448e-105">Retorna a negação booliana de um valor.</span><span class="sxs-lookup"><span data-stu-id="1448e-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="1448e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1448e-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="1448e-107">valor: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1448e-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1448e-108">O valor a ser negado.</span><span class="sxs-lookup"><span data-stu-id="1448e-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1448e-109">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1448e-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1448e-110">`true` se e somente se `value` for `false` .</span><span class="sxs-lookup"><span data-stu-id="1448e-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1448e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1448e-111">Remarks</span></span>

<span data-ttu-id="1448e-112">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="1448e-112">The following are equivalent:</span></span>

```qsharp
let x = not value;
let x = Not(value);
```