---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Operação PrepareUniformSuperposition
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 9b9f182ed7c1ea24ae74b8a2321a309042a17c97
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230082"
---
# <a name="prepareuniformsuperposition-operation"></a>Operação PrepareUniformSuperposition

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Cria uma superposição uniforme em Estados que codificam 0 a `nIndices - 1` .

Ou seja, esse unitário $U $ cria uma superposição uniforme em todos os Estados de número $0 $ para $M-$1, dado um estado de entrada $ \ket{0\cdots 0} $. Em outras palavras, $ $ \begin{align} U\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.
\end{align} $ $.

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="nindices--int"></a>nIndices: [int](xref:microsoft.quantum.lang-ref.int)

O número desejado de Estados $M $ na superposição uniforme.


### <a name="indexregister--littleendian"></a>indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

O registro qubit que armazena os Estados de número no `LittleEndian` formato.
Esse registro deve ser capaz de armazenar o número $M-$1 e presume-se que seja inicializado no estado $ \ket{0\cdots 0} $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

A operação é adjointable, mas requer que `indexRegister` esteja em uma superposição uniforme nos Estados da primeira `nIndices` base nesse caso.