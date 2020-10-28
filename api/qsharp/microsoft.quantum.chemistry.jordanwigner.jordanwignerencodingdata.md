---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData
title: Tipo definido pelo usuário JordanWignerEncodingData
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerEncodingData
qsharp.summary: Format of data passed from C# to Q# to represent all information for Hamiltonian simulation. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 62988eefa57d8a9e4ed9dcfbdbc6c3b630c6faa2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693705"
---
# <a name="jordanwignerencodingdata-user-defined-type"></a><span data-ttu-id="6b76d-102">Tipo definido pelo usuário JordanWignerEncodingData</span><span class="sxs-lookup"><span data-stu-id="6b76d-102">JordanWignerEncodingData user defined type</span></span>

<span data-ttu-id="6b76d-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="6b76d-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="6b76d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6b76d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6b76d-105">Formato dos dados passados de C# para Q # para representar todas as informações para a simulação de Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="6b76d-105">Format of data passed from C# to Q# to represent all information for Hamiltonian simulation.</span></span>
<span data-ttu-id="6b76d-106">O significado dos dados representados é determinado pelo algoritmo que o recebe.</span><span class="sxs-lookup"><span data-stu-id="6b76d-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JordanWignerEncodingData = (Int, Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms, (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), Double);
```

