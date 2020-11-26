---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Função FastHadamardTransformed
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 3e48701f22ddf154721355866e15a85fca0bc7df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203086"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="76627-102">Função FastHadamardTransformed</span><span class="sxs-lookup"><span data-stu-id="76627-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="76627-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="76627-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="76627-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="76627-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="76627-105">Computa a transformação Hadamard de uma função booliana na {-1,1} codificação usando o método de Yates</span><span class="sxs-lookup"><span data-stu-id="76627-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="76627-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="76627-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="76627-107">Func: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="76627-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="76627-108">Tabela verdadeira em {-1,1} codificação</span><span class="sxs-lookup"><span data-stu-id="76627-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="76627-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="76627-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="76627-110">Coeficientes Spectral da função</span><span class="sxs-lookup"><span data-stu-id="76627-110">Spectral coefficients of the function</span></span>