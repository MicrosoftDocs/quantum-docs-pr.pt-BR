---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: Função BlockEncodingByLCU
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 1d7890e96513817c127ef768f49c0b915ea22fa1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858153"
---
# <a name="blockencodingbylcu-function"></a><span data-ttu-id="6f1b7-102">Função BlockEncodingByLCU</span><span class="sxs-lookup"><span data-stu-id="6f1b7-102">BlockEncodingByLCU function</span></span>

<span data-ttu-id="6f1b7-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6f1b7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6f1b7-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6f1b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6f1b7-105">Codifica um operador de interesse em um `BlockEncoding` .</span><span class="sxs-lookup"><span data-stu-id="6f1b7-105">Encodes an operator of interest into a `BlockEncoding`.</span></span>

<span data-ttu-id="6f1b7-106">Isso constrói um `BlockEncoding` unitário $U = P\cdot V\cdot P ^ \dagger $ que codifica algum operador $H = \ sum_ {j} | \ alpha_j | U_j $ de interesse que é uma combinação linear de unidades.</span><span class="sxs-lookup"><span data-stu-id="6f1b7-106">This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="6f1b7-107">Normalmente, $P $ é uma \ket de preparação de estado, de modo que $P {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ e $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.</span><span class="sxs-lookup"><span data-stu-id="6f1b7-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="6f1b7-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f1b7-108">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="6f1b7-109">statePreparation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="6f1b7-109">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="6f1b7-110">Um unitário $P $ que prepara algum estado de destino.</span><span class="sxs-lookup"><span data-stu-id="6f1b7-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="6f1b7-111">seletor: (t, ' s) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="6f1b7-111">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="6f1b7-112">Um unitário $V $ que codifica as unidades de componente de $H $.</span><span class="sxs-lookup"><span data-stu-id="6f1b7-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--ts--unit--is-adj--ctl"></a><span data-ttu-id="6f1b7-113">Saída: (t, ' s) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="6f1b7-113">Output : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="6f1b7-114">Um unitário $U $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e satisfaz $U ^ \Dagger = U $.</span><span class="sxs-lookup"><span data-stu-id="6f1b7-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U^\dagger = U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6f1b7-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="6f1b7-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6f1b7-116">T'</span><span class="sxs-lookup"><span data-stu-id="6f1b7-116">'T</span></span>


### <a name="s"></a><span data-ttu-id="6f1b7-117">Do</span><span class="sxs-lookup"><span data-stu-id="6f1b7-117">'S</span></span>



## <a name="remarks"></a><span data-ttu-id="6f1b7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f1b7-118">Remarks</span></span>

<span data-ttu-id="6f1b7-119">Essa `BlockEncoding` implementação fornece as propriedades de um `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="6f1b7-119">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f1b7-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6f1b7-120">See Also</span></span>

- [<span data-ttu-id="6f1b7-121">Microsoft. Quantum. Simulation. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="6f1b7-121">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="6f1b7-122">Microsoft. Quantum. Simulation. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="6f1b7-122">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)