---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEC
title: Função ReversedOpLEC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEC
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 2dc6a596970f909af9c329dbe7002c165854cfec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846375"
---
# <a name="reversedoplec-function"></a>Função ReversedOpLEC

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação que usa uma entrada little-endian, retorna uma nova operação que usa uma entrada big endian.

```qsharp
function ReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)
```


## <a name="input"></a>Entrada

### <a name="op--littleendian--unit--is-ctl"></a>op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é CTL

A operação cuja entrada deve ser revertida.



## <a name="output--bigendian--unit--is-ctl"></a>Saída: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian é CTL

Uma nova operação que aceita sua entrada como um registro big endian.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. ApplyReversedOpLEC](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [Microsoft. Quantum. aritmético. ReversedOpLE](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Microsoft. Quantum. aritmético. ReversedOpLEA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [Microsoft. Quantum. aritmético. ReversedOpLECA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)