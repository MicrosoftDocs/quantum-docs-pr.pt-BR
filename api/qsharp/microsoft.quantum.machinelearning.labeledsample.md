---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Tipo definido pelo usuário LabeledSample
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: b357aae20b5bddb968ce1906fed3c1001efbfde7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846971"
---
# <a name="labeledsample-user-defined-type"></a>Tipo definido pelo usuário LabeledSample

Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Um exemplo, rotulado com uma classe à qual o exemplo pertence.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>Itens nomeados

### <a name="features--double"></a>Recursos: [Double](xref:microsoft.quantum.lang-ref.double)[]

Um vetor de recursos para o exemplo fornecido.
### <a name="label--int"></a>Rótulo: [int](xref:microsoft.quantum.lang-ref.int)

Um rótulo de número inteiro para a classe à qual este exemplo pertence.