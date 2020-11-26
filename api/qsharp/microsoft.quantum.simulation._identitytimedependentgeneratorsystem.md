---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Função _IdentityTimeDependentGeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 7b93a6674bec974e61496696a3d8403225b16d80
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225594"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a>Função _IdentityTimeDependentGeneratorSystem

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna um sistema gerador consistente com o Hamiltonian `H(s) = 0` , em que `s` é um parâmetro de agendamento.

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Entrada

### <a name="schedule--double"></a>agendamento: [duplo](xref:microsoft.quantum.lang-ref.double)

Essa entrada é ignorada e é definida para consistência com o <xref:microsoft.quantum.canon.timedependentgeneratorsystem> tipo definido pelo usuário.



## <a name="output--generatorsystem"></a>Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Um sistema gerador que representa a evolução nas $H Hamiltonian = $0 para todos os $s $.