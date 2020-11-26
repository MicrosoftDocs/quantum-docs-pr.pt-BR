---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Função BlockEncodingToReflection
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: 742d4f5623c7c26810998f6c96e2c7b05cc452d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225339"
---
# <a name="blockencodingtoreflection-function"></a><span data-ttu-id="000ea-102">Função BlockEncodingToReflection</span><span class="sxs-lookup"><span data-stu-id="000ea-102">BlockEncodingToReflection function</span></span>

<span data-ttu-id="000ea-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="000ea-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="000ea-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="000ea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="000ea-105">Converte um `BlockEncoding` em um equivalente `BLockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="000ea-105">Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.</span></span>

<span data-ttu-id="000ea-106">Ou seja, dado um `BlockEncoding` unitário $U $ que codifica algum operador $H $ de interesse, converte-o em um `BlockEncodingReflection` $U ' $ que codifica o mesmo operador, mas também satisfaz $U ' ^ \Dagger = U ' $.</span><span class="sxs-lookup"><span data-stu-id="000ea-106">That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$.</span></span>
<span data-ttu-id="000ea-107">Isso aumenta o tamanho do registro auxiliar de $U $ por um qubit.</span><span class="sxs-lookup"><span data-stu-id="000ea-107">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="000ea-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="000ea-108">Input</span></span>

### <a name="blockencoding--blockencoding"></a><span data-ttu-id="000ea-109">blockEncoding: [blockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span><span class="sxs-lookup"><span data-stu-id="000ea-109">blockEncoding : [BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span></span>

<span data-ttu-id="000ea-110">Um `BlockEncoding` unitário $U $ a ser convertido em uma reflexão.</span><span class="sxs-lookup"><span data-stu-id="000ea-110">A `BlockEncoding` unitary $U$ to be converted into a reflection.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="000ea-111">Saída: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="000ea-111">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="000ea-112">Um unitário $U ' $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e satisfaz $U ' ^ \Dagger = U ' $.</span><span class="sxs-lookup"><span data-stu-id="000ea-112">A unitary $U'$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^\dagger = U'$.</span></span>

## <a name="remarks"></a><span data-ttu-id="000ea-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="000ea-113">Remarks</span></span>

<span data-ttu-id="000ea-114">Isso aumenta o tamanho do registro auxiliar de $U $ por um qubit.</span><span class="sxs-lookup"><span data-stu-id="000ea-114">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

## <a name="references"></a><span data-ttu-id="000ea-115">Referências</span><span class="sxs-lookup"><span data-stu-id="000ea-115">References</span></span>

- <span data-ttu-id="000ea-116">Simulação de Hamiltonian por Qubitization Guang Hao Low, Julio L. Chuang https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="000ea-116">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="000ea-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="000ea-117">See Also</span></span>

- [<span data-ttu-id="000ea-118">Microsoft. Quantum. Simulation. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="000ea-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="000ea-119">Microsoft. Quantum. Simulation. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="000ea-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)