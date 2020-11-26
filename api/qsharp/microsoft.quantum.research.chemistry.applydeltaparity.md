---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Operação ApplyDeltaParity
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: 40157b6a166b09c6fee63d86e203f92069d008f1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225747"
---
# <a name="applydeltaparity-operation"></a><span data-ttu-id="ff15f-102">Operação ApplyDeltaParity</span><span class="sxs-lookup"><span data-stu-id="ff15f-102">ApplyDeltaParity operation</span></span>

<span data-ttu-id="ff15f-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ff15f-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="ff15f-104">Pacote: [Microsoft. Quantum. Research. química](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ff15f-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="ff15f-105">Calcula a diferença na paridade entre um PQRS anterior... termos e o próximo PQRS... prazo.</span><span class="sxs-lookup"><span data-stu-id="ff15f-105">Computes difference in parity between a previous PQRS... terms and the next PQRS... term.</span></span> <span data-ttu-id="ff15f-106">Essa diferença é calculada em um qubit auxiliar.</span><span class="sxs-lookup"><span data-stu-id="ff15f-106">This difference is computed on a auxiliary qubit.</span></span>

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ff15f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff15f-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="ff15f-108">prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ff15f-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ff15f-109">Lista de índices para PQRS anteriores... termos.</span><span class="sxs-lookup"><span data-stu-id="ff15f-109">List of indices to previous PQRS... terms.</span></span>


### <a name="nextfermionicterm--int"></a><span data-ttu-id="ff15f-110">nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ff15f-110">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ff15f-111">Lista de índices para o próximo PQRS... termos.</span><span class="sxs-lookup"><span data-stu-id="ff15f-111">List of indices to next PQRS... terms.</span></span>


### <a name="aux--qubit"></a><span data-ttu-id="ff15f-112">AUX: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ff15f-112">aux : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ff15f-113">Qubit auxiliar no qual os resultados de computação de paridade são armazenados.</span><span class="sxs-lookup"><span data-stu-id="ff15f-113">Auxiliary qubit onto which parity computation results are stored.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="ff15f-114">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ff15f-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ff15f-115">Qubit atuou por todos os PQRS... termos.</span><span class="sxs-lookup"><span data-stu-id="ff15f-115">Qubit acted on by all PQRS... terms.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ff15f-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ff15f-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ff15f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff15f-117">Remarks</span></span>

<span data-ttu-id="ff15f-118">Isso pressupõe que os índices de P < Q < R < S <... para prevPQ e nextPQ.</span><span class="sxs-lookup"><span data-stu-id="ff15f-118">This assumes that indices of P < Q < R < S < ... for both prevPQ and nextPQ.</span></span>