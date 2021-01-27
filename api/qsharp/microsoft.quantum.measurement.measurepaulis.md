---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Operação MeasurePaulis
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 1bc14ec8e7c608d1195a03a354c71e870594f86d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853778"
---
# <a name="measurepaulis-operation"></a><span data-ttu-id="a85b5-102">Operação MeasurePaulis</span><span class="sxs-lookup"><span data-stu-id="a85b5-102">MeasurePaulis operation</span></span>

<span data-ttu-id="a85b5-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="a85b5-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="a85b5-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a85b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a85b5-105">Dada uma matriz de operadores qubit Pauli, mede cada um deles usando um gadget de medida especificado e, em seguida, retorna a matriz de resultados.</span><span class="sxs-lookup"><span data-stu-id="a85b5-105">Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.</span></span>

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a><span data-ttu-id="a85b5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="a85b5-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="a85b5-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="a85b5-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="a85b5-108">Matriz de operadores qubit Pauli para medir.</span><span class="sxs-lookup"><span data-stu-id="a85b5-108">Array of multi-qubit Pauli operators to measure.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="a85b5-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a85b5-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a85b5-110">Registre-se para medir os operadores fornecidos.</span><span class="sxs-lookup"><span data-stu-id="a85b5-110">Register on which to measure the given operators.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="a85b5-111">gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="a85b5-111">gadget : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="a85b5-112">Operação que executa a medição de um determinado operador qubit.</span><span class="sxs-lookup"><span data-stu-id="a85b5-112">Operation which performs the measurement of a given multi-qubit operator.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a85b5-113">Saída: __inválido <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="a85b5-113">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="a85b5-114">A matriz de resultados obtidos na medição de cada elemento de `paulis` on `target` .</span><span class="sxs-lookup"><span data-stu-id="a85b5-114">The array of results obtained from measuring each element of `paulis` on `target`.</span></span>