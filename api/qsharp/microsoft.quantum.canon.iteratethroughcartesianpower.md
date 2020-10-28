---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Operação IterateThroughCartesianPower
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693987"
---
# <a name="iteratethroughcartesianpower-operation"></a>Operação IterateThroughCartesianPower

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


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



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. IterateThroughCartesianProduct](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)