---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Operação ReflectAboutInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: d4bae0cba5ee45e8d48070e36efab0159ade9137
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222364"
---
# <a name="reflectaboutinteger-operation"></a><span data-ttu-id="94c4a-102">Operação ReflectAboutInteger</span><span class="sxs-lookup"><span data-stu-id="94c4a-102">ReflectAboutInteger operation</span></span>

<span data-ttu-id="94c4a-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="94c4a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="94c4a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94c4a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="94c4a-105">Reflete um registro quântico sobre um determinado inteiro clássico.</span><span class="sxs-lookup"><span data-stu-id="94c4a-105">Reflects a quantum register about a given classical integer.</span></span>

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="94c4a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="94c4a-106">Description</span></span>

<span data-ttu-id="94c4a-107">Considerando um registro Quantum inicialmente no estado $ \ sum_i \ alpha_i \ket{i} $, em que cada $ \ket{i} $ é um estado base que representa um inteiro $i $, reflete o estado do registro sobre o estado base de um determinado inteiro $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $</span><span class="sxs-lookup"><span data-stu-id="94c4a-107">Given a quantum register initially in the state $\sum_i \alpha_i \ket{i}$, where each $\ket{i}$ is a basis state representing an integer $i$, reflects the state of the register about the basis state for a given integer $\ket{j}$, $$ \sum_i (-1)^{ \delta_{ij} } \alpha_i \ket{i} $$</span></span>

## <a name="input"></a><span data-ttu-id="94c4a-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="94c4a-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="94c4a-109">índice: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="94c4a-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="94c4a-110">O inteiro clássico que indexa o estado base sobre o qual refletir.</span><span class="sxs-lookup"><span data-stu-id="94c4a-110">The classical integer indexing the basis state about which to reflect.</span></span>


### <a name="reg--littleendian"></a><span data-ttu-id="94c4a-111">Reg: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="94c4a-111">reg : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="94c4a-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="94c4a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="94c4a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="94c4a-113">Remarks</span></span>

<span data-ttu-id="94c4a-114">Esta operação é implementada in-loco, sem a alocação explícita de qubits auxiliares adicionais.</span><span class="sxs-lookup"><span data-stu-id="94c4a-114">This operation is implemented in-place, without explicit allocation of additional auxiliary qubits.</span></span>