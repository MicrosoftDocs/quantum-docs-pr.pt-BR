---
uid: Microsoft.Quantum.Canon.GrayCode
title: Função GrayCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: b15586c57180b00064721afc990436320824cba2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206877"
---
# <a name="graycode-function"></a><span data-ttu-id="7709c-102">Função GrayCode</span><span class="sxs-lookup"><span data-stu-id="7709c-102">GrayCode function</span></span>

<span data-ttu-id="7709c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7709c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7709c-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7709c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7709c-105">Cria sequências de código cinza</span><span class="sxs-lookup"><span data-stu-id="7709c-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="7709c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="7709c-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="7709c-107">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7709c-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7709c-108">Número de bits</span><span class="sxs-lookup"><span data-stu-id="7709c-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="7709c-109">Saída: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="7709c-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="7709c-110">Matriz de tuplas.</span><span class="sxs-lookup"><span data-stu-id="7709c-110">Array of tuples.</span></span> <span data-ttu-id="7709c-111">O primeiro valor na tupla é o valor no segundo valor da sequência GrayCode na tupla é a posição para alterar o valor atual para obter o próximo.</span><span class="sxs-lookup"><span data-stu-id="7709c-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>