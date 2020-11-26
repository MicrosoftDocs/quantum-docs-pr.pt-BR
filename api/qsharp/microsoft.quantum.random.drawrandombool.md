---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Operação DrawRandomBool
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: dbe0836af5aa19f1bdce3cfe93be6833358c22be
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192954"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="a54dd-102">Operação DrawRandomBool</span><span class="sxs-lookup"><span data-stu-id="a54dd-102">DrawRandomBool operation</span></span>

<span data-ttu-id="a54dd-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="a54dd-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="a54dd-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a54dd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a54dd-105">Devido a uma probabilidade de êxito, retorna uma única avaliação de Bernoulli que é verdadeira com a probabilidade especificada.</span><span class="sxs-lookup"><span data-stu-id="a54dd-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="a54dd-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a54dd-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="a54dd-107">successProbability: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a54dd-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a54dd-108">A probabilidade com a qual `true` deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="a54dd-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a54dd-109">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a54dd-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a54dd-110">`true` com probabilidade `successProbability` e `false` com probabilidade `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="a54dd-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>