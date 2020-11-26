---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Operação por
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 9a90d15defd57cf2836a6fda5b52ddaa816fd55e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191016"
---
# <a name="addi-operation"></a>Operação por

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Escolhe automaticamente entre adição e sem, dependendo do tamanho do registro de `ys` .

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n o adendo de $ bit.


### <a name="ys--littleendian"></a>haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Adendo com pelo menos $n $ qubits. Manterá o resultado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

