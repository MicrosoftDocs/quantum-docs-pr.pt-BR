---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Função FunctionAsOperation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693628"
---
# <a name="functionasoperation-function"></a>Função FunctionAsOperation

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Agrupa [](https://nuget.org/packages/)


Converte funções em operações.

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a>Descrição

Dada uma função, retorna uma operação que chama essa função e que não faz mais nada.

## <a name="input"></a>Entrada

### <a name="fn--input---output"></a>FN: ' entrada-> ' saída

Uma função a ser convertida em uma operação.



## <a name="output--input--output"></a>Saída: ' entrada => ' saída 

Uma operação `op` que `op(input)` é idêntica a `fn(input)` para todos `input` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="input"></a>' Entrada

Tipo de entrada da função a ser convertida.
### <a name="output"></a>' Saída

Tipo de saída da função a ser convertida.

## <a name="remarks"></a>Comentários

Isso é útil principalmente para passar funções a funções ou operações que esperam uma operação como entrada.