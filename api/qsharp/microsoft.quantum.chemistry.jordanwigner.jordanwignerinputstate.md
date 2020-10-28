---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState
title: Tipo definido pelo usuário JordanWignerInputState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerInputState
qsharp.summary: Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 171a2999ab8c73925d4624c565bfd41a4e73c99d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693695"
---
# <a name="jordanwignerinputstate-user-defined-type"></a>Tipo definido pelo usuário JordanWignerInputState

Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Agrupa [](https://nuget.org/packages/)


Formato dos dados passados de C# para Q # para representar a preparação do estado inicial o significado dos dados representados é determinado pelo algoritmo que o recebe.

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

