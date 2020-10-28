---
uid: Microsoft.Quantum.Canon.RAll0
title: Operação RAll0
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll0
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.
ms.openlocfilehash: 6185e66e08d2af3aa0b35791638820b4dcc5af35
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693931"
---
# <a name="rall0-operation"></a><span data-ttu-id="c4fa4-102">Operação RAll0</span><span class="sxs-lookup"><span data-stu-id="c4fa4-102">RAll0 operation</span></span>

<span data-ttu-id="c4fa4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c4fa4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c4fa4-105">Executa uma operação de alternância de fase.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-105">Performs a phase shift operation.</span></span>

<span data-ttu-id="c4fa4-106">$R = \boldone-(1-e ^ {i \phi}) \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-106">$R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>

```qsharp
operation RAll0 (phase : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c4fa4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4fa4-107">Input</span></span>

### <a name="phase--double"></a><span data-ttu-id="c4fa4-108">fase: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-108">phase : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c4fa4-109">A fase $ \phi $ aplicada ao estado $ \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-109">The phase $\phi$ applied to state $\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="c4fa4-110">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c4fa4-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c4fa4-111">O registro cujo estado deve ser girado por $R $.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-111">The register whose state is to be rotated by $R$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c4fa4-112">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c4fa4-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c4fa4-113">See Also</span></span>

- [<span data-ttu-id="c4fa4-114">Microsoft. Quantum. Canon. RAll1</span><span class="sxs-lookup"><span data-stu-id="c4fa4-114">Microsoft.Quantum.Canon.RAll1</span></span>](xref:Microsoft.Quantum.Canon.RAll1)