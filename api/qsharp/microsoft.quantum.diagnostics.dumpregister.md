---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: Função DumpRegister
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: a6d29dbf0525077fd804563f85f189740fdc0429
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693532"
---
# <a name="dumpregister-function"></a><span data-ttu-id="74d59-102">Função DumpRegister</span><span class="sxs-lookup"><span data-stu-id="74d59-102">DumpRegister function</span></span>

<span data-ttu-id="74d59-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="74d59-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="74d59-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="74d59-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="74d59-105">Despeja o status atual da máquina de destino associada ao qubits fornecido.</span><span class="sxs-lookup"><span data-stu-id="74d59-105">Dumps the current target machine's status associated with the given qubits.</span></span>

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="74d59-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="74d59-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="74d59-107">local: ' t</span><span class="sxs-lookup"><span data-stu-id="74d59-107">location : 'T</span></span>

<span data-ttu-id="74d59-108">Fornece informações sobre onde gerar o despejo do estado.</span><span class="sxs-lookup"><span data-stu-id="74d59-108">Provides information on where to generate the state's dump.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="74d59-109">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="74d59-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="74d59-110">A lista de qubits a ser reportada.</span><span class="sxs-lookup"><span data-stu-id="74d59-110">The list of qubits to report.</span></span>



## <a name="output--unit"></a><span data-ttu-id="74d59-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74d59-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="74d59-112">nenhuma.</span><span class="sxs-lookup"><span data-stu-id="74d59-112">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="74d59-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="74d59-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="74d59-114">T'</span><span class="sxs-lookup"><span data-stu-id="74d59-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="74d59-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="74d59-115">Remarks</span></span>

<span data-ttu-id="74d59-116">Esse método permite que você despeje as informações associadas ao estado do determinado qubits em um arquivo ou em algum outro local.</span><span class="sxs-lookup"><span data-stu-id="74d59-116">This method allows you to dump the information associated with the state of the given qubits into a file or some other location.</span></span>
<span data-ttu-id="74d59-117">As informações reais geradas e a semântica de `location` são específicas para cada computador de destino.</span><span class="sxs-lookup"><span data-stu-id="74d59-117">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="74d59-118">No entanto, fornecer uma tupla vazia como um local ( `()` ) normalmente significa gerar a saída para o console.</span><span class="sxs-lookup"><span data-stu-id="74d59-118">However, providing an empty tuple as a location (`()`) typically means to generate the output to the console.</span></span>

<span data-ttu-id="74d59-119">Para o simulador de estado completo local distribuído como parte do kit de desenvolvimento Quantum, esse método espera uma cadeia de caracteres com o caminho para um arquivo no qual ele gravará o estado de determinado qubits (ou seja, a função Wave do subsistema correspondente) como uma matriz unidimensional de números complexos, na qual cada elemento representa as amplitudes da probabilidade de medir o estado correspondente.</span><span class="sxs-lookup"><span data-stu-id="74d59-119">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the state of the given qubits (i.e. the wave function of the corresponding  subsystem) as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>
<span data-ttu-id="74d59-120">Se o qubits fornecido for confusas com algum outro qubit e seu estado não puder ser separado, ele apenas relatará que o qubits é confusas.</span><span class="sxs-lookup"><span data-stu-id="74d59-120">If the given qubits are entangled with some other qubit and their state can't be separated, it just reports that the qubits are entangled.</span></span>