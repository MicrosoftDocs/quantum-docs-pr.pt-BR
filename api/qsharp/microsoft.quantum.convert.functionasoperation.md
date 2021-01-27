---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Função FunctionAsOperation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: cf4f8c97bf38b3a64eb952d0a502bc21c29c579c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833834"
---
# <a name="functionasoperation-function"></a>Função FunctionAsOperation

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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