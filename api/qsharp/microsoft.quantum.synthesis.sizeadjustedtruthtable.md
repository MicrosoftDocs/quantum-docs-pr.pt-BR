---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Função SizeAdjustedTruthTable
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 3480f022df7a289594b003f201d16d8bf7c29d7e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697090"
---
# <a name="sizeadjustedtruthtable-function"></a><span data-ttu-id="f817c-102">Função SizeAdjustedTruthTable</span><span class="sxs-lookup"><span data-stu-id="f817c-102">SizeAdjustedTruthTable function</span></span>

<span data-ttu-id="f817c-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f817c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f817c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f817c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f817c-105">Ajusta a tabela verdadeira da matriz de boolianos de acordo com o número de variáveis</span><span class="sxs-lookup"><span data-stu-id="f817c-105">Adjusts truth table from array of Booleans according to number of variables</span></span>

<span data-ttu-id="f817c-106">Uma nova matriz é retornada de comprimento `2^numVars` , possivelmente exigindo estender o `table` tamanho com `false` entradas ou truncando-a para os `2^numVars` elementos.</span><span class="sxs-lookup"><span data-stu-id="f817c-106">A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.</span></span>

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="f817c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f817c-107">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="f817c-108">tabela: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f817c-108">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="f817c-109">Verdade, tabela como matriz de valores da verdade</span><span class="sxs-lookup"><span data-stu-id="f817c-109">Truth table as array of truth values</span></span>


### <a name="numvars--int"></a><span data-ttu-id="f817c-110">numVars: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f817c-110">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f817c-111">Número de variáveis</span><span class="sxs-lookup"><span data-stu-id="f817c-111">Number of variables</span></span>



## <a name="output--bool"></a><span data-ttu-id="f817c-112">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f817c-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="f817c-113">Tabela da verdade ajustada por tamanho</span><span class="sxs-lookup"><span data-stu-id="f817c-113">Size adjusted truth table</span></span>