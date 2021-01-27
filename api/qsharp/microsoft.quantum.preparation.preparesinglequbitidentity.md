---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: Operação PrepareSingleQubitIdentity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: c6c9b5724354d6ee034dd8b6733901ebdd8072d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856861"
---
# <a name="preparesinglequbitidentity-operation"></a>Operação PrepareSingleQubitIdentity

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Prepara um qubit no estado máximo misto.

Ele prepara o determinado qubit no estado $ \boldone/$2 aplicando o \rho de despolarização do canal $ $ \begin{align} \Omega (\mathrel{): =} \frac {1} {4} \ sum_ {\mu na \{ 0, 1, 2, 3 \} } \sigma \_ {\mu} \rho \sigma \_ {\mu} ^ {\dagger}, \end{Align} $ $, em que $ \sigma \_ i $ é o operador $i $ th Pauli e em que $ \rho $ é um operador de densidade que representa um estado misto.

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a>Entrada

### <a name="qubit--qubit"></a>qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um qubit cujo estado deve ser depolarizado da maneira descrita acima.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

O estado misto $ \boldone/$2 que descreve o resultado da aplicação dessa operação a um estado descreve implicitamente um valor de expectativa sobre as escolhas aleatórias feitas nesta operação.
Portanto, para qualquer aplicativo único, essa operação mapeia Estados puros para Estados puros, mas atua conforme descrito em expectativa.
Em particular, essa operação pode ser usada no processo tomography para medir os componentes *não-unitários* de um canal.