---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Operação ApplyDeltaParity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: f5f1d74274994f042f1bc3f2e0d5332f504be02c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851105"
---
# <a name="applydeltaparity-operation"></a><span data-ttu-id="130de-102">Operação ApplyDeltaParity</span><span class="sxs-lookup"><span data-stu-id="130de-102">ApplyDeltaParity operation</span></span>

<span data-ttu-id="130de-103">Namespace: [Microsoft. Quantum. Research. química](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="130de-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="130de-104">Pacote: [Microsoft. Quantum. Research. química](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="130de-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="130de-105">Calcula a diferença na paridade entre um PQRS anterior... termos e o próximo PQRS... prazo.</span><span class="sxs-lookup"><span data-stu-id="130de-105">Computes difference in parity between a previous PQRS... terms and the next PQRS... term.</span></span> <span data-ttu-id="130de-106">Essa diferença é calculada em um qubit auxiliar.</span><span class="sxs-lookup"><span data-stu-id="130de-106">This difference is computed on a auxiliary qubit.</span></span>

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="130de-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="130de-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="130de-108">prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="130de-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="130de-109">Lista de índices para PQRS anteriores... termos.</span><span class="sxs-lookup"><span data-stu-id="130de-109">List of indices to previous PQRS... terms.</span></span>


### <a name="nextfermionicterm--int"></a><span data-ttu-id="130de-110">nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="130de-110">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="130de-111">Lista de índices para o próximo PQRS... termos.</span><span class="sxs-lookup"><span data-stu-id="130de-111">List of indices to next PQRS... terms.</span></span>


### <a name="aux--qubit"></a><span data-ttu-id="130de-112">AUX: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="130de-112">aux : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="130de-113">Qubit auxiliar no qual os resultados de computação de paridade são armazenados.</span><span class="sxs-lookup"><span data-stu-id="130de-113">Auxiliary qubit onto which parity computation results are stored.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="130de-114">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="130de-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="130de-115">Qubit atuou por todos os PQRS... termos.</span><span class="sxs-lookup"><span data-stu-id="130de-115">Qubit acted on by all PQRS... terms.</span></span>



## <a name="output--unit"></a><span data-ttu-id="130de-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="130de-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="130de-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="130de-117">Remarks</span></span>

<span data-ttu-id="130de-118">Isso pressupõe que os índices de P < Q < R < S <... para prevPQ e nextPQ.</span><span class="sxs-lookup"><span data-stu-id="130de-118">This assumes that indices of P < Q < R < S < ... for both prevPQ and nextPQ.</span></span>