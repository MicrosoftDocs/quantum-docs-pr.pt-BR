---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Operação KnillDistill
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 1135db83cf750918347df10c6f1301b636aaee0c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693452"
---
# <a name="knilldistill-operation"></a><span data-ttu-id="33e35-102">Operação KnillDistill</span><span class="sxs-lookup"><span data-stu-id="33e35-102">KnillDistill operation</span></span>

<span data-ttu-id="33e35-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="33e35-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="33e35-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="33e35-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="33e35-105">Implementa o algoritmo detalhamento de estado mágico Knill.</span><span class="sxs-lookup"><span data-stu-id="33e35-105">Implements the Knill magic state distillation algorithm.</span></span>

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a><span data-ttu-id="33e35-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="33e35-106">Description</span></span>

<span data-ttu-id="33e35-107">Dadas 15 cópias aproximadas de um estado mágico $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} {8} \ket {1} \end{Align}, $ $ produz uma cópia de qualidade superior.</span><span class="sxs-lookup"><span data-stu-id="33e35-107">Given 15 approximate copies of a magic state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1} \end{align}, $$ yields one higher-quality copy.</span></span>

## <a name="input"></a><span data-ttu-id="33e35-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="33e35-108">Input</span></span>

### <a name="roughmagic--qubit"></a><span data-ttu-id="33e35-109">roughMagic: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="33e35-109">roughMagic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="33e35-110">Um registro de quinze qubits que contém cópias aproximadas de um estado mágico.</span><span class="sxs-lookup"><span data-stu-id="33e35-110">A register of fifteen qubits containing approximate copies of a magic state.</span></span> <span data-ttu-id="33e35-111">O aplicativo a seguir deste procedimento detalhamento conterá `roughMagic[0]` uma cópia de qualidade superior e o restante do registro será redefinido para o estado $ \ket{00\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="33e35-111">Following application of this distillation procedure, `roughMagic[0]` will contain one higher-quality copy, and the rest of the register will be reset to the $\ket{00\cdots 0}$ state.</span></span>



## <a name="output--bool"></a><span data-ttu-id="33e35-112">Saída: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="33e35-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="33e35-113">Se `true` , o procedimento foi bem-sucedido e a cópia de qualidade superior deve ser aceita.</span><span class="sxs-lookup"><span data-stu-id="33e35-113">If `true`, then the procedure succeeded and the higher-quality copy should be accepted.</span></span> <span data-ttu-id="33e35-114">Se `false` , o procedimento falhou e o estado do registro deve ser considerado indefinido.</span><span class="sxs-lookup"><span data-stu-id="33e35-114">If `false`, the procedure failed, and the state of the register should be considered undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e35-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="33e35-115">Remarks</span></span>

<span data-ttu-id="33e35-116">Seguimos o algoritmo de Knill.</span><span class="sxs-lookup"><span data-stu-id="33e35-116">We follow the algorithm of Knill.</span></span>
<span data-ttu-id="33e35-117">No entanto, a implementação atual está longe de ser a ideal, pois ela usa muitas qubits.</span><span class="sxs-lookup"><span data-stu-id="33e35-117">However, the present implementation is far from being optimal, as it uses too many qubits.</span></span>
<span data-ttu-id="33e35-118">Os Estados mágicos são injetados nessa rotina; nesse caso, há protocolos melhores.</span><span class="sxs-lookup"><span data-stu-id="33e35-118">The magic states are injected in this routine, in which case there are better protocols.</span></span>

## <a name="references"></a><span data-ttu-id="33e35-119">Referências</span><span class="sxs-lookup"><span data-stu-id="33e35-119">References</span></span>

- [<span data-ttu-id="33e35-120">Knill</span><span class="sxs-lookup"><span data-stu-id="33e35-120">Knill</span></span>](https://arxiv.org/abs/quant-ph/0402171)