---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Operação CarryOutCoreCDKM
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 19a692a3b54a413f25a474c361e773ab6c65579e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223537"
---
# <a name="carryoutcorecdkm-operation"></a>Operação CarryOutCoreCDKM

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


A operação principal no RippleCarryAdderCDKM, usada com a operação ApplyOuterCDKMAdder acima, ou seja, conjugada com essa operação para obter a operação interna do RippleCarryAdderCDKM. Esta operação computa o qubit de execução e aplica uma sequência de não Gates em parte da entrada `ys` .

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Primeiro registro de qubit.


### <a name="ys--littleendian"></a>haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Segundo registro de qubit.


### <a name="ancilla--qubit"></a>ancilla: [qubit](xref:microsoft.quantum.lang-ref.qubit)

O ancilla qubit usado em RippleCarryAdderCDKM passado para esta operação.


### <a name="carry--qubit"></a>transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Execute qubit na operação RippleCarryAdderCDKM.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referências

- Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A New Quantum-balcão de adição de", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1