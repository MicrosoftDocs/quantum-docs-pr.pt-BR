---
uid: Microsoft.Quantum.Diagnostics.Fact
title: Função de fato
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 8e86000f04c01040d420c2f682fc1b4ccf35cf39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853317"
---
# <a name="fact-function"></a><span data-ttu-id="76848-102">Função de fato</span><span class="sxs-lookup"><span data-stu-id="76848-102">Fact function</span></span>

<span data-ttu-id="76848-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="76848-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="76848-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="76848-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="76848-105">Declara que uma condição clássica é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="76848-105">Declares that a classical condition is true.</span></span>

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="76848-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="76848-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="76848-107">real: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="76848-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="76848-108">A condição a ser declarada.</span><span class="sxs-lookup"><span data-stu-id="76848-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="76848-109">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="76848-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="76848-110">Cadeia de caracteres de mensagem de falha a ser impressa no caso de a condição clássica ser falsa.</span><span class="sxs-lookup"><span data-stu-id="76848-110">Failure message string to be printed in the case that the classical condition is false.</span></span>



## <a name="output--unit"></a><span data-ttu-id="76848-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="76848-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="76848-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="76848-112">Example</span></span>

<span data-ttu-id="76848-113">O seguinte trecho de código Q # falhará:</span><span class="sxs-lookup"><span data-stu-id="76848-113">The following Q# snippet will fail:</span></span>

```qsharp
Fact(false, "Expected true.");
```

## <a name="see-also"></a><span data-ttu-id="76848-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="76848-114">See Also</span></span>

- [<span data-ttu-id="76848-115">Microsoft. Quantum. Diagnostics. contradição</span><span class="sxs-lookup"><span data-stu-id="76848-115">Microsoft.Quantum.Diagnostics.Contradiction</span></span>](xref:Microsoft.Quantum.Diagnostics.Contradiction)