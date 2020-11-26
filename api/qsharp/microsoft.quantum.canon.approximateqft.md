---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Operação ApproximateQFT
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 97a410133e80cc5bffc810e9d6455baaee32364b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207693"
---
# <a name="approximateqft-operation"></a><span data-ttu-id="a95f2-102">Operação ApproximateQFT</span><span class="sxs-lookup"><span data-stu-id="a95f2-102">ApproximateQFT operation</span></span>

<span data-ttu-id="a95f2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a95f2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a95f2-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a95f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a95f2-105">Aplique a transformação de Fourier de Quantum aproximada (AQFT) a um registro do Quantum.</span><span class="sxs-lookup"><span data-stu-id="a95f2-105">Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.</span></span>

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a95f2-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a95f2-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="a95f2-107">r: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a95f2-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a95f2-108">parâmetro de aproximação que determina em qual nível as rotações Z controladas que ocorrem no circuito QFT são removidas.</span><span class="sxs-lookup"><span data-stu-id="a95f2-108">approximation parameter which determines at which level the controlled Z-rotations that occur in the QFT circuit are pruned.</span></span>

<span data-ttu-id="a95f2-109">O parâmetro de aproximação a determina o nível de remoção das rotações Z, ou seja, um ∈ {0.. n} e todas as rotações Z 2π/2K em que k>a são removidas do circuito QFT.</span><span class="sxs-lookup"><span data-stu-id="a95f2-109">The approximation parameter a determines the pruning level of the Z-rotations, i.e., a ∈ {0..n} and all Z-rotations 2π/2ᵏ where k>a are removed from the QFT circuit.</span></span> <span data-ttu-id="a95f2-110">É conhecido que para k >= log ₂ (n) + log ₂ (1/ε) + 3 um pode ser associado | | QFT-AQFT | |<ε.</span><span class="sxs-lookup"><span data-stu-id="a95f2-110">It is known that for k >= log₂(n)+log₂(1/ε)+3 one can bound ||QFT-AQFT||<ε.</span></span>


### <a name="qs--bigendian"></a><span data-ttu-id="a95f2-111">QS: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="a95f2-111">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="a95f2-112">registro da Quantum de n qubits para o qual a transformação de Fourier de Quantum aproximada é aplicada.</span><span class="sxs-lookup"><span data-stu-id="a95f2-112">quantum register of n qubits to which the Approximate Quantum Fourier Transform is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a95f2-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a95f2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a95f2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a95f2-114">Remarks</span></span>

<span data-ttu-id="a95f2-115">AQFT requer Gates de rotação Z do formato 2π/2K e Hadamard Gates.</span><span class="sxs-lookup"><span data-stu-id="a95f2-115">AQFT requires Z-rotation gates of the form 2π/2ᵏ and Hadamard gates.</span></span>

<span data-ttu-id="a95f2-116">Presume-se que a entrada e a saída sejam codificadas na codificação big endian.</span><span class="sxs-lookup"><span data-stu-id="a95f2-116">The input and output are assumed to be encoded in big endian encoding.</span></span>

## <a name="references"></a><span data-ttu-id="a95f2-117">Referências</span><span class="sxs-lookup"><span data-stu-id="a95f2-117">References</span></span>

- [<span data-ttu-id="a95f2-118">*M. Roetteler, th. Beth*, APL. Algebra Eng. Commun. Compute. 19 (3): 177-193 (2008)</span><span class="sxs-lookup"><span data-stu-id="a95f2-118"> *M. Roetteler, Th. Beth*, Appl. Algebra Eng. Commun. Comput. 19(3): 177-193 (2008) </span></span>](http://doi.org/10.1007/s00200-008-0072-2)
- [<span data-ttu-id="a95f2-119">*D. Coppersmith* arXiv: Quant-pH/0201067v1</span><span class="sxs-lookup"><span data-stu-id="a95f2-119"> *D. Coppersmith* arXiv:quant-ph/0201067v1 </span></span>](https://arxiv.org/abs/quant-ph/0201067)