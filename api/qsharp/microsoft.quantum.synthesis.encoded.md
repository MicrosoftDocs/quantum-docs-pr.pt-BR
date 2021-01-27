---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Função codificada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 44f6b247e6bfab7b55c46146cb63f8b6d219955b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855490"
---
# <a name="encoded-function"></a><span data-ttu-id="6bcc6-102">Função codificada</span><span class="sxs-lookup"><span data-stu-id="6bcc6-102">Encoded function</span></span>

<span data-ttu-id="6bcc6-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6bcc6-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6bcc6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6bcc6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6bcc6-105">Codificar a tabela verdade na {1,-1} codificação</span><span class="sxs-lookup"><span data-stu-id="6bcc6-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="6bcc6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6bcc6-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="6bcc6-107">tabela: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="6bcc6-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="6bcc6-108">Verdade, tabela como matriz de valores da verdade</span><span class="sxs-lookup"><span data-stu-id="6bcc6-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="6bcc6-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6bcc6-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6bcc6-110">Verdadeira tabela como matriz de {1,-1} inteiros</span><span class="sxs-lookup"><span data-stu-id="6bcc6-110">Truth table as array of {1,-1} integers</span></span>

## <a name="example"></a><span data-ttu-id="6bcc6-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6bcc6-111">Example</span></span>

```qsharp
Encoded([false, false, false, true]); // [1, 1, 1, -1]
```