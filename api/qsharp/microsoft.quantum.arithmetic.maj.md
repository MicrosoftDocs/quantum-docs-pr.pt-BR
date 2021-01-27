---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Operação MAJ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 68236f1deeb409a01152d4b7e854202a1134314e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846540"
---
# <a name="maj-operation"></a><span data-ttu-id="985f0-102">Operação MAJ</span><span class="sxs-lookup"><span data-stu-id="985f0-102">MAJ operation</span></span>

<span data-ttu-id="985f0-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="985f0-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="985f0-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="985f0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="985f0-105">Isso aplica a operação da maioria no local a 3 qubits.</span><span class="sxs-lookup"><span data-stu-id="985f0-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="985f0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="985f0-106">Description</span></span>

<span data-ttu-id="985f0-107">Se denotarmos o estado do qubit de destino como $ \ket{z} $ e os Estados de entrada da entrada qubits como $ \ket{x} $ e $ \ket{y} $, essa operação executará a seguinte transformação: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="985f0-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="985f0-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="985f0-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="985f0-109">input0: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="985f0-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="985f0-110">O primeiro qubit de entrada.</span><span class="sxs-lookup"><span data-stu-id="985f0-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="985f0-111">entrada1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="985f0-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="985f0-112">O segundo qubit de entrada.</span><span class="sxs-lookup"><span data-stu-id="985f0-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="985f0-113">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="985f0-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="985f0-114">Um qubit para o qual a função principal será aplicada.</span><span class="sxs-lookup"><span data-stu-id="985f0-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="985f0-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="985f0-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

