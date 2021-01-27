---
uid: Microsoft.Quantum.Intrinsic.M
title: Operação M
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 0037d7f5ad060857c6ca2c863b1d24aca3e338cf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818868"
---
# <a name="m-operation"></a><span data-ttu-id="b45b2-102">Operação M</span><span class="sxs-lookup"><span data-stu-id="b45b2-102">M operation</span></span>

<span data-ttu-id="b45b2-103">Namespace: [Microsoft. Quantum. intrínseco](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="b45b2-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="b45b2-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b45b2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b45b2-105">Executa uma medida de um único qubit na base do Pauli $Z $.</span><span class="sxs-lookup"><span data-stu-id="b45b2-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="b45b2-106">O resultado da saída é fornecido pela distribuição \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span><span class="sxs-lookup"><span data-stu-id="b45b2-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="b45b2-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="b45b2-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="b45b2-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="b45b2-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="b45b2-109">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b45b2-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b45b2-110">Qubit a ser medido.</span><span class="sxs-lookup"><span data-stu-id="b45b2-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="b45b2-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="b45b2-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="b45b2-112">`Zero` Se o $ + $1 eigenvalue for observado e `One` se o eigenvalue $-$1 for observado.</span><span class="sxs-lookup"><span data-stu-id="b45b2-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b45b2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b45b2-113">Remarks</span></span>

<span data-ttu-id="b45b2-114">Equivalente a:</span><span class="sxs-lookup"><span data-stu-id="b45b2-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```