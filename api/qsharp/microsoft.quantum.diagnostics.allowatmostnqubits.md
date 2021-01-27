---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Operação AllowAtMostNQubits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 3aa80767ac0f752e7be0efa2966c580ca3cb8f19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830906"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="1c4c2-102">Operação AllowAtMostNQubits</span><span class="sxs-lookup"><span data-stu-id="1c4c2-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="1c4c2-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="1c4c2-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="1c4c2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1c4c2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1c4c2-105">Entre uma chamada para essa operação e seu adjacente, o declara que, no máximo, um determinado número de qubits adicionais são alocados com instruções using.</span><span class="sxs-lookup"><span data-stu-id="1c4c2-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="1c4c2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1c4c2-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="1c4c2-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1c4c2-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1c4c2-108">O número máximo de qubits que podem ser alocadas.</span><span class="sxs-lookup"><span data-stu-id="1c4c2-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="1c4c2-109">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="1c4c2-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="1c4c2-110">Uma mensagem a ser exibida após a falha.</span><span class="sxs-lookup"><span data-stu-id="1c4c2-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1c4c2-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1c4c2-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="1c4c2-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1c4c2-112">Example</span></span>

<span data-ttu-id="1c4c2-113">O trecho a seguir falhará quando executado em computadores que dão suporte a este diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="1c4c2-113">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
within {
    AllowAtMostNQubits(3, "Too many qubits allocated.");
} apply {
    // Fails since this allocates four qubits.
    using (register = Qubit[4]) {
    }
}
```

## <a name="remarks"></a><span data-ttu-id="1c4c2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c4c2-114">Remarks</span></span>

<span data-ttu-id="1c4c2-115">Esta operação pode ser substituída por um não op em destinos que não dão suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="1c4c2-115">This operation may be replaced by a no-op on targets which do not support it.</span></span>