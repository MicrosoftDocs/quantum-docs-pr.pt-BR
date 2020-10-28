---
uid: Microsoft.Quantum.Preparation.ApplyToLittleEndian
title: Operação ApplyToLittleEndian
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApplyToLittleEndian
qsharp.summary: Applies an operation to the underlying qubits making up a little-endian register. This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.
ms.openlocfilehash: d94a9969a3f827d594946ab8ca6cd4672da7ef7e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696895"
---
# <a name="applytolittleendian-operation"></a>Operação ApplyToLittleEndian

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Agrupa [](https://nuget.org/packages/)


Aplica uma operação ao qubits subjacente que faz um registro little-endian. Essa operação é marcada como interna, já que um registro little-endian deve ser "opaco", de modo que esse é apenas um detalhe de implementação.

```qsharp
operation ApplyToLittleEndian (bareOp : (Qubit[] => Unit is Adj + Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Entrada

### <a name="bareop--qubit--unit-adj--ctl"></a>bareOp: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit) do ano + CTL




### <a name="register--littleendian"></a>registrar: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

