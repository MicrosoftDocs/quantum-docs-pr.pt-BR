---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Operação ApplyOuterCDKMAdder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: 81311a75beedb62331184faf4e1523f3ccc74f43
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190659"
---
# <a name="applyoutercdkmadder-operation"></a><span data-ttu-id="f7dd9-102">Operação ApplyOuterCDKMAdder</span><span class="sxs-lookup"><span data-stu-id="f7dd9-102">ApplyOuterCDKMAdder operation</span></span>

<span data-ttu-id="f7dd9-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f7dd9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f7dd9-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f7dd9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f7dd9-105">Operação reversível, Ripple in-loco-transporte que é usada na operação de adição de inteiro RippleCarryAdderCDKM abaixo.</span><span class="sxs-lookup"><span data-stu-id="f7dd9-105">Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below.</span></span>
<span data-ttu-id="f7dd9-106">Considerando dois registros `xs` de qubit e `ys` do mesmo comprimento, a operação aplica uma sequência de enrolamento de CNOT e CCNOT Gates com qubits no `xs` e `ys` como os controles e qubits `xs` como os destinos.</span><span class="sxs-lookup"><span data-stu-id="f7dd9-106">Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.</span></span>

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f7dd9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7dd9-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="f7dd9-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f7dd9-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f7dd9-109">Primeiro registro de qubit, que contém controles e destinos.</span><span class="sxs-lookup"><span data-stu-id="f7dd9-109">First qubit register, containing controls and targets.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="f7dd9-110">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f7dd9-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f7dd9-111">Segundo registro de qubit, contribuindo para os controles.</span><span class="sxs-lookup"><span data-stu-id="f7dd9-111">Second qubit register, contributing to the controls.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="f7dd9-112">ancilla: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f7dd9-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f7dd9-113">O ancilla qubit usado em RippleCarryAdderCDKM passado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="f7dd9-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7dd9-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7dd9-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="f7dd9-115">Referências</span><span class="sxs-lookup"><span data-stu-id="f7dd9-115">References</span></span>

- <span data-ttu-id="f7dd9-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A New Quantum-balcão de adição de", 2004.</span><span class="sxs-lookup"><span data-stu-id="f7dd9-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1