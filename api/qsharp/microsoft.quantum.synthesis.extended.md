---
uid: Microsoft.Quantum.Synthesis.Extended
title: Função estendida
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855465"
---
# <a name="extended-function"></a><span data-ttu-id="813ad-102">Função estendida</span><span class="sxs-lookup"><span data-stu-id="813ad-102">Extended function</span></span>

<span data-ttu-id="813ad-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="813ad-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="813ad-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="813ad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="813ad-105">Estende um espectro por coeficientes invertidos</span><span class="sxs-lookup"><span data-stu-id="813ad-105">Extends a spectrum by inverted coefficients</span></span>

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="813ad-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="813ad-106">Input</span></span>

### <a name="spectrum--int"></a><span data-ttu-id="813ad-107">espectro: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="813ad-107">spectrum : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="813ad-108">Coeficientes Spectral</span><span class="sxs-lookup"><span data-stu-id="813ad-108">Spectral coefficients</span></span>



## <a name="output--int"></a><span data-ttu-id="813ad-109">Saída: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="813ad-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="813ad-110">Coeficientes seguido por cópia invertida</span><span class="sxs-lookup"><span data-stu-id="813ad-110">Coefficients followed by inverted copy</span></span>

## <a name="example"></a><span data-ttu-id="813ad-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="813ad-111">Example</span></span>

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```