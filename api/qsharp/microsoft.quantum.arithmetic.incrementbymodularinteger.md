---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Operação IncrementByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: f5bacef299ab0b3627e757abdcaa798cf9b2e7b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846594"
---
# <a name="incrementbymodularinteger-operation"></a><span data-ttu-id="2b02b-102">Operação IncrementByModularInteger</span><span class="sxs-lookup"><span data-stu-id="2b02b-102">IncrementByModularInteger operation</span></span>

<span data-ttu-id="2b02b-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2b02b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2b02b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b02b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b02b-105">Executa um incremento modular de um registro qubit por uma constante de inteiro.</span><span class="sxs-lookup"><span data-stu-id="2b02b-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="2b02b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b02b-106">Description</span></span>

<span data-ttu-id="2b02b-107">Vamos indicar `increment` por $a $, `modulus` por $N $ e inteiro codificado `target` por $y $.</span><span class="sxs-lookup"><span data-stu-id="2b02b-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="2b02b-108">Em seguida, a operação executa a seguinte transformação: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} inteiros são codificados no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="2b02b-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format.</span></span>

## <a name="input"></a><span data-ttu-id="2b02b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b02b-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="2b02b-110">incremento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2b02b-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2b02b-111">Incremento inteiro $a $ a ser adicionado a $y $.</span><span class="sxs-lookup"><span data-stu-id="2b02b-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="2b02b-112">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2b02b-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2b02b-113">Integer $N $ que mods $y + a $.</span><span class="sxs-lookup"><span data-stu-id="2b02b-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="2b02b-114">destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2b02b-114">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2b02b-115">Inteiro $y $ no `LittleEndian` formato `increment` ao qual $a $ é adicionado.</span><span class="sxs-lookup"><span data-stu-id="2b02b-115">Integer $y$ in `LittleEndian` format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2b02b-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2b02b-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2b02b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b02b-117">Remarks</span></span>

<span data-ttu-id="2b02b-118">Pressupõe que o valor inicial de destino seja menor que $N $ e que o incremento $a $ seja menor que $N $.</span><span class="sxs-lookup"><span data-stu-id="2b02b-118">Assumes that the initial value of target is less than $N$ and that the increment $a$ is less than $N$.</span></span>
<span data-ttu-id="2b02b-119">Observe que <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> o implementa a mesma operação na `PhaseLittleEndian` base.</span><span class="sxs-lookup"><span data-stu-id="2b02b-119">Note that <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> implements the same operation in the `PhaseLittleEndian` basis.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b02b-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2b02b-120">See Also</span></span>

- [<span data-ttu-id="2b02b-121">Microsoft. Quantum. aritmético. IncrementPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="2b02b-121">Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)