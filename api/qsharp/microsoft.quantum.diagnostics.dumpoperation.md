---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Operação DumpOperation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: 444d42e2440b30b3bdf50d55a399568bed063222
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693535"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="6781c-102">Operação DumpOperation</span><span class="sxs-lookup"><span data-stu-id="6781c-102">DumpOperation operation</span></span>

<span data-ttu-id="6781c-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="6781c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="6781c-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6781c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6781c-105">Dada uma operação, exibe o diagnóstico sobre a operação disponibilizada pelo destino de execução atual.</span><span class="sxs-lookup"><span data-stu-id="6781c-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="6781c-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6781c-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="6781c-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6781c-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6781c-108">O número de qubits em que a operação fornecida funciona.</span><span class="sxs-lookup"><span data-stu-id="6781c-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit-adj"></a><span data-ttu-id="6781c-109">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6781c-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="6781c-110">A operação a ser diagnosticada.</span><span class="sxs-lookup"><span data-stu-id="6781c-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6781c-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6781c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6781c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6781c-112">Remarks</span></span>

<span data-ttu-id="6781c-113">Chamar esta operação não tem nenhum efeito observável de em Q #.</span><span class="sxs-lookup"><span data-stu-id="6781c-113">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="6781c-114">Os diagnósticos exatos que são exibidos, se houver, dependem do ambiente de destino e do editor de execução atual.</span><span class="sxs-lookup"><span data-stu-id="6781c-114">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="6781c-115">Por exemplo, quando usado no simulador de Quantum de estado completo, é exibida uma matriz unitário usada para representar `op` .</span><span class="sxs-lookup"><span data-stu-id="6781c-115">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="6781c-116">Observe que, quando executado em simuladores que admitem uma ambiguidade de fase global (por exemplo: o simulador de estado completo), representações retornadas podem variar até uma fase global.</span><span class="sxs-lookup"><span data-stu-id="6781c-116">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="6781c-117">Da mesma forma, a ordenação de representações de matriz de linhas e colunas pode variar com as convenções usadas por cada simulador que dá suporte a essa operação.</span><span class="sxs-lookup"><span data-stu-id="6781c-117">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>