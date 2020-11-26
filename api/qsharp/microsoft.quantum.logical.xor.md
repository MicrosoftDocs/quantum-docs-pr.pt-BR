---
uid: Microsoft.Quantum.Logical.Xor
title: Função XOR
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: afb94bd1fd0b791a9a7d84bc28b0cc2baf9a0938
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197085"
---
# <a name="xor-function"></a><span data-ttu-id="1dd69-102">Função XOR</span><span class="sxs-lookup"><span data-stu-id="1dd69-102">Xor function</span></span>

<span data-ttu-id="1dd69-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="1dd69-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="1dd69-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1dd69-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1dd69-105">Retorna a disjunção exclusiva booliana de dois valores.</span><span class="sxs-lookup"><span data-stu-id="1dd69-105">Returns the Boolean exclusive disjunction of two values.</span></span>

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="1dd69-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dd69-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="1dd69-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1dd69-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1dd69-108">O primeiro valor a ser considerado.</span><span class="sxs-lookup"><span data-stu-id="1dd69-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="1dd69-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1dd69-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1dd69-110">O segundo valor a ser considerado.</span><span class="sxs-lookup"><span data-stu-id="1dd69-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1dd69-111">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1dd69-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1dd69-112">`true` se e somente se for exatamente um de `a` e `b` for `true` .</span><span class="sxs-lookup"><span data-stu-id="1dd69-112">`true` if and only if exactly one of `a` and `b` is `true`.</span></span>