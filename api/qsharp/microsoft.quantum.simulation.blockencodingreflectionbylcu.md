---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: Função BlockEncodingReflectionByLCU
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: e1247d961a7ebce798106c24c46d924dd6e6d347
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229470"
---
# <a name="blockencodingreflectionbylcu-function"></a><span data-ttu-id="2b564-102">Função BlockEncodingReflectionByLCU</span><span class="sxs-lookup"><span data-stu-id="2b564-102">BlockEncodingReflectionByLCU function</span></span>

<span data-ttu-id="2b564-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="2b564-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="2b564-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b564-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b564-105">Codifica um operador de interesse em um `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="2b564-105">Encodes an operator of interest into a `BlockEncodingReflection`.</span></span>

<span data-ttu-id="2b564-106">Isso constrói um `BlockEncodingReflection` unitário $U = P\cdot V\cdot P ^ \dagger $ que codifica algum operador $H = \ sum_ {j} | \ alpha_j | U_j $ de interesse que é uma combinação linear de unidades.</span><span class="sxs-lookup"><span data-stu-id="2b564-106">This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="2b564-107">Normalmente, $P $ é uma \ket de preparação de estado, de modo que $P {0} \_ a \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ e $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.</span><span class="sxs-lookup"><span data-stu-id="2b564-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="2b564-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b564-108">Input</span></span>

### <a name="statepreparation--qubit--unit--is-adj--ctl"></a><span data-ttu-id="2b564-109">statePreparation: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="2b564-109">statePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2b564-110">Um unitário $P $ que prepara algum estado de destino.</span><span class="sxs-lookup"><span data-stu-id="2b564-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--qubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="2b564-111">seletor: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="2b564-111">selector : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2b564-112">Um unitário $V $ que codifica as unidades de componente de $H $.</span><span class="sxs-lookup"><span data-stu-id="2b564-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="2b564-113">Saída: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="2b564-113">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="2b564-114">Um unitário $U $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e satisfaz $U ' ^ {-1} = U $.</span><span class="sxs-lookup"><span data-stu-id="2b564-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^{-1} = U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b564-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b564-115">Remarks</span></span>

<span data-ttu-id="2b564-116">Essa `BlockEncoding` implementação fornece as propriedades de um `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="2b564-116">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b564-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2b564-117">See Also</span></span>

- [<span data-ttu-id="2b564-118">Microsoft. Quantum. Simulation. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="2b564-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="2b564-119">Microsoft. Quantum. Simulation. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="2b564-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)