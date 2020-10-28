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
# <a name="sizeadjustedtruthtable-function"></a>Função SizeAdjustedTruthTable

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Agrupa [](https://nuget.org/packages/)


Ajusta a tabela verdadeira da matriz de boolianos de acordo com o número de variáveis

Uma nova matriz é retornada de comprimento `2^numVars` , possivelmente exigindo estender o `table` tamanho com `false` entradas ou truncando-a para os `2^numVars` elementos.

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a>Entrada

### <a name="table--bool"></a>tabela: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Verdade, tabela como matriz de valores da verdade


### <a name="numvars--int"></a>numVars: [int](xref:microsoft.quantum.lang-ref.int)

Número de variáveis



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Tabela da verdade ajustada por tamanho