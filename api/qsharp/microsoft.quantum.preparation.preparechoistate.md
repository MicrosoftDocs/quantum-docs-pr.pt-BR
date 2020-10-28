---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Operação PrepareChoiState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiłkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: 8b2917a7d9414539f2f7c821c4115fc4b21d0373
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696880"
---
# <a name="preparechoistate-operation"></a><span data-ttu-id="59c31-102">Operação PrepareChoiState</span><span class="sxs-lookup"><span data-stu-id="59c31-102">PrepareChoiState operation</span></span>

<span data-ttu-id="59c31-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="59c31-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="59c31-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="59c31-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="59c31-105">Prepara o estado Choi – Jamiłkowski para uma determinada operação em determinados registros de referência e destino.</span><span class="sxs-lookup"><span data-stu-id="59c31-105">Prepares the Choi–Jamiłkowski state for a given operation onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="59c31-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="59c31-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="59c31-107">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="59c31-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="59c31-108">A operação $ \Lambda $ cujo Choi de estado $J (\Lambda)/2 ^ N $ deve ser preparada, em que $N $ é o número de qubits em que os `op` atos atuam.</span><span class="sxs-lookup"><span data-stu-id="59c31-108">Operation $\Lambda$ whose Choi–Jamiłkowski state $J(\Lambda) / 2^N$ is to be prepared, where $N$ is the number of qubits on which `op` acts.</span></span>


### <a name="reference--qubit"></a><span data-ttu-id="59c31-109">referência: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="59c31-109">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="59c31-110">Um registro de qubits a partir do estado $ \ket{00\cdots 0} $ a ser usado como uma referência para a ação de `op` .</span><span class="sxs-lookup"><span data-stu-id="59c31-110">A register of qubits starting in the $\ket{00\cdots 0}$ state to be used as a reference for the action of `op`.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="59c31-111">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="59c31-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="59c31-112">Um registro de qubits inicialmente no estado $ \ket{00\cdots 0} $ no qual deve `op` ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="59c31-112">A register of qubits initially in the $\ket{00\cdots 0}$ state on which `op` is to be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="59c31-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="59c31-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="59c31-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="59c31-114">Remarks</span></span>

<span data-ttu-id="59c31-115">O \Lambda (Choi-Jamiłkowski State $J) $ de um processo Quantum é definido como $ $ \begin{align} J (\Lambda) \mathrel{: =} (\boldone \otimes \Lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{Align} $ $, em que $ | X\rangle \! \rangle $ é a *vetorização* de uma matriz $X $ na Convenção de empilhamento de coluna.</span><span class="sxs-lookup"><span data-stu-id="59c31-115">The Choi–Jamiłkowski state $J(\Lambda)$ of a quantum process is defined as $$ \begin{align} J(\Lambda) \mathrel{:=} (\boldone \otimes \Lambda) (|\boldone\rangle\!\rangle\langle\!\langle\boldone|), \end{align} $$ where $|X\rangle\!\rangle$ is the *vectorization* of a matrix $X$ in the column-stacking convention.</span></span> <span data-ttu-id="59c31-116">Aprender uma descrição clássica desse Estado fornece informações completas sobre o efeito de $ \Lambda $ agindo em Estados de entrada arbitrários e forma a base do *processo Quantum tomography* .</span><span class="sxs-lookup"><span data-stu-id="59c31-116">Learning a classical description of this state provides full information about the effect of $\Lambda$ acting on arbitrary input states, and forms the foundation of *quantum process tomography* .</span></span>

## <a name="see-also"></a><span data-ttu-id="59c31-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="59c31-117">See Also</span></span>

- [<span data-ttu-id="59c31-118">Microsoft. Quantum. Preparation. PrepareChoiStateA</span><span class="sxs-lookup"><span data-stu-id="59c31-118">Microsoft.Quantum.Preparation.PrepareChoiStateA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [<span data-ttu-id="59c31-119">Microsoft. Quantum. Preparation. PrepareChoiStateC</span><span class="sxs-lookup"><span data-stu-id="59c31-119">Microsoft.Quantum.Preparation.PrepareChoiStateC</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [<span data-ttu-id="59c31-120">Microsoft. Quantum. Preparation. PrepareChoiStateCA</span><span class="sxs-lookup"><span data-stu-id="59c31-120">Microsoft.Quantum.Preparation.PrepareChoiStateCA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)