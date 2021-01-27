---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterCA
title: Operação ApplyToSubregisterCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterCA
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9f24c3ca9b152cf9bbf81e59b86f83a0ab459031
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841218"
---
# <a name="applytosubregisterca-operation"></a><span data-ttu-id="f16f0-102">Operação ApplyToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="f16f0-102">ApplyToSubregisterCA operation</span></span>

<span data-ttu-id="f16f0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f16f0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f16f0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f16f0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f16f0-105">Aplica uma operação a um subregistro de um registro, com qubits especificado por uma matriz de seus índices.</span><span class="sxs-lookup"><span data-stu-id="f16f0-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>
<span data-ttu-id="f16f0-106">O modificador `CA` indica que a operação é controlável e de adjointable.</span><span class="sxs-lookup"><span data-stu-id="f16f0-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToSubregisterCA (op : (Qubit[] => Unit is Ctl + Adj), idxs : Int[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f16f0-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f16f0-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="f16f0-108">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="f16f0-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f16f0-109">Operação a ser aplicada ao subregistro.</span><span class="sxs-lookup"><span data-stu-id="f16f0-109">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="f16f0-110">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f16f0-110">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f16f0-111">Matriz de índices, indicando a qual qubits a operação será aplicada.</span><span class="sxs-lookup"><span data-stu-id="f16f0-111">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f16f0-112">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f16f0-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f16f0-113">Registrar em que a operação atua.</span><span class="sxs-lookup"><span data-stu-id="f16f0-113">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f16f0-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f16f0-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f16f0-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f16f0-115">See Also</span></span>

- [<span data-ttu-id="f16f0-116">Microsoft. Quantum. Canon. ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="f16f0-116">Microsoft.Quantum.Canon.ApplyToSubregister</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregister)