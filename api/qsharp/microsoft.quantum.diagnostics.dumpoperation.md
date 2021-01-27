---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Operação DumpOperation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: cde188806506c586c4c77a7f9b2b43ad0e10ef1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829270"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="1f1c2-102">Operação DumpOperation</span><span class="sxs-lookup"><span data-stu-id="1f1c2-102">DumpOperation operation</span></span>

<span data-ttu-id="1f1c2-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="1f1c2-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="1f1c2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1f1c2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1f1c2-105">Dada uma operação, exibe o diagnóstico sobre a operação disponibilizada pelo destino de execução atual.</span><span class="sxs-lookup"><span data-stu-id="1f1c2-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="1f1c2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f1c2-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="1f1c2-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1f1c2-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1f1c2-108">O número de qubits em que a operação fornecida funciona.</span><span class="sxs-lookup"><span data-stu-id="1f1c2-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="1f1c2-109">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="1f1c2-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="1f1c2-110">A operação a ser diagnosticada.</span><span class="sxs-lookup"><span data-stu-id="1f1c2-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1f1c2-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1f1c2-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="1f1c2-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1f1c2-112">Example</span></span>

<span data-ttu-id="1f1c2-113">Quando executado no destino do simulador do Quantum, o trecho a seguir produzirá a matriz $ $ \begin{aligned} \left (\begin{Matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \end{Matrix}\right) \end{aligned}.</span><span class="sxs-lookup"><span data-stu-id="1f1c2-113">When run on the quantum simulator target, the following snippet will output the matrix $$ \begin{aligned} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \end{matrix}\right) \end{aligned}.</span></span>
$$

```qsharp
operation DumpCnot() : Unit {
    DumpOperation(2, ApplyToFirstTwoQubitsCA(CNOT, _));
}
```

## <a name="remarks"></a><span data-ttu-id="1f1c2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f1c2-114">Remarks</span></span>

<span data-ttu-id="1f1c2-115">Chamar esta operação não tem nenhum efeito observável de em Q #.</span><span class="sxs-lookup"><span data-stu-id="1f1c2-115">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="1f1c2-116">Os diagnósticos exatos que são exibidos, se houver, dependem do ambiente de destino e do editor de execução atual.</span><span class="sxs-lookup"><span data-stu-id="1f1c2-116">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="1f1c2-117">Por exemplo, quando usado no simulador de Quantum de estado completo, é exibida uma matriz unitário usada para representar `op` .</span><span class="sxs-lookup"><span data-stu-id="1f1c2-117">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="1f1c2-118">Observe que, quando executado em simuladores que admitem uma ambiguidade de fase global (por exemplo: o simulador de estado completo), representações retornadas podem variar até uma fase global.</span><span class="sxs-lookup"><span data-stu-id="1f1c2-118">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="1f1c2-119">Da mesma forma, a ordenação de representações de matriz de linhas e colunas pode variar com as convenções usadas por cada simulador que dá suporte a essa operação.</span><span class="sxs-lookup"><span data-stu-id="1f1c2-119">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>