---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Função TrotterStepSize
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: fabfbff74572b3c96c701de5443e4265a0468d78
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693873"
---
# <a name="trotterstepsize-function"></a>Função TrotterStepSize

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Computa o tamanho da etapa Trotter na implementação recursiva do algoritmo de simulação de Trotter.

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a>Entrada

### <a name="order--int"></a>ordem: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Comentários

Esta operação usa uma Convenção de indexação diferente da [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139). Em particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponde ao escalar $p _2 (\lambda) $ em Quant-pH/0508139.