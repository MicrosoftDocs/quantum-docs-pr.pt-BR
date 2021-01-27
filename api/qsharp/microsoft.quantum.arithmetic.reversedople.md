---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLE
title: Função ReversedOpLE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLE
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d02817e5372b841f3ab633cafa22af603c5310c2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846388"
---
# <a name="reversedople-function"></a>Função ReversedOpLE

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação que usa uma entrada little-endian, retorna uma nova operação que usa uma entrada big endian.

```qsharp
function ReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)
```


## <a name="input"></a>Entrada

### <a name="op--littleendian--unit"></a>op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian 

A operação cuja entrada deve ser revertida.



## <a name="output--bigendian--unit"></a>Saída: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) BigEndian 

Uma nova operação que aceita sua entrada como um registro big endian.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. aritmético. ApplyReversedOpLE](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [Microsoft. Quantum. aritmético. ReversedOpLEA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [Microsoft. Quantum. aritmético. ReversedOpLEC](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [Microsoft. Quantum. aritmético. ReversedOpLECA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)