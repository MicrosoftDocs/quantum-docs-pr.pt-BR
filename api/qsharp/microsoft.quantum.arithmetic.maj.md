---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Operação MAJ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 68236f1deeb409a01152d4b7e854202a1134314e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846540"
---
# <a name="maj-operation"></a>Operação MAJ

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Isso aplica a operação da maioria no local a 3 qubits.

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Se denotarmos o estado do qubit de destino como $ \ket{z} $ e os Estados de entrada da entrada qubits como $ \ket{x} $ e $ \ket{y} $, essa operação executará a seguinte transformação: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.

## <a name="input"></a>Entrada

### <a name="input0--qubit"></a>input0: [qubit](xref:microsoft.quantum.lang-ref.qubit)

O primeiro qubit de entrada.


### <a name="input1--qubit"></a>entrada1: [qubit](xref:microsoft.quantum.lang-ref.qubit)

O segundo qubit de entrada.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um qubit para o qual a função principal será aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

