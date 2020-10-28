---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Operação AssertMostSignificantBit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694828"
---
# <a name="assertmostsignificantbit-operation"></a>Operação AssertMostSignificantBit

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Agrupa [](https://nuget.org/packages/)


Declara que o qubit mais significativo de um registro de qubit que representa um inteiro não assinado está em um estado específico.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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