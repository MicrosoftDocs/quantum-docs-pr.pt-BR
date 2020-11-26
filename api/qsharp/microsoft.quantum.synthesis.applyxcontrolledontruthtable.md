---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: Operação ApplyXControlledOnTruthTable
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: aa4e1bc0d5058228721728a894b896331ec626d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203290"
---
# <a name="applyxcontrolledontruthtable-operation"></a><span data-ttu-id="6d0b8-102">Operação ApplyXControlledOnTruthTable</span><span class="sxs-lookup"><span data-stu-id="6d0b8-102">ApplyXControlledOnTruthTable operation</span></span>

<span data-ttu-id="6d0b8-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6d0b8-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6d0b8-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6d0b8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6d0b8-105">Aplica a @"microsoft.quantum.intrinsic.x" operação em `target` , se a função booliana `func` for avaliada como true para a atribuição clássica no `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="6d0b8-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="6d0b8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d0b8-106">Description</span></span>

<span data-ttu-id="6d0b8-107">A operação implementa a operação unitário \begin{align} U\ket {x} \ ket {y} = \ket{x}\ket{y \oplus f (x)} \end{align} em que $x $ e $y $ representam `controlRegister` e `target` , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-107">The operation implements the unitary operation \begin{align} U\ket{x}\ket{y} = \ket{x}\ket{y \oplus f(x)} \end{align} where $x$ and $y$ represent `controlRegister` and `target`, respectively.</span></span>

<span data-ttu-id="6d0b8-108">A função booliana $f $ é representada como uma tabela verdadeira em termos de um grande inteiro.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-108">The Boolean function $f$ is represented as a truth table in terms of a big integer.</span></span>
<span data-ttu-id="6d0b8-109">Por exemplo, a função principal em três entradas é representada pelo bitstring `11101000` , onde o bit mais significativo `1` corresponde à atribuição de entrada `(1, 1, 1)` e o bit menos significativo `0` corresponde à atribuição de entrada `(0, 0, 0)` .</span><span class="sxs-lookup"><span data-stu-id="6d0b8-109">For example, the majority function on three inputs is represented by the bitstring `11101000`, where the most significant bit `1` corresponds to the input assignment `(1, 1, 1)`, and the least significant bit `0` corresponds to the input assignment `(0, 0, 0)`.</span></span>
<span data-ttu-id="6d0b8-110">Ele pode ser representado pelo grande inteiro `0xE8L` em notação hexadecimal ou como `232L` em notação decimal.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-110">It can be represented by the big integer `0xE8L` in hexadecimal notation or as `232L` in decimal notation.</span></span>  <span data-ttu-id="6d0b8-111">O `L` sufixo indica que a constante é do tipo `BigInt` .</span><span class="sxs-lookup"><span data-stu-id="6d0b8-111">The `L` suffix indicates that the constant is of type `BigInt`.</span></span>
<span data-ttu-id="6d0b8-112">Mais detalhes sobre essa representação também podem ser encontrados nas [tabelas da verdade Kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span><span class="sxs-lookup"><span data-stu-id="6d0b8-112">More details on this representation can also be found in the [truth tables kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span></span>

<span data-ttu-id="6d0b8-113">A implementação usa @"microsoft.quantum.intrinsic.cnot" e @"microsoft.quantum.intrinsic.r1" Gates.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-113">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>

## <a name="input"></a><span data-ttu-id="6d0b8-114">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d0b8-114">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="6d0b8-115">Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6d0b8-115">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6d0b8-116">Tabela booliana da verdade representada como um inteiro grande</span><span class="sxs-lookup"><span data-stu-id="6d0b8-116">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="6d0b8-117">controlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6d0b8-117">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6d0b8-118">Registro de qubits de controle</span><span class="sxs-lookup"><span data-stu-id="6d0b8-118">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="6d0b8-119">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6d0b8-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6d0b8-120">Qubit de destino</span><span class="sxs-lookup"><span data-stu-id="6d0b8-120">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="6d0b8-121">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6d0b8-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="6d0b8-122">Referências</span><span class="sxs-lookup"><span data-stu-id="6d0b8-122">References</span></span>

- [<span data-ttu-id="6d0b8-123">*N. Schuch*, *J. Siewert*, PRL 91, no. 027902, 2003, arXiv: Quant-pH/0303063</span><span class="sxs-lookup"><span data-stu-id="6d0b8-123">*N. Schuch*, *J. Siewert*, PRL 91, no. 027902, 2003, arXiv:quant-ph/0303063</span></span>](https://arxiv.org/abs/quant-ph/0303063)
- [<span data-ttu-id="6d0b8-124">*Mathias Soeken*, *Martin Roetteler*, arXiv: 2005.12310</span><span class="sxs-lookup"><span data-stu-id="6d0b8-124">*Mathias Soeken*, *Martin Roetteler*, arXiv:2005.12310</span></span>](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a><span data-ttu-id="6d0b8-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6d0b8-125">See Also</span></span>

- [<span data-ttu-id="6d0b8-126">Microsoft. Quantum. síntese. ApplyXControlledOnTruthTableWithCleanTarget</span><span class="sxs-lookup"><span data-stu-id="6d0b8-126">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)