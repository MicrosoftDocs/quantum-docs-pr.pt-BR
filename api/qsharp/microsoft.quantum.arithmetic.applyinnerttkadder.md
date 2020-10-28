---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdder
title: Operação ApplyInnerTTKAdder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdder
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 23c1f6dcdf3894cf1b416efd922c9eed01ac8f85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694874"
---
# <a name="applyinnerttkadder-operation"></a><span data-ttu-id="ed652-102">Operação ApplyInnerTTKAdder</span><span class="sxs-lookup"><span data-stu-id="ed652-102">ApplyInnerTTKAdder operation</span></span>

<span data-ttu-id="ed652-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ed652-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ed652-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ed652-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ed652-105">Implementa a função de adição interna para a operação RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="ed652-105">Implements the inner addition function for the operation RippleCarryAdderTTK.</span></span> <span data-ttu-id="ed652-106">Essa é a operação interna que está conjugada com a operação externa para construir o adicionador completo.</span><span class="sxs-lookup"><span data-stu-id="ed652-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="ed652-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed652-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="ed652-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ed652-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ed652-109">LittleEndian qubit registrar o primeiro inteiro soma entrada para RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="ed652-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="ed652-110">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ed652-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ed652-111">LittleEndian qubit registrar o segundo inteiro soma entrada para RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="ed652-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="ed652-112">transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ed652-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ed652-113">Qubit, é XORed com o bit mais significativo da soma.</span><span class="sxs-lookup"><span data-stu-id="ed652-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ed652-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed652-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ed652-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed652-115">Remarks</span></span>

<span data-ttu-id="ed652-116">A operação controlada especificada faz uso de simetria e cancelamento mútuo de operações para melhorar a implementação padrão que adiciona um controle a cada operação.</span><span class="sxs-lookup"><span data-stu-id="ed652-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="ed652-117">Referências</span><span class="sxs-lookup"><span data-stu-id="ed652-117">References</span></span>

- <span data-ttu-id="ed652-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "circuitos de adição Quantum e Fan-out não vinculado", informações de Quantum e computação, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="ed652-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530