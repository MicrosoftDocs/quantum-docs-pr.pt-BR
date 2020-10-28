---
uid: Microsoft.Quantum.Arrays.Unique
title: Função Unique
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: c5d40bb82f2de640e9c78eef0c27e4766b477826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694395"
---
# <a name="unique-function"></a>Função Unique

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Agrupa [](https://nuget.org/packages/)


Retorna uma nova matriz que não tem nenhum elemento adjacente igual.

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a>Descrição

Dada parte de uma matriz de elementos e uma função para testar a igualdade, essa função retorna uma nova matriz na qual a ordem relativa dos elementos é mantida, mas todos os elementos adjacentes que são iguais são filtrados para apenas um único elemento.

## <a name="input"></a>Entrada

### <a name="equal--tt---bool"></a>igual: (não, não)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Uma função que compara dois elementos, de modo que `a` é considerado igual a `b` If `equal(a, b)` is `true` .


### <a name="array--t"></a>matriz: ' t []

A matriz a ser filtrada para elementos exclusivos.



## <a name="output--t"></a>Saída: ' T' []

Matriz sem elementos adjacentes iguais.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de cada elemento de `array` .

## <a name="remarks"></a>Comentários

Se houver vários elementos que são iguais, mas não próximos um do outro, haverá várias ocorrências na matriz de saída.  Use essa função junto com `Sorted` para obter uma matriz com elementos exclusivos gerais.