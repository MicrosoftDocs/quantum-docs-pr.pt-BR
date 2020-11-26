---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: Função HTermsToGenSys
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: 936e1bcc58b2f1af3bdb606884128c38d2f58867
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204106"
---
# <a name="htermstogensys-function"></a>Função HTermsToGenSys

Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)

Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Converte um Hamiltonian no `HTerm[]` formato de dados em um GeneratorSystem.

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Entrada

### <a name="data--hterm"></a>dados: [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]

Dados de entrada no `HTerm[]` formato.


### <a name="termtype--int"></a>termtype: [int](xref:microsoft.quantum.lang-ref.int)[]

Informações adicionais adicionadas ao GeneratorIndex.



## <a name="output--generatorsystem"></a>Saída: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Um GeneratorSystem que representa um Hamiltonian representado pela entrada `data` .