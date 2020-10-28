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
# <a name="hterm-user-defined-type"></a><span data-ttu-id="3bca2-102">Tipo definido pelo usuário HTerm</span><span class="sxs-lookup"><span data-stu-id="3bca2-102">HTerm user defined type</span></span>

<span data-ttu-id="3bca2-103">Namespace: [Microsoft. Quantum. química](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="3bca2-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="3bca2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3bca2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3bca2-105">Formato dos dados passados de C# para Q # para representar um termo de Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="3bca2-105">Format of data passed from C# to Q# to represent a term of the Hamiltonian.</span></span>
<span data-ttu-id="3bca2-106">O significado dos dados representados é determinado pelo algoritmo que o recebe.</span><span class="sxs-lookup"><span data-stu-id="3bca2-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype HTerm = (Int[], Double[]);
```

