---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Função IdentityGeneratorIndex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: 2dd3c705b0496df1719dc677e4defea5e435b839
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229283"
---
# <a name="identitygeneratorindex-function"></a>Função IdentityGeneratorIndex

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna um índice de gerador consistente com o zero Hamiltonian, `H = 0` , que corresponde à operação de evolução da identidade.

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Entrada

### <a name="idxterm--int"></a>idxTerm: [int](xref:microsoft.quantum.lang-ref.int)

Essa entrada é ignorada e é definida para consistência com o <xref:microsoft.quantum.simulation.generatorsystem> tipo definido pelo usuário.



## <a name="output--generatorindex"></a>Saída: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Um índice de gerador que representa a evolução sob o Hamiltonian $H = $0.