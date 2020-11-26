---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Operação DumpOperation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: b0e07173ddbeb8a96d4a85928258b6e30deb394d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202049"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="d7cbb-102">Operação DumpOperation</span><span class="sxs-lookup"><span data-stu-id="d7cbb-102">DumpOperation operation</span></span>

<span data-ttu-id="d7cbb-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d7cbb-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d7cbb-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d7cbb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d7cbb-105">Dada uma operação, exibe o diagnóstico sobre a operação disponibilizada pelo destino de execução atual.</span><span class="sxs-lookup"><span data-stu-id="d7cbb-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="d7cbb-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7cbb-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="d7cbb-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d7cbb-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d7cbb-108">O número de qubits em que a operação fornecida funciona.</span><span class="sxs-lookup"><span data-stu-id="d7cbb-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="d7cbb-109">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="d7cbb-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d7cbb-110">A operação a ser diagnosticada.</span><span class="sxs-lookup"><span data-stu-id="d7cbb-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d7cbb-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d7cbb-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d7cbb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7cbb-112">Remarks</span></span>

<span data-ttu-id="d7cbb-113">Chamar esta operação não tem nenhum efeito observável de em Q #.</span><span class="sxs-lookup"><span data-stu-id="d7cbb-113">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="d7cbb-114">Os diagnósticos exatos que são exibidos, se houver, dependem do ambiente de destino e do editor de execução atual.</span><span class="sxs-lookup"><span data-stu-id="d7cbb-114">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="d7cbb-115">Por exemplo, quando usado no simulador de Quantum de estado completo, é exibida uma matriz unitário usada para representar `op` .</span><span class="sxs-lookup"><span data-stu-id="d7cbb-115">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="d7cbb-116">Observe que, quando executado em simuladores que admitem uma ambiguidade de fase global (por exemplo: o simulador de estado completo), representações retornadas podem variar até uma fase global.</span><span class="sxs-lookup"><span data-stu-id="d7cbb-116">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="d7cbb-117">Da mesma forma, a ordenação de representações de matriz de linhas e colunas pode variar com as convenções usadas por cada simulador que dá suporte a essa operação.</span><span class="sxs-lookup"><span data-stu-id="d7cbb-117">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>