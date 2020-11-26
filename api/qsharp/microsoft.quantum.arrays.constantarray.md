---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Função ConstantArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 8cba68af2f1e178a1ef96921283f85e4feb498ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210056"
---
# <a name="constantarray-function"></a>Função ConstantArray

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Cria uma matriz de comprimento determinado com todos os elementos iguais ao valor fornecido.

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a>Entrada

### <a name="length--int"></a>comprimento: [int](xref:microsoft.quantum.lang-ref.int)

Comprimento da nova matriz.


### <a name="value--t"></a>valor: ' t

O valor de cada elemento da nova matriz.



## <a name="output--t"></a>Saída: ' T' []

Uma nova matriz de comprimento `length` , de modo que cada elemento é `value` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

