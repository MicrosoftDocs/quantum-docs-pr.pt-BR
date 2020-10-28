---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Função EqualityWithinToleranceFact
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693519"
---
# <a name="equalitywithintolerancefact-function"></a>Função EqualityWithinToleranceFact

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Agrupa [](https://nuget.org/packages/)


Representa a declaração de que um valor de ponto flutuante clássico tem o valor esperado até uma determinada tolerância absoluta.

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a>Entrada

### <a name="actual--double"></a>real: [duplo](xref:microsoft.quantum.lang-ref.double)

O número a ser verificado.


### <a name="expected--double"></a>esperado: [duplo](xref:microsoft.quantum.lang-ref.double)

O valor esperado.


### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

Tolerância absoluta na diferença entre real e esperado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

