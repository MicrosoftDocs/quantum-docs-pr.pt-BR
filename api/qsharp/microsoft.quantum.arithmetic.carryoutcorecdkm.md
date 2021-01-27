---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Operação CarryOutCoreCDKM
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 2065c767b341241d32e5ac06bcff0071cbadb266
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843336"
---
# <a name="carryoutcorecdkm-operation"></a><span data-ttu-id="78d69-102">Operação CarryOutCoreCDKM</span><span class="sxs-lookup"><span data-stu-id="78d69-102">CarryOutCoreCDKM operation</span></span>

<span data-ttu-id="78d69-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="78d69-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="78d69-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="78d69-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="78d69-105">A operação principal no RippleCarryAdderCDKM, usada com a operação ApplyOuterCDKMAdder acima, ou seja, conjugada com essa operação para obter a operação interna do RippleCarryAdderCDKM.</span><span class="sxs-lookup"><span data-stu-id="78d69-105">The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM.</span></span> <span data-ttu-id="78d69-106">Esta operação computa o qubit de execução e aplica uma sequência de não Gates em parte da entrada `ys` .</span><span class="sxs-lookup"><span data-stu-id="78d69-106">This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.</span></span>

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="78d69-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="78d69-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="78d69-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="78d69-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="78d69-109">Primeiro registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="78d69-109">First qubit register.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="78d69-110">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="78d69-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="78d69-111">Segundo registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="78d69-111">Second qubit register.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="78d69-112">ancilla: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="78d69-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="78d69-113">O ancilla qubit usado em RippleCarryAdderCDKM passado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="78d69-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="78d69-114">transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="78d69-114">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="78d69-115">Execute qubit na operação RippleCarryAdderCDKM.</span><span class="sxs-lookup"><span data-stu-id="78d69-115">Carry out qubit in the RippleCarryAdderCDKM operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="78d69-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="78d69-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="78d69-117">Referências</span><span class="sxs-lookup"><span data-stu-id="78d69-117">References</span></span>

- <span data-ttu-id="78d69-118">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A New Quantum-balcão de adição de", 2004.</span><span class="sxs-lookup"><span data-stu-id="78d69-118">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1