---
uid: Microsoft.Quantum.Convert.Call
title: Operação de chamada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 93458d08aa83ffa8b7b33de8bf51c970af291db9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850206"
---
# <a name="call-operation"></a>Operação de chamada

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Chama uma função com uma determinada entrada.

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a>Descrição

Dada uma função e uma entrada para essa função, o chama a função e retorna sua saída.

## <a name="input"></a>Entrada

### <a name="fn--input---output"></a>FN: ' entrada-> ' saída

Uma função a ser chamada.


### <a name="input--input"></a>entrada: ' entrada

A entrada a ser passada para a função.



## <a name="output--output"></a>Saída: ' saída

O resultado da chamada para `fn`.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="input"></a>' Entrada


### <a name="output"></a>' Saída



## <a name="remarks"></a>Comentários

Essa operação é útil principalmente para forçar a chamada de uma função em um local específico dentro de uma operação ou para chamar uma função em que uma operação é esperada.