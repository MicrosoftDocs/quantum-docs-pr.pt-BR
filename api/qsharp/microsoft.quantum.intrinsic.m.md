---
uid: Microsoft.Quantum.Intrinsic.M
title: Operação M
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: ced3a617a7299e169c7a58a1cd0f83f656b2f0b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212334"
---
# <a name="m-operation"></a><span data-ttu-id="0ea32-102">Operação M</span><span class="sxs-lookup"><span data-stu-id="0ea32-102">M operation</span></span>

<span data-ttu-id="0ea32-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="0ea32-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="0ea32-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0ea32-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="0ea32-105">Executa uma medida de um único qubit na base do Pauli $Z $.</span><span class="sxs-lookup"><span data-stu-id="0ea32-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="0ea32-106">O resultado da saída é fornecido pela distribuição \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span><span class="sxs-lookup"><span data-stu-id="0ea32-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="0ea32-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="0ea32-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="0ea32-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="0ea32-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="0ea32-109">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0ea32-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0ea32-110">Qubit a ser medido.</span><span class="sxs-lookup"><span data-stu-id="0ea32-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="0ea32-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="0ea32-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="0ea32-112">`Zero` Se o $ + $1 eigenvalue for observado e `One` se o eigenvalue $-$1 for observado.</span><span class="sxs-lookup"><span data-stu-id="0ea32-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea32-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ea32-113">Remarks</span></span>

<span data-ttu-id="0ea32-114">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="0ea32-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```