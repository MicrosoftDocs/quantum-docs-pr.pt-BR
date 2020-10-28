---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdderWithoutCarry
title: Operação ApplyInnerTTKAdderWithoutCarry
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdderWithoutCarry
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 3335c63b8509090deed1172419158da0d5e80409
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694872"
---
# <a name="applyinnerttkadderwithoutcarry-operation"></a><span data-ttu-id="43b3b-102">Operação ApplyInnerTTKAdderWithoutCarry</span><span class="sxs-lookup"><span data-stu-id="43b3b-102">ApplyInnerTTKAdderWithoutCarry operation</span></span>

<span data-ttu-id="43b3b-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="43b3b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="43b3b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="43b3b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="43b3b-105">Implementa a função de adição interna para a operação RippleCarryAdderNoCarryTTK.</span><span class="sxs-lookup"><span data-stu-id="43b3b-105">Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK.</span></span> <span data-ttu-id="43b3b-106">Essa é a operação interna que está conjugada com a operação externa para construir o adicionador completo.</span><span class="sxs-lookup"><span data-stu-id="43b3b-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdderWithoutCarry (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="43b3b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="43b3b-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="43b3b-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="43b3b-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="43b3b-109">LittleEndian qubit registrar o primeiro inteiro soma entrada para RippleCarryAdderNoCarryTTK.</span><span class="sxs-lookup"><span data-stu-id="43b3b-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderNoCarryTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="43b3b-110">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="43b3b-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="43b3b-111">LittleEndian qubit registrar o segundo inteiro soma entrada para RippleCarryAdderNoCarryTTK.</span><span class="sxs-lookup"><span data-stu-id="43b3b-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderNoCarryTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="43b3b-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43b3b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="43b3b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="43b3b-113">Remarks</span></span>

<span data-ttu-id="43b3b-114">A operação controlada especificada faz uso de simetria e cancelamento mútuo de operações para melhorar a implementação padrão que adiciona um controle a cada operação.</span><span class="sxs-lookup"><span data-stu-id="43b3b-114">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="43b3b-115">Referências</span><span class="sxs-lookup"><span data-stu-id="43b3b-115">References</span></span>

- <span data-ttu-id="43b3b-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "circuitos de adição Quantum e Fan-out não vinculado", informações de Quantum e computação, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="43b3b-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530