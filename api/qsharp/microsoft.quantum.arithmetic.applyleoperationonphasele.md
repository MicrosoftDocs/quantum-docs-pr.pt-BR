---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLE
title: Operação ApplyLEOperationOnPhaseLE
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 33e6cb81916737bf5db467e10fd2aeebb619116a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190897"
---
# <a name="applyleoperationonphasele-operation"></a><span data-ttu-id="28f91-102">Operação ApplyLEOperationOnPhaseLE</span><span class="sxs-lookup"><span data-stu-id="28f91-102">ApplyLEOperationOnPhaseLE operation</span></span>

<span data-ttu-id="28f91-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="28f91-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="28f91-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="28f91-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="28f91-105">Aplica uma operação que usa um <xref:microsoft.quantum.arithmetic.phaselittleendian> registro como entrada em um registro de destino do tipo <xref:microsoft.quantum.arithmetic.littleendian> .</span><span class="sxs-lookup"><span data-stu-id="28f91-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>

```qsharp
operation ApplyLEOperationOnPhaseLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="28f91-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="28f91-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="28f91-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian</span><span class="sxs-lookup"><span data-stu-id="28f91-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="28f91-108">A operação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="28f91-108">The operation to be applied.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="28f91-109">destino: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="28f91-109">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="28f91-110">O registro ao qual a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="28f91-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="28f91-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="28f91-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="28f91-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="28f91-112">Remarks</span></span>

<span data-ttu-id="28f91-113">O registro é transformado `LittleEndian` pelo uso de <xref:microsoft.quantum.canon.qftle> e, em seguida, retornado para sua representação original após a aplicação do `op` .</span><span class="sxs-lookup"><span data-stu-id="28f91-113">The register is transformed to `LittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="28f91-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="28f91-114">See Also</span></span>

- [<span data-ttu-id="28f91-115">Microsoft. Quantum. Canon. ApplyLEOperationonPhaseLEA</span><span class="sxs-lookup"><span data-stu-id="28f91-115">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA)
- [<span data-ttu-id="28f91-116">Microsoft. Quantum. Canon. ApplyLEOperationonPhaseLEC</span><span class="sxs-lookup"><span data-stu-id="28f91-116">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)
- [<span data-ttu-id="28f91-117">Microsoft. Quantum. Canon. ApplyLEOperationonPhaseLECA</span><span class="sxs-lookup"><span data-stu-id="28f91-117">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)