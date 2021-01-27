---
uid: Microsoft.Quantum.Canon.MultiplexerFromGenerator
title: Função MultiplexerFromGenerator
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexerFromGenerator
qsharp.summary: >-
  Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: b86238debe66747ba23c3b41164813594f80b27c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852545"
---
# <a name="multiplexerfromgenerator-function"></a><span data-ttu-id="09e03-102">Função MultiplexerFromGenerator</span><span class="sxs-lookup"><span data-stu-id="09e03-102">MultiplexerFromGenerator function</span></span>

<span data-ttu-id="09e03-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="09e03-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="09e03-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09e03-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="09e03-105">Retorna uma operação unitário com controle de multiplicação $U $ que aplica um $V unitário _j $ quando controlado pelo estado do número n-qubit $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="09e03-105">Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="09e03-106">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="09e03-106">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
function MultiplexerFromGenerator (unitaryGenerator : (Int, (Int -> (Qubit[] => Unit is Adj + Ctl)))) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="09e03-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="09e03-107">Input</span></span>

### <a name="unitarygenerator--intint---qubit--unit--is-adj--ctl"></a><span data-ttu-id="09e03-108">unitaryGenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL)</span><span class="sxs-lookup"><span data-stu-id="09e03-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

<span data-ttu-id="09e03-109">Uma tupla em que o primeiro elemento `Int` é o número de unidades $N $, e o segundo elemento `(Int -> ('T => () is Adj + Ctl))` é uma função que usa um inteiro $j $ em $ [0, N-1] $ e gera a operação unitário $V _J $.</span><span class="sxs-lookup"><span data-stu-id="09e03-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>



## <a name="output--littleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="09e03-110">Saída: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="09e03-110">Output : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="09e03-111">Uma operação unitário com controle de multiplicação $U $ que aplica unidades descritas por `unitaryGenerator` .</span><span class="sxs-lookup"><span data-stu-id="09e03-111">A multiply-controlled unitary operation $U$ that applies unitaries described by `unitaryGenerator`.</span></span>

## <a name="see-also"></a><span data-ttu-id="09e03-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="09e03-112">See Also</span></span>

- [<span data-ttu-id="09e03-113">Microsoft. Quantum. Canon. MultiplexOperationsFromGenerator</span><span class="sxs-lookup"><span data-stu-id="09e03-113">Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)