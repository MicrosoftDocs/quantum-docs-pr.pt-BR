---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: Operação ResetAll
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: 00b7c0f508d76fb0f5b46c7ec00c0718469365a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693328"
---
# <a name="resetall-operation"></a><span data-ttu-id="34dc8-102">Operação ResetAll</span><span class="sxs-lookup"><span data-stu-id="34dc8-102">ResetAll operation</span></span>

<span data-ttu-id="34dc8-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="34dc8-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="34dc8-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34dc8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34dc8-105">Dada uma matriz de qubits, meça-os e verifique se estão no estado | 0 ⟩, de modo que eles possam ser liberados com segurança.</span><span class="sxs-lookup"><span data-stu-id="34dc8-105">Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.</span></span>

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="34dc8-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="34dc8-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="34dc8-107">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="34dc8-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="34dc8-108">Uma matriz de qubits cujos Estados devem ser redefinidos para $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="34dc8-108">An array of qubits whose states are to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="34dc8-109">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34dc8-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

