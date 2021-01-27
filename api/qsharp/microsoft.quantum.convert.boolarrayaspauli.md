---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Função BoolArrayAsPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c11ca05ad8a939d704547c65a8e8a6537d0df4b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834243"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="e8c4a-102">Função BoolArrayAsPauli</span><span class="sxs-lookup"><span data-stu-id="e8c4a-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="e8c4a-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="e8c4a-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="e8c4a-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8c4a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8c4a-105">Dada uma cadeia de caracteres de bits, retorna um operador qubit Pauli representado como uma matriz de operadores de Pauli de qubit único.</span><span class="sxs-lookup"><span data-stu-id="e8c4a-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="e8c4a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8c4a-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="e8c4a-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e8c4a-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e8c4a-108">Operador Pauli a ser aplicado a qubits onde `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="e8c4a-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="e8c4a-109">bitApply: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e8c4a-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e8c4a-110">Aplique Pauli se bit for esse valor.</span><span class="sxs-lookup"><span data-stu-id="e8c4a-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="e8c4a-111">bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="e8c4a-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="e8c4a-112">Matriz booliana.</span><span class="sxs-lookup"><span data-stu-id="e8c4a-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="e8c4a-113">Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="e8c4a-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="e8c4a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8c4a-114">Remarks</span></span>

<span data-ttu-id="e8c4a-115">A matriz booliana e o registro do Quantum devem ser de comprimento igual.</span><span class="sxs-lookup"><span data-stu-id="e8c4a-115">The Boolean array and the quantum register must be of equal length.</span></span>