---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZZTermToPauliGenIdx
title: Função _ZZTermToPauliGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZZTermToPauliGenIdx
qsharp.summary: Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: f8a173e2adb4494a08b48158a010f264562bbaa6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693718"
---
# <a name="_zztermtopauligenidx-function"></a><span data-ttu-id="364f5-102">Função _ZZTermToPauliGenIdx</span><span class="sxs-lookup"><span data-stu-id="364f5-102">_ZZTermToPauliGenIdx function</span></span>

<span data-ttu-id="364f5-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="364f5-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="364f5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="364f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="364f5-105">Converte um GeneratorIndex que descreve um termo ZZ para uma expressão ' GeneratorIndex [] ' em termos de Paulis.</span><span class="sxs-lookup"><span data-stu-id="364f5-105">Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZZTermToPauliGenIdx (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="364f5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="364f5-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="364f5-107">termo: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="364f5-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="364f5-108">`GeneratorIndex` representando um termo ZZ.</span><span class="sxs-lookup"><span data-stu-id="364f5-108">`GeneratorIndex` representing a ZZ term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="364f5-109">Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="364f5-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="364f5-110">' GeneratorIndex [] ' expressando o termo ZZ como termos de Pauli.</span><span class="sxs-lookup"><span data-stu-id="364f5-110">'GeneratorIndex[]' expressing ZZ term as Pauli terms.</span></span>