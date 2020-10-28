---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector operação
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 01b6d5aede102e47df86ea70d071d81eba1ade6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693577"
---
# <a name="_assertequalonbasisvector-operation"></a><span data-ttu-id="89380-102">_assertEqualOnBasisVector operação</span><span class="sxs-lookup"><span data-stu-id="89380-102">_assertEqualOnBasisVector operation</span></span>

<span data-ttu-id="89380-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="89380-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="89380-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="89380-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="89380-105">Verifica se o resultado da aplicação de duas operações `givenU` e `expectedU` um estado de base é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="89380-105">Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same.</span></span> <span data-ttu-id="89380-106">O estado base é descrito por `basis` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="89380-106">The basis state is described by `basis` parameter.</span></span>
<span data-ttu-id="89380-107">Consulte <xref:microsoft.quantum.extensions.fliptobasis> a função para obter mais detalhes sobre essa descrição.</span><span class="sxs-lookup"><span data-stu-id="89380-107">See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.</span></span>

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="89380-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="89380-108">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="89380-109">base: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="89380-109">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="89380-110">Estado base especificado por uma ID de estado de base de qubit único (0 <= ID <= 3) para cada um dos $n $ qubits.</span><span class="sxs-lookup"><span data-stu-id="89380-110">Basis state specified by a single-qubit basis state ID (0 <= id <= 3) for each of $n$ qubits.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="89380-111">dada: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="89380-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="89380-112">Operação em $n $ qubits a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="89380-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="89380-113">expected: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="89380-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="89380-114">A operação de referência em $n $ qubits que é comparada é comparada com.</span><span class="sxs-lookup"><span data-stu-id="89380-114">Reference operation on $n$ qubits that givenU is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="89380-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="89380-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

