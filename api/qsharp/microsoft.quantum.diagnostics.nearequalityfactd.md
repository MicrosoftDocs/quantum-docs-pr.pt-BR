---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Função NearEqualityFactD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: d632a7a12c9ebbebfbc7939f2b8a24de8ae1ba2a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827901"
---
# <a name="nearequalityfactd-function"></a>Função NearEqualityFactD

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que um valor de ponto flutuante clássico tem o valor esperado até uma pequena tolerância de 1e-10.

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a>Entrada

### <a name="actual--double"></a>real: [duplo](xref:microsoft.quantum.lang-ref.double)

O número a ser verificado.


### <a name="expected--double"></a>esperado: [duplo](xref:microsoft.quantum.lang-ref.double)

O valor esperado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Isso é equivalente a <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> com a tolerância codificada de $10 ^ {-10} $.