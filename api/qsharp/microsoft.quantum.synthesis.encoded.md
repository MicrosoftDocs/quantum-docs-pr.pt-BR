---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Função codificada
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 6b9d21969ee90f3928b65a1c97a5b0f15157e381
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697052"
---
# <a name="encoded-function"></a><span data-ttu-id="ae541-102">Função codificada</span><span class="sxs-lookup"><span data-stu-id="ae541-102">Encoded function</span></span>

<span data-ttu-id="ae541-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="ae541-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="ae541-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ae541-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ae541-105">Codificar a tabela verdade na {1,-1} codificação</span><span class="sxs-lookup"><span data-stu-id="ae541-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="ae541-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ae541-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="ae541-107">tabela: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="ae541-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="ae541-108">Verdade, tabela como matriz de valores da verdade</span><span class="sxs-lookup"><span data-stu-id="ae541-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="ae541-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ae541-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ae541-110">Verdadeira tabela como matriz de {1,-1} inteiros</span><span class="sxs-lookup"><span data-stu-id="ae541-110">Truth table as array of {1,-1} integers</span></span>