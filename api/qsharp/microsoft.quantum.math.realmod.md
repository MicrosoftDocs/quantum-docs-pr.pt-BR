---
uid: Microsoft.Quantum.Math.RealMod
title: Função RealMod
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848356"
---
# <a name="realmod-function"></a><span data-ttu-id="05b3b-102">Função RealMod</span><span class="sxs-lookup"><span data-stu-id="05b3b-102">RealMod function</span></span>

<span data-ttu-id="05b3b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="05b3b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="05b3b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="05b3b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="05b3b-105">Computa o módulo entre dois números reais.</span><span class="sxs-lookup"><span data-stu-id="05b3b-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="05b3b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="05b3b-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="05b3b-107">valor: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="05b3b-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="05b3b-108">Um número real $x $ para pegar o módulo de.</span><span class="sxs-lookup"><span data-stu-id="05b3b-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="05b3b-109">módulo: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="05b3b-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="05b3b-110">Um número real para pegar o módulo de $x $ com relação a.</span><span class="sxs-lookup"><span data-stu-id="05b3b-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="05b3b-111">minValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="05b3b-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="05b3b-112">O menor valor a ser retornado por essa função.</span><span class="sxs-lookup"><span data-stu-id="05b3b-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="05b3b-113">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="05b3b-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="example"></a><span data-ttu-id="05b3b-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="05b3b-114">Example</span></span>

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a><span data-ttu-id="05b3b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="05b3b-115">Remarks</span></span>

<span data-ttu-id="05b3b-116">Essa função computa o módulo real encapsulando a linha real sobre o círculo da unidade e, em seguida, localizando o ângulo no círculo da unidade correspondente à entrada.</span><span class="sxs-lookup"><span data-stu-id="05b3b-116">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="05b3b-117">`minValue`Em seguida, a entrada especifica efetivamente onde recortar o círculo da unidade.</span><span class="sxs-lookup"><span data-stu-id="05b3b-117">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>