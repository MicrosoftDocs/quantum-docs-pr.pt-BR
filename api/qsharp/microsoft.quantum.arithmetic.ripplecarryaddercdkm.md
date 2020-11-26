---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: Operação RippleCarryAdderCDKM
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: b08d8823fd539263205aca1ee15ee69adcb163b7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222092"
---
# <a name="ripplecarryaddercdkm-operation"></a><span data-ttu-id="22ab0-102">Operação RippleCarryAdderCDKM</span><span class="sxs-lookup"><span data-stu-id="22ab0-102">RippleCarryAdderCDKM operation</span></span>

<span data-ttu-id="22ab0-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="22ab0-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="22ab0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="22ab0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="22ab0-105">Reversível, ondulado no local, adição de dois inteiros.</span><span class="sxs-lookup"><span data-stu-id="22ab0-105">Reversible, in-place ripple-carry addition of two integers.</span></span>

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="22ab0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="22ab0-106">Description</span></span>

<span data-ttu-id="22ab0-107">Dado dois $n inteiros de $ bit codificados em registros de LittleEndian `xs` e `ys` , e um qubit de transporte, a operação computa a soma dos dois inteiros em que o $n $ menos significativo bits do resultado são mantidos `ys` e o bit de execução é XORed para o qubit `carry` .</span><span class="sxs-lookup"><span data-stu-id="22ab0-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

## <a name="input"></a><span data-ttu-id="22ab0-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="22ab0-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="22ab0-109">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="22ab0-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="22ab0-110">LittleEndian qubit registrar o primeiro soma inteiro.</span><span class="sxs-lookup"><span data-stu-id="22ab0-110">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="22ab0-111">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="22ab0-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="22ab0-112">LittleEndian qubit a codificação do segundo inteiro soma, é modificada para conter os bits do n menos significativos da soma.</span><span class="sxs-lookup"><span data-stu-id="22ab0-112">LittleEndian qubit register encoding the second integer summand, is modified to hold the n least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="22ab0-113">transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="22ab0-113">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="22ab0-114">Qubit, é XORed com o bit mais significativo da soma.</span><span class="sxs-lookup"><span data-stu-id="22ab0-114">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="22ab0-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="22ab0-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="22ab0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="22ab0-116">Remarks</span></span>

<span data-ttu-id="22ab0-117">Esta operação tem a mesma funcionalidade que RippleCarryAdderD, mas usa apenas um qubit auxiliar em vez de $n $.</span><span class="sxs-lookup"><span data-stu-id="22ab0-117">This operation has the same functionality as RippleCarryAdderD, but only uses one auxiliary qubit instead of $n$.</span></span>

## <a name="references"></a><span data-ttu-id="22ab0-118">Referências</span><span class="sxs-lookup"><span data-stu-id="22ab0-118">References</span></span>

- <span data-ttu-id="22ab0-119">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A New Quantum-balcão de adição de", 2004.</span><span class="sxs-lookup"><span data-stu-id="22ab0-119">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1