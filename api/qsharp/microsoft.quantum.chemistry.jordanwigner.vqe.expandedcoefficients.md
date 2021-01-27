---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Função ExpandedCoefficients
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: b953fb8f5737956e8597cd90a7d6bfc0bafce4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835613"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="bcda5-102">Função ExpandedCoefficients</span><span class="sxs-lookup"><span data-stu-id="bcda5-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="bcda5-103">Namespace: [Microsoft. Quantum. química. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="bcda5-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="bcda5-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="bcda5-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="bcda5-105">Expande a representação compacta dos coeficientes Jordan-Wigner para obter um mapeamento um-para-um entre esses e Pauli termos.</span><span class="sxs-lookup"><span data-stu-id="bcda5-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="bcda5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="bcda5-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="bcda5-107">coeff: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="bcda5-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="bcda5-108">Uma matriz de coeficientes, como lida da estrutura de dados do Jordan-Wigner Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="bcda5-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="bcda5-109">termtype: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bcda5-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bcda5-110">O tipo do termo de Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="bcda5-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="bcda5-111">Saída: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="bcda5-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="bcda5-112">Matrizes expandidas de coeficientes, uma por termo Pauli.</span><span class="sxs-lookup"><span data-stu-id="bcda5-112">Expanded arrays of coefficients, one per Pauli term.</span></span>