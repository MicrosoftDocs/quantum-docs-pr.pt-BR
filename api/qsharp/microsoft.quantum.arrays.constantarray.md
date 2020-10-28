---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Função ConstantArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694500"
---
# <a name="constantarray-function"></a>Função ConstantArray

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


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

