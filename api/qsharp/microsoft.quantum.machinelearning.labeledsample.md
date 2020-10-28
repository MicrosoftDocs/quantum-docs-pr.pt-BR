---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Tipo definido pelo usuário LabeledSample
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: 8b4afa1eaf7ca69938b2606163cd1ec17a1ad80f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693317"
---
# <a name="labeledsample-user-defined-type"></a>Tipo definido pelo usuário LabeledSample

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Agrupa [](https://nuget.org/packages/)


Um exemplo, rotulado com uma classe à qual o exemplo pertence.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>Itens nomeados

### <a name="features--double"></a>Recursos: [Double](xref:microsoft.quantum.lang-ref.double)[]

Um vetor de recursos para o exemplo fornecido.
### <a name="label--int"></a>Rótulo: [int](xref:microsoft.quantum.lang-ref.int)

Um rótulo de número inteiro para a classe à qual este exemplo pertence.