---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationC
title: Operação ApplyWithInputTransformationC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationC
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 030c41d3ce0a5d613a95c6511f7278497ec5cda1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217162"
---
# <a name="applywithinputtransformationc-operation"></a>Operação ApplyWithInputTransformationC

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação que aceita alguma entrada, uma função que retorna uma saída compatível com essa operação e uma entrada para essa função, aplica a operação usando a função para transformar a entrada em um formato esperado pela operação.

```qsharp
operation ApplyWithInputTransformationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl), input : 'U) : Unit is Ctl
```


## <a name="input"></a>Entrada

### <a name="fn--u---t"></a>FN: ' U-> ' t

Uma função que transforma a entrada fornecida em um formulário esperado pela operação.


### <a name="op--t--unit--is-ctl"></a>op: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é CTL

A operação a ser aplicada.


### <a name="input--u"></a>entrada: ' U

Uma entrada para a função.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'


### <a name="u"></a>' U



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyWithInputTransformation](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. Quantum. Canon. ApplyWithInputTransformationA](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [Microsoft. Quantum. Canon. ApplyWithInputTransformationCA](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [Microsoft. Quantum. Canon. TransformedOperation](xref:Microsoft.Quantum.Canon.TransformedOperation)