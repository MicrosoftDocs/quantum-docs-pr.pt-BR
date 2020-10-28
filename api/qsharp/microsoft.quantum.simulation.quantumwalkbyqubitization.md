---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: Função QuantumWalkByQubitization
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: ef9740f1867cee3c79a7ec0bf90f2c2f4b39ad28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697105"
---
# <a name="quantumwalkbyqubitization-function"></a><span data-ttu-id="86de2-102">Função QuantumWalkByQubitization</span><span class="sxs-lookup"><span data-stu-id="86de2-102">QuantumWalkByQubitization function</span></span>

<span data-ttu-id="86de2-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="86de2-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="86de2-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86de2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86de2-105">Converte uma reflexão de codificação de bloco em uma Walk de Quantum.</span><span class="sxs-lookup"><span data-stu-id="86de2-105">Converts a block-encoding reflection into a quantum walk.</span></span>

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="86de2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="86de2-106">Description</span></span>

<span data-ttu-id="86de2-107">Dado um `BlockEncodingReflection` representado por um unitário $U $ que codifica algum operador $H $ de interesse, converte-o em uma passagem quantum $W $ contendo o espectro de $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.</span><span class="sxs-lookup"><span data-stu-id="86de2-107">Given a `BlockEncodingReflection` represented by a unitary $U$ that encodes some operator $H$ of interest, converts it into a quantum walk $W$ containing the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="input"></a><span data-ttu-id="86de2-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="86de2-108">Input</span></span>

### <a name="blockencoding--blockencodingreflection"></a><span data-ttu-id="86de2-109">blockEncoding: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="86de2-109">blockEncoding : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="86de2-110">Um `BlockEncodingReflection` unitário $U $ a ser convertido em uma Walk de Quantum.</span><span class="sxs-lookup"><span data-stu-id="86de2-110">A `BlockEncodingReflection` unitary $U$ to be converted into a Quantum walk.</span></span>



## <a name="output--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="86de2-111">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit) adj + CTL</span><span class="sxs-lookup"><span data-stu-id="86de2-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="86de2-112">Uma Walk do Quantum $W $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e contém o espectro de $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.</span><span class="sxs-lookup"><span data-stu-id="86de2-112">A quantum walk $W$ acting jointly on registers `a` and `s` that block- encodes $H$, and contains the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="references"></a><span data-ttu-id="86de2-113">Referências</span><span class="sxs-lookup"><span data-stu-id="86de2-113">References</span></span>

- <span data-ttu-id="86de2-114">Simulação de Hamiltonian por Qubitization Guang Hao Low, Julio L. Chuang https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="86de2-114">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="86de2-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="86de2-115">See Also</span></span>

- [<span data-ttu-id="86de2-116">Microsoft. Quantum. Simulation. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="86de2-116">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="86de2-117">Microsoft. Quantum. Simulation. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="86de2-117">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)