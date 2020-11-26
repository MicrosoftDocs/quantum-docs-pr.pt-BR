---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterTTKAdder
title: Operação ApplyOuterTTKAdder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterTTKAdder
qsharp.summary: Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.
ms.openlocfilehash: aed15a4d1f3ca7121d6da665f5c08442fd495619
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190608"
---
# <a name="applyouterttkadder-operation"></a><span data-ttu-id="a7db9-102">Operação ApplyOuterTTKAdder</span><span class="sxs-lookup"><span data-stu-id="a7db9-102">ApplyOuterTTKAdder operation</span></span>

<span data-ttu-id="a7db9-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a7db9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a7db9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a7db9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a7db9-105">Implementa a operação externa para RippleCarryAdderTTK para conjugar a operação interna para construir o adicionador completo.</span><span class="sxs-lookup"><span data-stu-id="a7db9-105">Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.</span></span>

```qsharp
operation ApplyOuterTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a7db9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7db9-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="a7db9-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a7db9-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a7db9-108">LittleEndian qubit registrar o primeiro inteiro soma entrada para RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="a7db9-108">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="a7db9-109">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a7db9-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a7db9-110">LittleEndian qubit registrar o segundo inteiro soma entrada para RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="a7db9-110">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a7db9-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7db9-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="a7db9-112">Referências</span><span class="sxs-lookup"><span data-stu-id="a7db9-112">References</span></span>

- <span data-ttu-id="a7db9-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "circuitos de adição Quantum e Fan-out não vinculado", informações de Quantum e computação, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="a7db9-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530