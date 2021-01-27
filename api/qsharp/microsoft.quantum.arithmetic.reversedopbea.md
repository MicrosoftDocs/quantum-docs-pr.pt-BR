---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEA
title: Função ReversedOpBEA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 392b97171bcfb9d35a38189fc9c27e61cf9cf7d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846465"
---
# <a name="reversedopbea-function"></a>Função ReversedOpBEA

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação que usa uma entrada big-endian, retorna uma nova operação que usa uma entrada little-endian.

```qsharp
function ReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)
```


## <a name="input"></a>Entrada

### <a name="op--bigendian--unit--is-adj"></a>op: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian é adj

A operação cuja entrada deve ser revertida.



## <a name="output--littleendian--unit--is-adj"></a>Saída: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj

Uma nova operação que aceita sua entrada como um registro little-endian.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. ApplyReversedOpBEA](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [Microsoft. Quantum. aritmético. ReversedOpBE](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [Microsoft. Quantum. aritmético. ReversedOpBEC](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [Microsoft. Quantum. aritmético. ReversedOpBECA](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)