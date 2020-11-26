---
uid: Microsoft.Quantum.Convert.BoolArrayAsResultArray
title: Função BoolArrayAsResultArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsResultArray
qsharp.summary: Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: 388fb67ba33810fc813fb646577bfa7f4a2b51ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224455"
---
# <a name="boolarrayasresultarray-function"></a><span data-ttu-id="a51a9-102">Função BoolArrayAsResultArray</span><span class="sxs-lookup"><span data-stu-id="a51a9-102">BoolArrayAsResultArray function</span></span>

<span data-ttu-id="a51a9-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="a51a9-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="a51a9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a51a9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a51a9-105">Converte um `Bool[]` tipo em um `Result[]` tipo, onde `true` é mapeado para `One` e `false` é mapeado para `Zero` .</span><span class="sxs-lookup"><span data-stu-id="a51a9-105">Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.</span></span>

```qsharp
function BoolArrayAsResultArray (input : Bool[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="a51a9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a51a9-106">Input</span></span>

### <a name="input--bool"></a><span data-ttu-id="a51a9-107">entrada: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="a51a9-107">input : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="a51a9-108">`Bool[]` a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="a51a9-108">`Bool[]` to be converted.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a51a9-109">Saída: __inválido <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="a51a9-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="a51a9-110">Um `Result[]` que representa o `input`.</span><span class="sxs-lookup"><span data-stu-id="a51a9-110">A `Result[]` representing the `input`.</span></span>