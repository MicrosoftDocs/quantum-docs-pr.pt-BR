---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Operação PrepareChoiState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: cb34078c09f8c28b5b9bbda1bae6936d13ffcc78
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854395"
---
# <a name="preparechoistate-operation"></a><span data-ttu-id="b3c57-102">Operação PrepareChoiState</span><span class="sxs-lookup"><span data-stu-id="b3c57-102">PrepareChoiState operation</span></span>

<span data-ttu-id="b3c57-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b3c57-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b3c57-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b3c57-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b3c57-105">Prepara o estado Choi – Jamiołkowski para uma determinada operação em determinados registros de referência e destino.</span><span class="sxs-lookup"><span data-stu-id="b3c57-105">Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b3c57-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b3c57-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="b3c57-107">op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="b3c57-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b3c57-108">A operação $ \Lambda $ cujo Choi de estado $J (\Lambda)/2 ^ N $ deve ser preparada, em que $N $ é o número de qubits em que os `op` atos atuam.</span><span class="sxs-lookup"><span data-stu-id="b3c57-108">Operation $\Lambda$ whose Choi–Jamiołkowski state $J(\Lambda) / 2^N$ is to be prepared, where $N$ is the number of qubits on which `op` acts.</span></span>


### <a name="reference--qubit"></a><span data-ttu-id="b3c57-109">referência: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b3c57-109">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b3c57-110">Um registro de qubits a partir do estado $ \ket{00\cdots 0} $ a ser usado como uma referência para a ação de `op` .</span><span class="sxs-lookup"><span data-stu-id="b3c57-110">A register of qubits starting in the $\ket{00\cdots 0}$ state to be used as a reference for the action of `op`.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b3c57-111">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b3c57-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b3c57-112">Um registro de qubits inicialmente no estado $ \ket{00\cdots 0} $ no qual deve `op` ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="b3c57-112">A register of qubits initially in the $\ket{00\cdots 0}$ state on which `op` is to be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b3c57-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b3c57-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b3c57-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3c57-114">Remarks</span></span>

<span data-ttu-id="b3c57-115">O \Lambda (Choi-Jamiłkowski State $J) $ de um processo Quantum é definido como $ $ \begin{align} J (\Lambda) \mathrel{: =} (\boldone \otimes \Lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{Align} $ $, em que $ | X\rangle \! \rangle $ é a *vetorização* de uma matriz $X $ na Convenção de empilhamento de coluna.</span><span class="sxs-lookup"><span data-stu-id="b3c57-115">The Choi–Jamiłkowski state $J(\Lambda)$ of a quantum process is defined as $$ \begin{align} J(\Lambda) \mathrel{:=} (\boldone \otimes \Lambda) (|\boldone\rangle\!\rangle\langle\!\langle\boldone|), \end{align} $$ where $|X\rangle\!\rangle$ is the *vectorization* of a matrix $X$ in the column-stacking convention.</span></span> <span data-ttu-id="b3c57-116">Aprender uma descrição clássica desse Estado fornece informações completas sobre o efeito de $ \Lambda $ agindo em Estados de entrada arbitrários e forma a base do *processo Quantum tomography*.</span><span class="sxs-lookup"><span data-stu-id="b3c57-116">Learning a classical description of this state provides full information about the effect of $\Lambda$ acting on arbitrary input states, and forms the foundation of *quantum process tomography*.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3c57-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b3c57-117">See Also</span></span>

- [<span data-ttu-id="b3c57-118">Microsoft. Quantum. Preparation. PrepareChoiStateA</span><span class="sxs-lookup"><span data-stu-id="b3c57-118">Microsoft.Quantum.Preparation.PrepareChoiStateA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [<span data-ttu-id="b3c57-119">Microsoft. Quantum. Preparation. PrepareChoiStateC</span><span class="sxs-lookup"><span data-stu-id="b3c57-119">Microsoft.Quantum.Preparation.PrepareChoiStateC</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [<span data-ttu-id="b3c57-120">Microsoft. Quantum. Preparation. PrepareChoiStateCA</span><span class="sxs-lookup"><span data-stu-id="b3c57-120">Microsoft.Quantum.Preparation.PrepareChoiStateCA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)