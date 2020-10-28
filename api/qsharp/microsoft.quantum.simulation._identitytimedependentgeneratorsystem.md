---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: Função _IdentityTimeDependentGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 0b440ce9adaab562e16b02da46844c68a7470b11
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693225"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a>Função _IdentityTimeDependentGeneratorSystem

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Agrupa [](https://nuget.org/packages/)


Retorna um sistema gerador consistente com o Hamiltonian `H(s) = 0` , em que `s` é um parâmetro de agendamento.

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Entrada

### <a name="schedule--double"></a>agendamento: [duplo](xref:microsoft.quantum.lang-ref.double)

Essa entrada é ignorada e é definida para consistência com o <xref:microsoft.quantum.canon.timedependentgeneratorsystem> tipo definido pelo usuário.



## <a name="output--generatorsystem"></a>Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Um sistema gerador que representa a evolução nas $H Hamiltonian = $0 para todos os $s $.