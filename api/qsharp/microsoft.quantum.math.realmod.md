---
uid: Microsoft.Quantum.Math.RealMod
title: Função RealMod
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 6ec799885bd2f0d35314ed727356499efbe9fcf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694665"
---
# <a name="realmod-function"></a><span data-ttu-id="0d28a-102">Função RealMod</span><span class="sxs-lookup"><span data-stu-id="0d28a-102">RealMod function</span></span>

<span data-ttu-id="0d28a-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="0d28a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="0d28a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0d28a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0d28a-105">Computa o módulo entre dois números reais.</span><span class="sxs-lookup"><span data-stu-id="0d28a-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="0d28a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d28a-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="0d28a-107">valor: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0d28a-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0d28a-108">Um número real $x $ para pegar o módulo de.</span><span class="sxs-lookup"><span data-stu-id="0d28a-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="0d28a-109">módulo: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0d28a-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0d28a-110">Um número real para pegar o módulo de $x $ com relação a.</span><span class="sxs-lookup"><span data-stu-id="0d28a-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="0d28a-111">minValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0d28a-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0d28a-112">O menor valor a ser retornado por essa função.</span><span class="sxs-lookup"><span data-stu-id="0d28a-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="0d28a-113">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0d28a-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="0d28a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d28a-114">Remarks</span></span>

<span data-ttu-id="0d28a-115">Essa função computa o módulo real encapsulando a linha real sobre o círculo da unidade e, em seguida, localizando o ângulo no círculo da unidade correspondente à entrada.</span><span class="sxs-lookup"><span data-stu-id="0d28a-115">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="0d28a-116">`minValue`Em seguida, a entrada especifica efetivamente onde recortar o círculo da unidade.</span><span class="sxs-lookup"><span data-stu-id="0d28a-116">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>