---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterTTKAdder
title: Operação ApplyOuterTTKAdder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterTTKAdder
qsharp.summary: Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.
ms.openlocfilehash: afcc3085965907b7478b513028e25d1813cf7b76
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843697"
---
# <a name="applyouterttkadder-operation"></a><span data-ttu-id="1fc18-102">Operação ApplyOuterTTKAdder</span><span class="sxs-lookup"><span data-stu-id="1fc18-102">ApplyOuterTTKAdder operation</span></span>

<span data-ttu-id="1fc18-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1fc18-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1fc18-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1fc18-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1fc18-105">Implementa a operação externa para RippleCarryAdderTTK para conjugar a operação interna para construir o adicionador completo.</span><span class="sxs-lookup"><span data-stu-id="1fc18-105">Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.</span></span>

```qsharp
operation ApplyOuterTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1fc18-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fc18-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="1fc18-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1fc18-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1fc18-108">LittleEndian qubit registrar o primeiro inteiro soma entrada para RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="1fc18-108">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="1fc18-109">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1fc18-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1fc18-110">LittleEndian qubit registrar o segundo inteiro soma entrada para RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="1fc18-110">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1fc18-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1fc18-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="1fc18-112">Referências</span><span class="sxs-lookup"><span data-stu-id="1fc18-112">References</span></span>

- <span data-ttu-id="1fc18-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "circuitos de adição Quantum e Fan-out não vinculado", informações de Quantum e computação, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="1fc18-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530