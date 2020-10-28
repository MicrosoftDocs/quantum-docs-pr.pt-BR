---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Operação IncrementByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 271033b32b0de6cf600dca82126dab19c2bb4f5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694781"
---
# <a name="incrementbymodularinteger-operation"></a><span data-ttu-id="89230-102">Operação IncrementByModularInteger</span><span class="sxs-lookup"><span data-stu-id="89230-102">IncrementByModularInteger operation</span></span>

<span data-ttu-id="89230-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="89230-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="89230-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="89230-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="89230-105">Executa um incremento modular de um registro qubit por uma constante de inteiro.</span><span class="sxs-lookup"><span data-stu-id="89230-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="89230-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="89230-106">Description</span></span>

<span data-ttu-id="89230-107">Vamos indicar `increment` por $a $, `modulus` por $N $ e inteiro codificado `target` por $y $.</span><span class="sxs-lookup"><span data-stu-id="89230-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="89230-108">Em seguida, a operação executa a seguinte transformação: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} inteiros são codificados no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="89230-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format.</span></span>

## <a name="input"></a><span data-ttu-id="89230-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="89230-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="89230-110">incremento: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="89230-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="89230-111">Incremento inteiro $a $ a ser adicionado a $y $.</span><span class="sxs-lookup"><span data-stu-id="89230-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="89230-112">módulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="89230-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="89230-113">Integer $N $ que mods $y + a $.</span><span class="sxs-lookup"><span data-stu-id="89230-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="89230-114">destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="89230-114">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="89230-115">Inteiro $y $ no `LittleEndian` formato `increment` ao qual $a $ é adicionado.</span><span class="sxs-lookup"><span data-stu-id="89230-115">Integer $y$ in `LittleEndian` format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="89230-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="89230-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="89230-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="89230-117">Remarks</span></span>

<span data-ttu-id="89230-118">Pressupõe que o valor inicial de destino seja menor que $N $ e que o incremento $a $ seja menor que $N $.</span><span class="sxs-lookup"><span data-stu-id="89230-118">Assumes that the initial value of target is less than $N$ and that the increment $a$ is less than $N$.</span></span>
<span data-ttu-id="89230-119">Observe que <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> o implementa a mesma operação na `PhaseLittleEndian` base.</span><span class="sxs-lookup"><span data-stu-id="89230-119">Note that <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> implements the same operation in the `PhaseLittleEndian` basis.</span></span>

## <a name="see-also"></a><span data-ttu-id="89230-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="89230-120">See Also</span></span>

- [<span data-ttu-id="89230-121">Microsoft. Quantum. aritmético. IncrementPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="89230-121">Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)