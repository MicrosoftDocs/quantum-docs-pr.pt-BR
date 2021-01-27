---
uid: Microsoft.Quantum.Synthesis.FlipMasks
title: Função FlipMasks
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FlipMasks
qsharp.summary: For every 2-level unitary calculates "flip mask", which denotes qubits which should be inverted before and after applying corresponding 1-qubit gate. For convenience prepends result with 0.
ms.openlocfilehash: ca0ce69b3353379a42cc109cebb32efe4e364825
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859116"
---
# <a name="flipmasks-function"></a>Função FlipMasks

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Para cada unitário de dois níveis, ele calcula "inverter máscara", que denota qubits que deve ser invertida antes e depois da aplicação da porta 1-qubit correspondente.
Para a conveniência, os preparadores resultam em 0.

```qsharp
function FlipMasks (decomposition : (Microsoft.Quantum.Math.Complex[][], Int, Int)[], allQubitsMask : Int) : Int[]
```


## <a name="input"></a>Entrada

### <a name="decomposition--complexintint"></a>decomposição: ([Complex](xref:Microsoft.Quantum.Math.Complex)[] [],[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []




### <a name="allqubitsmask--int"></a>allQubitsMask: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)[]

