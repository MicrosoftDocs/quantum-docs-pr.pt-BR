---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEA
title: Função ReversedOpLEA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: b0fcf1c735bb19308a381307e64314d9d961e5da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846421"
---
# <a name="reversedoplea-function"></a>Função ReversedOpLEA

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação que usa uma entrada little-endian, retorna uma nova operação que usa uma entrada big endian.

```qsharp
function ReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)
```


## <a name="input"></a>Entrada

### <a name="op--littleendian--unit--is-adj"></a>op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj

A operação cuja entrada deve ser revertida.



## <a name="output--bigendian--unit--is-adj"></a>Saída: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian é adj

Uma nova operação que aceita sua entrada como um registro big endian.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. ApplyReversedOpLEA](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [Microsoft. Quantum. aritmético. ReversedOpLE](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Microsoft. Quantum. aritmético. ReversedOpLEC](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [Microsoft. Quantum. aritmético. ReversedOpLECA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)