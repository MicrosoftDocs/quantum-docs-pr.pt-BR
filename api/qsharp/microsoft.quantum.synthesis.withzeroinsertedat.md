---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Função WithZeroInsertedAt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 414b703151b9152aa69709d9c28e68e5ae63506f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228858"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="f6489-102">Função WithZeroInsertedAt</span><span class="sxs-lookup"><span data-stu-id="f6489-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="f6489-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f6489-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f6489-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f6489-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f6489-105">Inserir um 0-bit em um número inteiro</span><span class="sxs-lookup"><span data-stu-id="f6489-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="f6489-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6489-106">Description</span></span>

<span data-ttu-id="f6489-107">Essa operação usa um número inteiro, insere um 0 no bit `position` e retorna o valor atualizado como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="f6489-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="f6489-108">Por exemplo, inserir um 0 na posição 2 no número 10 (US $10 _ {10} = 1010_ {2} $) retorna o número 18 ($18 _ {10} = 10010_ {2} $).</span><span class="sxs-lookup"><span data-stu-id="f6489-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="f6489-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f6489-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="f6489-110">posição: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f6489-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f6489-111">A posição na qual 0 é inserido</span><span class="sxs-lookup"><span data-stu-id="f6489-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="f6489-112">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f6489-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f6489-113">O valor que é modificado</span><span class="sxs-lookup"><span data-stu-id="f6489-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="f6489-114">Saída: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f6489-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f6489-115">Valor modificado</span><span class="sxs-lookup"><span data-stu-id="f6489-115">Modified value</span></span>