---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Operação de exp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: b923374a954f90aba2deaead79dd419fbf67fea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693344"
---
# <a name="exp-operation"></a><span data-ttu-id="9d589-102">Operação de exp</span><span class="sxs-lookup"><span data-stu-id="9d589-102">Exp operation</span></span>

<span data-ttu-id="9d589-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="9d589-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="9d589-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9d589-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9d589-105">Aplica o exponencial de um operador qubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="9d589-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="9d589-106">\begin{align} e ^ {i \theta [P_0 \otimes P_1 \cdots P_ {N-1}]}, \end{align} em que $P _i $ é o elemento $i $ th de `paulis` e onde $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="9d589-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="9d589-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9d589-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="9d589-108">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="9d589-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="9d589-109">Matriz de valores de Pauli de qubit único que indicam os fatores de produto tensor em cada qubit.</span><span class="sxs-lookup"><span data-stu-id="9d589-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="9d589-110">teta: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9d589-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9d589-111">Ângulo sobre o operador qubit Pauli fornecido pelo qual o registro de destino deve ser girado.</span><span class="sxs-lookup"><span data-stu-id="9d589-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="9d589-112">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9d589-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9d589-113">Registre-se para aplicar a rotação fornecida ao.</span><span class="sxs-lookup"><span data-stu-id="9d589-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9d589-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d589-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

