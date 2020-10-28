---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: Função DumpMachine
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: c85cf6764bdc913a71448c525318f45743bf1df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693537"
---
# <a name="dumpmachine-function"></a><span data-ttu-id="80b3c-102">Função DumpMachine</span><span class="sxs-lookup"><span data-stu-id="80b3c-102">DumpMachine function</span></span>

<span data-ttu-id="80b3c-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="80b3c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="80b3c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80b3c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80b3c-105">Despeja o status do computador de destino atual.</span><span class="sxs-lookup"><span data-stu-id="80b3c-105">Dumps the current target machine's status.</span></span>

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="80b3c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="80b3c-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="80b3c-107">local: ' t</span><span class="sxs-lookup"><span data-stu-id="80b3c-107">location : 'T</span></span>

<span data-ttu-id="80b3c-108">Fornece informações sobre onde gerar o despejo da máquina.</span><span class="sxs-lookup"><span data-stu-id="80b3c-108">Provides information on where to generate the machine's dump.</span></span>



## <a name="output--unit"></a><span data-ttu-id="80b3c-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="80b3c-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="80b3c-110">nenhuma.</span><span class="sxs-lookup"><span data-stu-id="80b3c-110">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="80b3c-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="80b3c-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="80b3c-112">T'</span><span class="sxs-lookup"><span data-stu-id="80b3c-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="80b3c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="80b3c-113">Remarks</span></span>

<span data-ttu-id="80b3c-114">Esse método permite despejar informações sobre o status atual do computador de destino em um arquivo ou em algum outro local.</span><span class="sxs-lookup"><span data-stu-id="80b3c-114">This method allows you to dump information about the current status of the target machine into a file or some other location.</span></span>
<span data-ttu-id="80b3c-115">As informações reais geradas e a semântica de `location` são específicas para cada computador de destino.</span><span class="sxs-lookup"><span data-stu-id="80b3c-115">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="80b3c-116">No entanto, fornecer uma tupla vazia como um local ( `()` ) ou simplesmente omitir o `location` parâmetro normalmente significa gerar a saída para o console.</span><span class="sxs-lookup"><span data-stu-id="80b3c-116">However, providing an empty tuple as a location (`()`) or just omitting the `location` parameter typically means to generate the output to the console.</span></span>

<span data-ttu-id="80b3c-117">Para o simulador de estado completo local distribuído como parte do kit de desenvolvimento Quantum, esse método espera uma cadeia de caracteres com o caminho para um arquivo no qual ele gravará a função Wave como uma matriz unidimensional de números complexos, na qual cada elemento representa as amplitudes da probabilidade de medir o estado correspondente.</span><span class="sxs-lookup"><span data-stu-id="80b3c-117">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the wave function as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>