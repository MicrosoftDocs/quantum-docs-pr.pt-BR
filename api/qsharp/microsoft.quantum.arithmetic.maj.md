---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Operação MAJ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: c1801d1d7ed04ead11b672f24d44a94989cf8f1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694767"
---
# <a name="maj-operation"></a><span data-ttu-id="9063e-102">Operação MAJ</span><span class="sxs-lookup"><span data-stu-id="9063e-102">MAJ operation</span></span>

<span data-ttu-id="9063e-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9063e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9063e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9063e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9063e-105">Isso aplica a operação da maioria no local a 3 qubits.</span><span class="sxs-lookup"><span data-stu-id="9063e-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="9063e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9063e-106">Description</span></span>

<span data-ttu-id="9063e-107">Se denotarmos o estado do qubit de destino como $ \ket{z} $ e os Estados de entrada da entrada qubits como $ \ket{x} $ e $ \ket{y} $, essa operação executará a seguinte transformação: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="9063e-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="9063e-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="9063e-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="9063e-109">input0: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9063e-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9063e-110">O primeiro qubit de entrada.</span><span class="sxs-lookup"><span data-stu-id="9063e-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="9063e-111">entrada1: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9063e-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9063e-112">O segundo qubit de entrada.</span><span class="sxs-lookup"><span data-stu-id="9063e-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9063e-113">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9063e-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9063e-114">Um qubit para o qual a função principal será aplicada.</span><span class="sxs-lookup"><span data-stu-id="9063e-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9063e-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9063e-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

