---
uid: Microsoft.Quantum.Chemistry.HTerm
title: Tipo definido pelo usuário HTerm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 7a18db539e55e4c1086b3d83725e3d4ba87f0117
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693822"
---
# <a name="hterm-user-defined-type"></a>Tipo definido pelo usuário HTerm

Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)

Agrupa [](https://nuget.org/packages/)


Formato dos dados passados de C# para Q # para representar um termo de Hamiltonian.
O significado dos dados representados é determinado pelo algoritmo que o recebe.

```qsharp

newtype HTerm = (Int[], Double[]);
```

