---
uid: Microsoft.Quantum.Canon.BoundA
title: Função bounda
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3d0a5ba5d3d9c76289ed29e59a9c226358b83797
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844534"
---
# <a name="bounda-function"></a>Função bounda

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma matriz de operações que atuam em uma única entrada, o produz uma nova operação que executa cada operação específica em sequência.
O modificador `A` indica que todas as operações na matriz são adjointable.

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a>Entrada

### <a name="operations--t--unit--is-adj"></a>operações: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj []

Uma sequência de operações a ser executada em uma determinada entrada.



## <a name="output--t--unit--is-adj"></a>Saída: ' T' = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

Uma nova operação que executa cada operação específica em sequência em sua entrada.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual cada uma das operações na matriz atua.

## <a name="example"></a>Exemplo

Os itens a seguir são equivalentes:

```qsharp
let bound = BoundA([U, V]);
bound(x);
```

e

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. Bound](xref:Microsoft.Quantum.Canon.Bound)