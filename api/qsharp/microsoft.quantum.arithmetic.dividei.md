---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Operação de divisão
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 0cc16dddc27a000dbc30de6ae27976a01fd9f4ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694801"
---
# <a name="dividei-operation"></a><span data-ttu-id="dd82a-102">Operação de divisão</span><span class="sxs-lookup"><span data-stu-id="dd82a-102">DivideI operation</span></span>

<span data-ttu-id="dd82a-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="dd82a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="dd82a-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dd82a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dd82a-105">Divide dois inteiros de Quantum.</span><span class="sxs-lookup"><span data-stu-id="dd82a-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="dd82a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd82a-106">Description</span></span>

<span data-ttu-id="dd82a-107">`xs` manterá o restante `xs - floor(xs/ys) * ys` e `result` será mantido `floor(xs/ys)` .</span><span class="sxs-lookup"><span data-stu-id="dd82a-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="dd82a-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="dd82a-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="dd82a-109">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="dd82a-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="dd82a-110">$n dividendo de $ bits, será substituído pelo restante.</span><span class="sxs-lookup"><span data-stu-id="dd82a-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="dd82a-111">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="dd82a-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="dd82a-112">divisor de $ bits $n</span><span class="sxs-lookup"><span data-stu-id="dd82a-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="dd82a-113">resultado: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="dd82a-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="dd82a-114">$n resultado de $ bit, deve estar no estado $ \ket {0} $ inicialmente e será substituído pelo resultado da divisão de inteiro.</span><span class="sxs-lookup"><span data-stu-id="dd82a-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dd82a-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dd82a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dd82a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd82a-116">Remarks</span></span>

<span data-ttu-id="dd82a-117">Usa uma abordagem Shift-and-Subtract padrão para implementar a divisão.</span><span class="sxs-lookup"><span data-stu-id="dd82a-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="dd82a-118">A versão controlada é especializada, pois a subtração não requer controles adicionais.</span><span class="sxs-lookup"><span data-stu-id="dd82a-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>