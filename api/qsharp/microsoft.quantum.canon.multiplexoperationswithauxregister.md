---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Operação MultiplexOperationsWithAuxRegister
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: f6a90657324f8528aaa2e9e511a7f8cbcd2f540f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693954"
---
# <a name="multiplexoperationswithauxregister-operation"></a><span data-ttu-id="4b5c3-102">Operação MultiplexOperationsWithAuxRegister</span><span class="sxs-lookup"><span data-stu-id="4b5c3-102">MultiplexOperationsWithAuxRegister operation</span></span>

<span data-ttu-id="4b5c3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4b5c3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4b5c3-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4b5c3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4b5c3-105">Etapa de implementação de MultiplexOperations.</span><span class="sxs-lookup"><span data-stu-id="4b5c3-105">Implementation step of MultiplexOperations.</span></span>

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="4b5c3-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b5c3-106">Input</span></span>

### <a name="unitaries--t--unit-adj--ctl"></a><span data-ttu-id="4b5c3-107">unidades: não => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL []</span><span class="sxs-lookup"><span data-stu-id="4b5c3-107">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>




### <a name="auxillaryregister--qubit"></a><span data-ttu-id="4b5c3-108">auxillaryRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4b5c3-108">auxillaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="index--littleendian"></a><span data-ttu-id="4b5c3-109">índice: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4b5c3-109">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="target--t"></a><span data-ttu-id="4b5c3-110">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="4b5c3-110">target : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="4b5c3-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4b5c3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4b5c3-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4b5c3-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4b5c3-113">T'</span><span class="sxs-lookup"><span data-stu-id="4b5c3-113">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="4b5c3-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4b5c3-114">See Also</span></span>

- [<span data-ttu-id="4b5c3-115">Microsoft. Quantum. Canon. MultiplexOperations</span><span class="sxs-lookup"><span data-stu-id="4b5c3-115">Microsoft.Quantum.Canon.MultiplexOperations</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperations)