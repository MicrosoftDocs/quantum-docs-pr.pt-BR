---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Função SizeAdjustedTruthTable
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: c53ac3f2c46bca955847fc7b380337e3910390ac
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202916"
---
# <a name="sizeadjustedtruthtable-function"></a><span data-ttu-id="2f470-102">Função SizeAdjustedTruthTable</span><span class="sxs-lookup"><span data-stu-id="2f470-102">SizeAdjustedTruthTable function</span></span>

<span data-ttu-id="2f470-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="2f470-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="2f470-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2f470-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2f470-105">Ajusta a tabela verdadeira da matriz de boolianos de acordo com o número de variáveis</span><span class="sxs-lookup"><span data-stu-id="2f470-105">Adjusts truth table from array of Booleans according to number of variables</span></span>

<span data-ttu-id="2f470-106">Uma nova matriz é retornada de comprimento `2^numVars` , possivelmente exigindo estender o `table` tamanho com `false` entradas ou truncando-a para os `2^numVars` elementos.</span><span class="sxs-lookup"><span data-stu-id="2f470-106">A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.</span></span>

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="2f470-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f470-107">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="2f470-108">tabela: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="2f470-108">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="2f470-109">Verdade, tabela como matriz de valores da verdade</span><span class="sxs-lookup"><span data-stu-id="2f470-109">Truth table as array of truth values</span></span>


### <a name="numvars--int"></a><span data-ttu-id="2f470-110">numVars: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2f470-110">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2f470-111">Número de variáveis</span><span class="sxs-lookup"><span data-stu-id="2f470-111">Number of variables</span></span>



## <a name="output--bool"></a><span data-ttu-id="2f470-112">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="2f470-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="2f470-113">Tabela da verdade ajustada por tamanho</span><span class="sxs-lookup"><span data-stu-id="2f470-113">Size adjusted truth table</span></span>