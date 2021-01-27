---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterA
title: Operação ApplyToSubregisterA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 7a5ae78edcda363f21cadaaed5cb273d35cb60cc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841223"
---
# <a name="applytosubregistera-operation"></a><span data-ttu-id="ec0ba-102">Operação ApplyToSubregisterA</span><span class="sxs-lookup"><span data-stu-id="ec0ba-102">ApplyToSubregisterA operation</span></span>

<span data-ttu-id="ec0ba-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ec0ba-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ec0ba-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ec0ba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ec0ba-105">Aplica uma operação a um subregistro de um registro, com qubits especificado por uma matriz de seus índices.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="ec0ba-106">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToSubregisterA (op : (Qubit[] => Unit is Adj), idxs : Int[], target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="ec0ba-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec0ba-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="ec0ba-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="ec0ba-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ec0ba-109">Operação a ser aplicada ao subregistro.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="ec0ba-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ec0ba-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ec0ba-111">Matriz de índices, indicando a qual qubits a operação será aplicada.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="ec0ba-112">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ec0ba-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ec0ba-113">Registrar em que a operação atua.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ec0ba-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec0ba-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ec0ba-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ec0ba-115">See Also</span></span>

- [<span data-ttu-id="ec0ba-116">Microsoft. Quantum. Canon. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="ec0ba-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)