---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: Função DecomposedIntoTimeStepsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: cfd563c1c6350255364de1e227442624acc98c22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694032"
---
# <a name="decomposedintotimestepsca-function"></a>Função DecomposedIntoTimeStepsCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Retorna uma operação que implementa o integrador Trotter – Suzuki para uma determinada operação.

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Entrada

### <a name="nsteps--int"></a>nSteps: [int](xref:microsoft.quantum.lang-ref.int)

O número de operações a serem decompostas em etapas de tempo.


### <a name="op--intdoublet--unit-adj--ctl"></a>op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL

Uma operação que aceita uma entrada de índice (tipo `Int` ) e uma entrada de hora (tipo `Double` ) para decomposição.


### <a name="trotterorder--int"></a>trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)

Seleciona a ordem do Trotter – integrador de Suzuki a ser usado.
Ordem 1 e até mesmo pedidos 2, 4, 6,... atualmente têm suporte.



## <a name="output--doublet--unit-adj--ctl"></a>Saída: ([Double](xref:microsoft.quantum.lang-ref.double), ' t) => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL

Retorna um unitário que implementa o integrador Trotter – Suzuki, em que o primeiro parâmetro `Double` é o tamanho da etapa de integração e o segundo parâmetro é o destino.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo em que cada etapa de tempo deve agir; Normalmente, o `Qubit[]` ou o `Qubit` .

## <a name="remarks"></a>Comentários

Quando chamado com `order` igual a `1` , essa função retorna uma operação que pode ser simulada pelo Trotter de ordem mais baixa – integrador Suzuki $ $ \begin{align} S_1 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_j \lambda}, \end{align} $ $ em que seguimos a notação de [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139) e permitimos que $ \lambda $ seja o tempo de evolução (representado pela primeira entrada da operação retornada), e permitiu que $ \{ H_j \} _ {j = 1} ^ {m} $ seja o conjunto de geradores dinâmicos (distorção-Hermitian), que `op(j, lambda, _)` é simulado pelo operador unitário $e ^ {H_j \lambda} $.

Da mesma forma, um `order` de `2` retorna o Trotter simétrico de segunda ordem – integrador de Suzuki $ $ \begin{align} S_2 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_k \lambda/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \lambda/2}.
\end{align} $ $

Valores maiores iguais de `order` são implementados usando a construção recursiva de [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).

## <a name="references"></a>Referências

- [*D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders*](https://arxiv.org/abs/quant-ph/0508139)