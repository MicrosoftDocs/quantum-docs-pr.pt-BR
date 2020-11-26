---
uid: Microsoft.Quantum.Arrays.Zip
title: Função zip
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 44db8d38d96babd16ead5ae6dde91da23bdee2c9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219848"
---
# <a name="zip-function"></a>Função zip

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> O zip foi preterido. Use <xref:Microsoft.Quantum.Arrays.Zipped> em seu lugar.

Dadas duas matrizes, retorna uma nova matriz de pares, de modo que cada par contém um elemento de cada matriz original.

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a>Entrada

### <a name="left--t"></a>esquerda: ' t []

Uma matriz que contém valores para o primeiro elemento de cada tupla.


### <a name="right--u"></a>direita: ' U []

Uma matriz que contém valores para o segundo elemento de cada tupla.



## <a name="output--tu"></a>Saída: (t, ' U) []

Uma matriz que contém pares do formulário `(left[idx], right[idx])` para cada `idx` . Se as duas matrizes não forem de comprimento igual, a saída será consumida quanto a menor das entradas.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo dos elementos da matriz esquerda.
### <a name="u"></a>' U

O tipo dos elementos da matriz direita.

## <a name="see-also"></a>Consulte Também

- [Microsoft.Quantum.Arrays.Zip3](xref:Microsoft.Quantum.Arrays.Zip3)
- [Microsoft.Quantum.Arrays.Zip4](xref:Microsoft.Quantum.Arrays.Zip4)
- [Microsoft. Quantum. arrays. descompactado](xref:Microsoft.Quantum.Arrays.Unzipped)