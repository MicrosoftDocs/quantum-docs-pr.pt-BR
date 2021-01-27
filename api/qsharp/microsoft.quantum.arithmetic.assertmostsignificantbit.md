---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Operação AssertMostSignificantBit
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: b0b52a4ba7492d68896669aeb0b6b550d2f27f64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843417"
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