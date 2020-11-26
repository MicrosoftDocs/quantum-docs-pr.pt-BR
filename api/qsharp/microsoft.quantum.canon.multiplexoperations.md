---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Operação MultiplexOperations
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: ad66b39fcfacbe5231ec3b9ba96989d6d5d449c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206095"
---
# <a name="multiplexoperations-operation"></a>Operação MultiplexOperations

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma matriz de operações controladas por uma matriz de Estados de número.

Ou seja, aplica a operação unitário controlada por multiplicação $U $ que aplica um $V unitário _j $ quando controlado $n pelo estado do número $ qubit $ \ket{j} $.

$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="unitaries--t--unit--is-adj--ctl"></a>unidades: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL []

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