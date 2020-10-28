---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Função ExpandedCoefficients
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 8f5a2319b5839d0d9e47972389330dc16dffcaf0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693657"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="06788-102">Função ExpandedCoefficients</span><span class="sxs-lookup"><span data-stu-id="06788-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="06788-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="06788-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="06788-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06788-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06788-105">Expande a representação compacta dos coeficientes Jordan-Wigner para obter um mapeamento um-para-um entre esses e Pauli termos.</span><span class="sxs-lookup"><span data-stu-id="06788-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="06788-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="06788-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="06788-107">coeff: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="06788-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="06788-108">Uma matriz de coeficientes, como lida da estrutura de dados do Jordan-Wigner Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="06788-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="06788-109">termtype: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="06788-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="06788-110">O tipo do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="06788-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="06788-111">Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="06788-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="06788-112">Matrizes expandidas de coeficientes, uma por termo Pauli.</span><span class="sxs-lookup"><span data-stu-id="06788-112">Expanded arrays of coefficients, one per Pauli term.</span></span>