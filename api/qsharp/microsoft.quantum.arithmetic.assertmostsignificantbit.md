---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Operação AssertMostSignificantBit
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 41381455d1a96970647f887e038f7dff3a4eb204
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223775"
---
# <a name="assertmostsignificantbit-operation"></a>Operação AssertMostSignificantBit

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que o qubit mais significativo de um registro de qubit que representa um inteiro não assinado está em um estado específico.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="value--__invalidresult__"></a>valor: __inválido <Result>__

O valor do maior bit que está sendo declarado.


### <a name="number--littleendian"></a>número: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Inteiro sem sinal do qual o bit mais alto está marcado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

A versão controlada dessa operação ignora os controles.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. intrínseca. Assert](xref:Microsoft.Quantum.Intrinsic.Assert)