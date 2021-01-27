---
uid: Microsoft.Quantum.Arrays.Zip4
title: Função Zip4
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip4
qsharp.summary: >-
  > [!WARNING]

  > Zip4 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.


  Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: 534721e6544a31f6f5d27db0c077e9d8c574aecd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850875"
---
# <a name="zip4-function"></a>Função Zip4

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Zip4 foi preterido. Use <xref:Microsoft.Quantum.Arrays.Zipped4> em seu lugar.

Dadas quatro matrizes, retorna uma nova matriz de 4 tuplas, de modo que cada 4 tupla contém um elemento de cada matriz original.

```qsharp
function Zip4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a>Entrada

### <a name="first--t1"></a>Primeiro: t 1 []

Uma matriz que contém valores para o primeiro elemento de cada tupla.


### <a name="second--t2"></a>Segundo: ' t 2 []

Uma matriz que contém valores para o segundo elemento de cada tupla.


### <a name="third--t3"></a>terceiro: ' t 3 []

Uma matriz que contém valores para o terceiro elemento de cada tupla.


### <a name="fourth--t4"></a>quarto: t 4 []

Uma matriz que contém valores para o quarto elemento de cada tupla.



## <a name="output--t1t2t3t4"></a>Saída: (t 1, não 2, ' T' 3, ' t 4) []

Uma matriz que contém 4 tuplas do formulário `(first[idx], second[idx], third[idx], fourth[idx])` para cada `idx` . Se as quatro matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t1"></a>Não 1

O tipo dos primeiros elementos da matriz.
### <a name="t2"></a>Não 2

O tipo da segunda matriz de elementos.
### <a name="t3"></a>' T 3

O tipo dos elementos da terceira matriz.
### <a name="t4"></a>' T 4

O tipo dos elementos da quarta matriz.

## <a name="see-also"></a>Consulte Também

- [Microsoft.Quantum.Arrays.Zip](xref:Microsoft.Quantum.Arrays.Zip)
- [Microsoft.Quantum.Arrays.Zip3](xref:Microsoft.Quantum.Arrays.Zip3)