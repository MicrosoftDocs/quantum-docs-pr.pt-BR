---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdder
title: Operação ApplyInnerTTKAdder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdder
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 1de0248066aec531d78130703414067603ffd34d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190999"
---
# <a name="applyinnerttkadder-operation"></a>Operação ApplyInnerTTKAdder

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementa a função de adição interna para a operação RippleCarryAdderTTK. Essa é a operação interna que está conjugada com a operação externa para construir o adicionador completo.

```qsharp
operation ApplyInnerTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian qubit registrar o primeiro inteiro soma entrada para RippleCarryAdderTTK.


### <a name="ys--littleendian"></a>haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian qubit registrar o segundo inteiro soma entrada para RippleCarryAdderTTK.


### <a name="carry--qubit"></a>transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit, é XORed com o bit mais significativo da soma.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

A operação controlada especificada faz uso de simetria e cancelamento mútuo de operações para melhorar a implementação padrão que adiciona um controle a cada operação.

## <a name="references"></a>Referências

- Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "circuitos de adição Quantum e Fan-out não vinculado", informações de Quantum e computação, Vol. 10, 2010.
  https://arxiv.org/abs/0910.2530