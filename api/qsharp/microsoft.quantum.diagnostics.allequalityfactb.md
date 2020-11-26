---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: Função AllEqualityFactB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 79dcf65956ba9436fb6fdd452f22f35d4852d6f8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213694"
---
# <a name="allequalityfactb-function"></a><span data-ttu-id="f658a-102">Função AllEqualityFactB</span><span class="sxs-lookup"><span data-stu-id="f658a-102">AllEqualityFactB function</span></span>

<span data-ttu-id="f658a-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f658a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f658a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f658a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f658a-105">Declara que duas matrizes de valores Boolianos são iguais.</span><span class="sxs-lookup"><span data-stu-id="f658a-105">Asserts that two arrays of boolean values are equal.</span></span>

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="f658a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f658a-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="f658a-107">real: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f658a-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="f658a-108">A matriz produzida por um caso de teste de interesse.</span><span class="sxs-lookup"><span data-stu-id="f658a-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="f658a-109">esperado: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f658a-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="f658a-110">A matriz que é esperada de um caso de teste de interesse.</span><span class="sxs-lookup"><span data-stu-id="f658a-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="f658a-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="f658a-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="f658a-112">Uma mensagem a ser impressa se as matrizes não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="f658a-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f658a-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f658a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

