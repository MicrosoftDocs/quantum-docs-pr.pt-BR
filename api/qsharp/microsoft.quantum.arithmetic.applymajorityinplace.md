---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Operação ApplyMajorityInPlace
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 3664ffe96cd1db8cf5e8898387fe7f2d45b4ea98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694864"
---
# <a name="applymajorityinplace-operation"></a>Operação ApplyMajorityInPlace

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Agrupa [](https://nuget.org/packages/)


Aplica a operação de maioria qubit no local em um registro de qubits.

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit
```


## <a name="description"></a>Descrição

Esta operação computa a função principal in-loco em 3 qubits.

Se denotarmos qubit de saída como $z $ e qubits de entrada como $x $ e $y $, a operação executará a seguinte transformação: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.

## <a name="input"></a>Entrada

### <a name="output--qubit"></a>saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Primeiro qubit de entrada. Observe que a saída é calculada in-loco e armazenada neste qubit.


### <a name="input--qubit"></a>entrada: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Segundo e terceiro qubits de entrada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

