---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Operação quadrada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 6813c8144b0ac98bae404b5e9b97e08b06c6bb3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846307"
---
# <a name="squarei-operation"></a>Operação quadrada

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Computa o quadrado do inteiro `xs` em `result` , que deve ser inicialmente zero.

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

número de $n de $ bits para quadrado (LittleEndian)


### <a name="result--littleendian"></a>resultado: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

o resultado de $2n $-bit (LittleEndian) deve estar no estado $ \ket {0} $ inicialmente.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Usa uma abordagem Shift-and-add padrão para calcular o quadrado. Salva $n-$1 qubits em comparação com a solução direta, que primeiro copia XS antes de aplicar um multiplicador regular e, em seguida, desfazendo a operação de cópia.