---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Função FastHadamardTransformed
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: be54413ef2d3fdaf7ddc726bc0906adb4ec382ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855462"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="4d157-102">Função FastHadamardTransformed</span><span class="sxs-lookup"><span data-stu-id="4d157-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="4d157-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="4d157-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="4d157-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4d157-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4d157-105">Computa a transformação Hadamard de uma função booliana na {-1,1} codificação usando o método de Yates</span><span class="sxs-lookup"><span data-stu-id="4d157-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="4d157-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d157-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="4d157-107">Func: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4d157-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4d157-108">Tabela verdadeira em {-1,1} codificação</span><span class="sxs-lookup"><span data-stu-id="4d157-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="4d157-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4d157-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4d157-110">Coeficientes Spectral da função</span><span class="sxs-lookup"><span data-stu-id="4d157-110">Spectral coefficients of the function</span></span>

## <a name="example"></a><span data-ttu-id="4d157-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4d157-111">Example</span></span>

```qsharp
FastHadamardTransformed([1, 1, 1, -1]); // [2, 2, 2, -2]
```