---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderTTK
title: Operação RippleCarryAdderTTK
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: 45ba1b644166029ee548307cc1a7290c48e48a4b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221923"
---
# <a name="ripplecarryadderttk-operation"></a><span data-ttu-id="33340-102">Operação RippleCarryAdderTTK</span><span class="sxs-lookup"><span data-stu-id="33340-102">RippleCarryAdderTTK operation</span></span>

<span data-ttu-id="33340-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="33340-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="33340-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="33340-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="33340-105">Reversível, ondulado no local, adição de dois inteiros.</span><span class="sxs-lookup"><span data-stu-id="33340-105">Reversible, in-place ripple-carry addition of two integers.</span></span>
<span data-ttu-id="33340-106">Dado dois $n inteiros de $ bit codificados em registros de LittleEndian `xs` e `ys` , e um qubit de transporte, a operação computa a soma dos dois inteiros em que o $n $ menos significativo bits do resultado são mantidos `ys` e o bit de execução é XORed para o qubit `carry` .</span><span class="sxs-lookup"><span data-stu-id="33340-106">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

```qsharp
operation RippleCarryAdderTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="33340-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="33340-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="33340-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="33340-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="33340-109">LittleEndian qubit registrar o primeiro soma inteiro.</span><span class="sxs-lookup"><span data-stu-id="33340-109">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="33340-110">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="33340-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="33340-111">LittleEndian qubit a codificação do segundo inteiro soma, é modificado para manter o $n $ menos significativo bits da soma.</span><span class="sxs-lookup"><span data-stu-id="33340-111">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="33340-112">transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="33340-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="33340-113">Qubit, é XORed com o bit mais significativo da soma.</span><span class="sxs-lookup"><span data-stu-id="33340-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="33340-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33340-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="33340-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="33340-115">Remarks</span></span>

<span data-ttu-id="33340-116">Esta operação tem a mesma funcionalidade que RippleCarryAdderD e RippleCarryAdderCDKM, mas não usa nenhuma qubits de ancilla.</span><span class="sxs-lookup"><span data-stu-id="33340-116">This operation has the same functionality as RippleCarryAdderD and, RippleCarryAdderCDKM but does not use any ancilla qubits.</span></span>

## <a name="references"></a><span data-ttu-id="33340-117">Referências</span><span class="sxs-lookup"><span data-stu-id="33340-117">References</span></span>

- <span data-ttu-id="33340-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "circuitos de adição Quantum e Fan-out não vinculado", informações de Quantum e computação, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="33340-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530