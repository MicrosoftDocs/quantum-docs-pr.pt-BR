---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Operação de soma
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: b31d8ab39676ee6723e5fc053eba9e0af3ac2b2f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694515"
---
# <a name="sum-operation"></a><span data-ttu-id="acb3b-102">Operação de soma</span><span class="sxs-lookup"><span data-stu-id="acb3b-102">Sum operation</span></span>

<span data-ttu-id="acb3b-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="acb3b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="acb3b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="acb3b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="acb3b-105">Implementa uma porta de soma reversível.</span><span class="sxs-lookup"><span data-stu-id="acb3b-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="acb3b-106">Dado um bit de transporte codificado em qubit `carryIn` e dois bits de soma codificados no `summand1` e `summand2` no, o computa o XOR bit e o de `carryIn` `summand1` `summand2` qubit `summand2` .</span><span class="sxs-lookup"><span data-stu-id="acb3b-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="acb3b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="acb3b-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="acb3b-108">transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="acb3b-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="acb3b-109">Qubit de transporte.</span><span class="sxs-lookup"><span data-stu-id="acb3b-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="acb3b-110">summand1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="acb3b-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="acb3b-111">Primeiro soma qubit.</span><span class="sxs-lookup"><span data-stu-id="acb3b-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="acb3b-112">summand2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="acb3b-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="acb3b-113">Segundo soma qubit, é substituído pelo menor bit da soma de `summand1` e `summand2` .</span><span class="sxs-lookup"><span data-stu-id="acb3b-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="acb3b-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="acb3b-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="acb3b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="acb3b-115">Remarks</span></span>

<span data-ttu-id="acb3b-116">Ao contrário da `Carry` operação, isso não computa o bit de execução.</span><span class="sxs-lookup"><span data-stu-id="acb3b-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>