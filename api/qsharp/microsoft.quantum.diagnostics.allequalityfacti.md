---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: Função AllEqualityFactI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: a7043b9c670f79e270180c583fef56b70c1a3bcb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830901"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="800f1-102">Função AllEqualityFactI</span><span class="sxs-lookup"><span data-stu-id="800f1-102">AllEqualityFactI function</span></span>

<span data-ttu-id="800f1-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="800f1-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="800f1-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="800f1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="800f1-105">Declara que duas matrizes de valores inteiros são iguais.</span><span class="sxs-lookup"><span data-stu-id="800f1-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="800f1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="800f1-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="800f1-107">real: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="800f1-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="800f1-108">A matriz produzida por um caso de teste de interesse.</span><span class="sxs-lookup"><span data-stu-id="800f1-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="800f1-109">esperado: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="800f1-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="800f1-110">A matriz que é esperada de um caso de teste de interesse.</span><span class="sxs-lookup"><span data-stu-id="800f1-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="800f1-111">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="800f1-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="800f1-112">Uma mensagem a ser impressa se as matrizes não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="800f1-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="800f1-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="800f1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

