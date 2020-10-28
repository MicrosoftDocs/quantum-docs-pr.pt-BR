---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Operação MultiplexOperations
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 267c9c2858090ebe024fd387938e8bd2f8c76867
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693960"
---
# <a name="multiplexoperations-operation"></a>Operação MultiplexOperations

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Aplica uma matriz de operações controladas por uma matriz de Estados de número.

Ou seja, aplica a operação unitário controlada por multiplicação $U $ que aplica um $V unitário _j $ quando controlado $n pelo estado do número $ qubit $ \ket{j} $.

$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a>Entrada

### <a name="unitaries--t--unit-adj--ctl"></a>unidades: não => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL []

Matriz de até $2 ^ n $ operações de unitário. A operação $j $ th é indexada pelo estado do número $ \ket{j} $ codificado em um formato little-endian.


### <a name="index--littleendian"></a>índice: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.


### <a name="target--t"></a>destino: ' t

Registro de qubit genérico que $V _j $ age em.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

`coefficients` será preenchido com elementos de identidade se menos de $2 ^ n $ forem especificados. Essa implementação usa $n auxiliar qubits-$1.

## <a name="references"></a>Referências

- Para a primeira simulação de Quantum com aumento de velocidade Quantum Andrew M. Childs, Dmitri Maslov, Yunseong, Neil J. Ross, iuan Su https://arxiv.org/abs/1711.10980