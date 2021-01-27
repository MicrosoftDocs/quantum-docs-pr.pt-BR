---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: Operação GreaterThan
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: 553efb0fc83f24235cb4a77933bd1d547bbd1fed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846625"
---
# <a name="greaterthan-operation"></a><span data-ttu-id="2876d-102">Operação GreaterThan</span><span class="sxs-lookup"><span data-stu-id="2876d-102">GreaterThan operation</span></span>

<span data-ttu-id="2876d-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2876d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2876d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2876d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2876d-105">Aplica uma comparação maior que entre dois inteiros codificados em registros de qubit, invertendo um qubit de destino com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="2876d-105">Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.</span></span>

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="2876d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2876d-106">Description</span></span>

<span data-ttu-id="2876d-107">Executa uma comparação estritamente maior que de dois inteiros $x $ e $y $, codificados em qubit registra xs e haves.</span><span class="sxs-lookup"><span data-stu-id="2876d-107">Carries out a strictly greater than comparison of two integers $x$ and $y$, encoded in qubit registers xs and ys.</span></span> <span data-ttu-id="2876d-108">Se $x > y $, o resultado qubit será invertido, caso contrário, o resultado qubit reterá seu estado.</span><span class="sxs-lookup"><span data-stu-id="2876d-108">If $x > y$, then the result qubit will be flipped, otherwise the result qubit will retain its state.</span></span>

## <a name="input"></a><span data-ttu-id="2876d-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="2876d-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="2876d-110">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2876d-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2876d-111">LittleEndian qubit registrar a codificação do primeiro inteiro $x $.</span><span class="sxs-lookup"><span data-stu-id="2876d-111">LittleEndian qubit register encoding the first integer $x$.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="2876d-112">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2876d-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2876d-113">LittleEndian qubit a codificação do segundo inteiro $y $.</span><span class="sxs-lookup"><span data-stu-id="2876d-113">LittleEndian qubit register encoding the second integer $y$.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="2876d-114">resultado: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2876d-114">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2876d-115">Qubit único que será invertido se $x > y $.</span><span class="sxs-lookup"><span data-stu-id="2876d-115">Single qubit that will be flipped if $x > y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2876d-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2876d-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2876d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2876d-117">Remarks</span></span>

<span data-ttu-id="2876d-118">Usa o truque que $x-y = (x ' + y) ' $, onde ' denota o complemento de um.</span><span class="sxs-lookup"><span data-stu-id="2876d-118">Uses the trick that $x - y = (x'+y)'$, where ' denotes the one's complement.</span></span>

## <a name="references"></a><span data-ttu-id="2876d-119">Referências</span><span class="sxs-lookup"><span data-stu-id="2876d-119">References</span></span>

- <span data-ttu-id="2876d-120">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A New Quantum-balcão de adição de", 2004.</span><span class="sxs-lookup"><span data-stu-id="2876d-120">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1

- <span data-ttu-id="2876d-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "fatoração usando 2n + 2 qubits com multiplicação modular baseada em Toffoli", 2016 https://arxiv.org/abs/1611.07995</span><span class="sxs-lookup"><span data-stu-id="2876d-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "Factoring using 2n+2 qubits with Toffoli based modular multiplication", 2016 https://arxiv.org/abs/1611.07995</span></span>