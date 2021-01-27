---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Operação PrepareUniformSuperposition
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: dc9d4ce1638b397748cafaa757241ce78633c67c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854313"
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



## <a name="example"></a>Exemplo

O exemplo a seguir prepara o estado $ \frac {1} {\sqrt {6} } \ sum_ {j = 0} ^ {5} \ket{j} $ em $3 $ qubits.

```qsharp
let nIndices = 6;
using(indexRegister = Qubit[3]) {
    PrepareUniformSuperposition(nIndices, LittleEndian(indexRegister));
    // ...
}
```

## <a name="remarks"></a>Comentários

A operação é adjointable, mas requer que `indexRegister` esteja em uma superposição uniforme nos Estados da primeira `nIndices` base nesse caso.