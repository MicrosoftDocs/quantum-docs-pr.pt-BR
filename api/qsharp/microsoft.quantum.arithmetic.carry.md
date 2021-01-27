---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Operação de execução
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: dfb08a9a9c805c0b611ab993c9b1eb949810a7da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843346"
---
# <a name="carry-operation"></a><span data-ttu-id="aa4b6-102">Operação de execução</span><span class="sxs-lookup"><span data-stu-id="aa4b6-102">Carry operation</span></span>

<span data-ttu-id="aa4b6-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="aa4b6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="aa4b6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa4b6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa4b6-105">Implementa uma porta de transporte reversível.</span><span class="sxs-lookup"><span data-stu-id="aa4b6-105">Implements a reversible carry gate.</span></span> <span data-ttu-id="aa4b6-106">Dado um bit de transporte codificado em qubit `carryIn` e dois bits de soma codificados no `summand1` e no, o `summand2` computa o XOR bit e o de `carryIn` `summand1` `summand2` qubit `summand2` e a execução é XORed para o qubit `carryOut` .</span><span class="sxs-lookup"><span data-stu-id="aa4b6-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.</span></span>

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="aa4b6-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa4b6-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="aa4b6-108">transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="aa4b6-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="aa4b6-109">Qubit de transporte.</span><span class="sxs-lookup"><span data-stu-id="aa4b6-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="aa4b6-110">summand1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="aa4b6-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="aa4b6-111">Primeiro soma qubit.</span><span class="sxs-lookup"><span data-stu-id="aa4b6-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="aa4b6-112">summand2: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="aa4b6-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="aa4b6-113">Segundo soma qubit, é substituído pelo menor bit da soma de `summand1` e `summand2` .</span><span class="sxs-lookup"><span data-stu-id="aa4b6-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>


### <a name="carryout--qubit"></a><span data-ttu-id="aa4b6-114">postergar: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="aa4b6-114">carryOut : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="aa4b6-115">Qubit de execução, será XORed com o bit mais alto da soma.</span><span class="sxs-lookup"><span data-stu-id="aa4b6-115">Carry-out qubit, will be xored with the higher bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aa4b6-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aa4b6-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

