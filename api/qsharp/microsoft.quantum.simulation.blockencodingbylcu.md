---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: Função BlockEncodingByLCU
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 04738aa54ce8b719b05954824e3553388a995df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697003"
---
# <a name="blockencodingbylcu-function"></a><span data-ttu-id="4e0cd-102">Função BlockEncodingByLCU</span><span class="sxs-lookup"><span data-stu-id="4e0cd-102">BlockEncodingByLCU function</span></span>

<span data-ttu-id="4e0cd-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4e0cd-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4e0cd-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4e0cd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4e0cd-105">Codifica um operador de interesse em um `BlockEncoding` .</span><span class="sxs-lookup"><span data-stu-id="4e0cd-105">Encodes an operator of interest into a `BlockEncoding`.</span></span>

<span data-ttu-id="4e0cd-106">Isso constrói um `BlockEncoding` unitário $U = P\cdot V\cdot P ^ \dagger $ que codifica algum operador $H = \ sum_ {j} | \ alpha_j | U_j $ de interesse que é uma combinação linear de unidades.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-106">This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="4e0cd-107">Normalmente, $P $ é uma \ket de preparação de estado, de modo que $P {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ e $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="4e0cd-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e0cd-108">Input</span></span>

### <a name="statepreparation--t--unit-adj--ctl"></a><span data-ttu-id="4e0cd-109">statePreparation: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="4e0cd-109">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="4e0cd-110">Um unitário $P $ que prepara algum estado de destino.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--ts--unit-adj--ctl"></a><span data-ttu-id="4e0cd-111">seletor: (t, ' s) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="4e0cd-111">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="4e0cd-112">Um unitário $V $ que codifica as unidades de componente de $H $.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--ts--unit-adj--ctl"></a><span data-ttu-id="4e0cd-113">Saída: (t, ' s) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="4e0cd-113">Output : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="4e0cd-114">Um unitário $U $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e satisfaz $U ^ \Dagger = U $.</span><span class="sxs-lookup"><span data-stu-id="4e0cd-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U^\dagger = U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4e0cd-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="4e0cd-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4e0cd-116">T'</span><span class="sxs-lookup"><span data-stu-id="4e0cd-116">'T</span></span>


### <a name="s"></a><span data-ttu-id="4e0cd-117">Do</span><span class="sxs-lookup"><span data-stu-id="4e0cd-117">'S</span></span>



## <a name="remarks"></a><span data-ttu-id="4e0cd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e0cd-118">Remarks</span></span>

<span data-ttu-id="4e0cd-119">Essa `BlockEncoding` implementação fornece as propriedades de um `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="4e0cd-119">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e0cd-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4e0cd-120">See Also</span></span>

- [<span data-ttu-id="4e0cd-121">Microsoft. Quantum. Simulation. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="4e0cd-121">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="4e0cd-122">Microsoft. Quantum. Simulation. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="4e0cd-122">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)