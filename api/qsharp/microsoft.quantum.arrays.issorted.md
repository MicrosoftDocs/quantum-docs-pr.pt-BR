---
uid: Microsoft.Quantum.Arrays.IsSorted
title: Função IsSorted
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: a5916b5cbf36e1b6c421a81e04016a333e2b5be7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845730"
---
# <a name="issorted-function"></a>Função IsSorted

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz, retorna se essa matriz é classificada conforme definido por uma determinada função de comparação.

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Entrada

### <a name="comparison--tt---bool"></a>comparação: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Uma função que compara dois elementos, de modo que `a` é considerado menor ou igual a `b` se `comparison(a, b)` for `true` .


### <a name="array--t"></a>matriz: ' t []

A matriz a ser verificada.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` se e somente se for para cada par de `a` elementos `b` e `array` ocorrer nessa ordem, `comparison(a, b)` será `true` .

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de cada elemento de `array` .

## <a name="remarks"></a>Comentários

Presume- `comparison` se que a função seja transitiva, de modo que, se `comparison(a, b)` e `comparison(b, c)` , `comparison(a, c)` for assumido. Se essa propriedade não for mantida, a saída dessa função poderá estar incorreta.