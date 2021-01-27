---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: Função ReversedOpBEC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 0674567f5d45890aa2f631b2e0e4d75d20a72449
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846444"
---
# <a name="reversedopbec-function"></a>Função ReversedOpBEC

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação que usa uma entrada big-endian, retorna uma nova operação que usa uma entrada little-endian.

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="op--bigendian--unit--is-ctl"></a>op: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian é CTL

A operação cuja entrada deve ser revertida.



## <a name="output--littleendian--unit--is-ctl"></a>Saída: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é CTL

Uma nova operação que aceita sua entrada como um registro little-endian.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. ApplyReversedOpBEC](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [Microsoft. Quantum. aritmético. ReversedOpBE](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [Microsoft. Quantum. aritmético. ReversedOpBEA](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [Microsoft. Quantum. aritmético. ReversedOpBECA](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)