---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Operação DrawMany
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: bf63ce308679cef97c776d3383ff732ed4d4e500
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846214"
---
# <a name="drawmany-operation"></a>Operação DrawMany

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Repete uma operação para um determinado número de amostras, coletando suas saídas em uma matriz.

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a>Entrada

### <a name="op--tinput--toutput"></a>op: ' TInput => ' TOutput 

A operação a ser chamada repetidamente.


### <a name="nsamples--int"></a>nSamples: [int](xref:microsoft.quantum.lang-ref.int)

O número de amostras de chamada `op` para Collect.


### <a name="input--tinput"></a>entrada: ' TInput

A entrada a ser passada para `op` .



## <a name="output--toutput"></a>Saída: ' TOutput []



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="tinput"></a>'TInput


### <a name="toutput"></a>'TOutput



## <a name="example"></a>Exemplo

O exemplo a seguir fornece um inteiro, dada uma operação que obtém um único bit por vez.

```qsharp
let randomInteger = BoolArrayAsInt(DrawMany(SampleRandomBit, 16, ()));
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. Repeat](xref:Microsoft.Quantum.Canon.Repeat)