---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Operação IterateThroughCartesianPower
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 3a303d13c4a6f102dab92d814e24df9d90213fbe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840290"
---
# <a name="iteratethroughcartesianpower-operation"></a>Operação IterateThroughCartesianPower

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação para cada índice na potência cartesianas de um intervalo inteiro.

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Descrição

Aplica iterativamente uma operação para cada elemento de uma potência cartesianas do intervalo `0..(bound - 1)` .

## <a name="input"></a>Entrada

### <a name="power--int"></a>potência: [int](xref:microsoft.quantum.lang-ref.int)

O poder cartesiano para o qual o intervalo `0..(bound - 1)` deve ser gerado.


### <a name="bound--int"></a>associado: [int](xref:microsoft.quantum.lang-ref.int)

Uma especificação do intervalo a ser iterado, dado como o comprimento do intervalo.


### <a name="op--int--unit"></a>op: [int](xref:microsoft.quantum.lang-ref.int)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Uma operação a ser chamada para cada elemento da potência cartesianas fornecida.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Exemplo

Dada uma operação `op` , os dois trechos de código a seguir são equivalentes:

```qsharp
IterateThroughCartesianPower(2, 3, op);
```

```qsharp
op([0, 0]);
op([1, 0]);
op([2, 0]);
op([0, 1]);
// ..
op([2, 2]);
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. IterateThroughCartesianProduct](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)