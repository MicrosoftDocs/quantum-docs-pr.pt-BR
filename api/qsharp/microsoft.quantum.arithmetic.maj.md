---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Operação MAJ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 356689baa6d47b7b93a393f3672991bb589f6921
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222755"
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

