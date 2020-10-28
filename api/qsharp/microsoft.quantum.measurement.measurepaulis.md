---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Operação MeasurePaulis
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 7348ab3941af391c451d5c66f888cf3b6662cf20
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694655"
---
# <a name="measurepaulis-operation"></a><span data-ttu-id="787ea-102">Operação MeasurePaulis</span><span class="sxs-lookup"><span data-stu-id="787ea-102">MeasurePaulis operation</span></span>

<span data-ttu-id="787ea-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="787ea-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="787ea-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="787ea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="787ea-105">Dada uma matriz de operadores qubit Pauli, mede cada um deles usando um gadget de medida especificado e, em seguida, retorna a matriz de resultados.</span><span class="sxs-lookup"><span data-stu-id="787ea-105">Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.</span></span>

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a><span data-ttu-id="787ea-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="787ea-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="787ea-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="787ea-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="787ea-108">Matriz de operadores qubit Pauli para medir.</span><span class="sxs-lookup"><span data-stu-id="787ea-108">Array of multi-qubit Pauli operators to measure.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="787ea-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="787ea-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="787ea-110">Registre-se para medir os operadores fornecidos.</span><span class="sxs-lookup"><span data-stu-id="787ea-110">Register on which to measure the given operators.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="787ea-111">gadget: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="787ea-111">gadget : ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="787ea-112">Operação que executa a medição de um determinado operador qubit.</span><span class="sxs-lookup"><span data-stu-id="787ea-112">Operation which performs the measurement of a given multi-qubit operator.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="787ea-113">Saída: __inválido <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="787ea-113">Output : __invalid<Result>__ []</span></span>

<span data-ttu-id="787ea-114">A matriz de resultados obtidos na medição de cada elemento de `paulis` on `target` .</span><span class="sxs-lookup"><span data-stu-id="787ea-114">The array of results obtained from measuring each element of `paulis` on `target`.</span></span>