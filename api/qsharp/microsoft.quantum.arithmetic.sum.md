---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Operação de soma
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: 7758e29c9f08f4d05253defbe5a43a5316289522
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221786"
---
# <a name="sum-operation"></a><span data-ttu-id="15837-102">Operação de soma</span><span class="sxs-lookup"><span data-stu-id="15837-102">Sum operation</span></span>

<span data-ttu-id="15837-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="15837-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="15837-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="15837-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="15837-105">Implementa uma porta de soma reversível.</span><span class="sxs-lookup"><span data-stu-id="15837-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="15837-106">Dado um bit de transporte codificado em qubit `carryIn` e dois bits de soma codificados no `summand1` e `summand2` no, o computa o XOR bit e o de `carryIn` `summand1` `summand2` qubit `summand2` .</span><span class="sxs-lookup"><span data-stu-id="15837-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="15837-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="15837-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="15837-108">transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="15837-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="15837-109">Qubit de transporte.</span><span class="sxs-lookup"><span data-stu-id="15837-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="15837-110">summand1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="15837-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="15837-111">Primeiro soma qubit.</span><span class="sxs-lookup"><span data-stu-id="15837-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="15837-112">summand2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="15837-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="15837-113">Segundo soma qubit, é substituído pelo menor bit da soma de `summand1` e `summand2` .</span><span class="sxs-lookup"><span data-stu-id="15837-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="15837-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="15837-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="15837-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="15837-115">Remarks</span></span>

<span data-ttu-id="15837-116">Ao contrário da `Carry` operação, isso não computa o bit de execução.</span><span class="sxs-lookup"><span data-stu-id="15837-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>