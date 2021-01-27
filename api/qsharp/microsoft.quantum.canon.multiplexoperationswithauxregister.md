---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: Operação MultiplexOperationsWithAuxRegister
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: 91db22d6261709c1c3506c80ff600c904748575a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852472"
---
# <a name="multiplexoperationswithauxregister-operation"></a><span data-ttu-id="467f7-102">Operação MultiplexOperationsWithAuxRegister</span><span class="sxs-lookup"><span data-stu-id="467f7-102">MultiplexOperationsWithAuxRegister operation</span></span>

<span data-ttu-id="467f7-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="467f7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="467f7-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="467f7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="467f7-105">Etapa de implementação de MultiplexOperations.</span><span class="sxs-lookup"><span data-stu-id="467f7-105">Implementation step of MultiplexOperations.</span></span>

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="467f7-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="467f7-106">Input</span></span>

### <a name="unitaries--t--unit--is-adj--ctl"></a><span data-ttu-id="467f7-107">unidades: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL []</span><span class="sxs-lookup"><span data-stu-id="467f7-107">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>




### <a name="auxillaryregister--qubit"></a><span data-ttu-id="467f7-108">auxillaryRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="467f7-108">auxillaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="index--littleendian"></a><span data-ttu-id="467f7-109">índice: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="467f7-109">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="target--t"></a><span data-ttu-id="467f7-110">destino: ' t</span><span class="sxs-lookup"><span data-stu-id="467f7-110">target : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="467f7-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="467f7-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="467f7-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="467f7-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="467f7-113">T'</span><span class="sxs-lookup"><span data-stu-id="467f7-113">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="467f7-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="467f7-114">See Also</span></span>

- [<span data-ttu-id="467f7-115">Microsoft. Quantum. Canon. MultiplexOperations</span><span class="sxs-lookup"><span data-stu-id="467f7-115">Microsoft.Quantum.Canon.MultiplexOperations</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperations)