---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Função HTermToGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: dd72355adb32f9a0d109ee36b24be2d445f3fa66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693817"
---
# <a name="htermtogenidx-function"></a>Função HTermToGenIdx

Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)

Agrupa [](https://nuget.org/packages/)


Converte um termo Hamiltonian no `HTerm` formato de dados em um GeneratorIndex.

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Entrada

### <a name="term--hterm"></a>termo: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)

Dados de entrada no `HTerm` formato.


### <a name="termtype--int"></a>termtype: [int](xref:microsoft.quantum.lang-ref.int)[]

Informações adicionais adicionadas ao GeneratorIndex.



## <a name="output--generatorindex"></a>Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Um GeneratorIndex que representa um termo Hamiltonian representado pelo `term` , junto com informações adicionais adicionadas pelo `termType` .