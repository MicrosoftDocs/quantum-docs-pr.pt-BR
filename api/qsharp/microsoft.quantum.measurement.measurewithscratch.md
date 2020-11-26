---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Operação MeasureWithScratch
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: c42316a811e0e4a81c7f244c093a2be88fe5c733
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227056"
---
# <a name="measurewithscratch-operation"></a><span data-ttu-id="020cb-102">Operação MeasureWithScratch</span><span class="sxs-lookup"><span data-stu-id="020cb-102">MeasureWithScratch operation</span></span>

<span data-ttu-id="020cb-103">Namespace: [Microsoft. Quantum. medição](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="020cb-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="020cb-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="020cb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="020cb-105">Mede o operador Pauli fornecido usando um qubit de rascunho explícito para executar a medição.</span><span class="sxs-lookup"><span data-stu-id="020cb-105">Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.</span></span>

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="020cb-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="020cb-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="020cb-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="020cb-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="020cb-108">Um operador qubit Pauli especificado como uma matriz de operadores de Pauli de qubit único.</span><span class="sxs-lookup"><span data-stu-id="020cb-108">A multi-qubit Pauli operator specified as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="020cb-109">destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="020cb-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="020cb-110">Qubit o registro a ser medido.</span><span class="sxs-lookup"><span data-stu-id="020cb-110">Qubit register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="020cb-111">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="020cb-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="020cb-112">O resultado da medição do operador Pauli fornecido no `target` registro.</span><span class="sxs-lookup"><span data-stu-id="020cb-112">The result of measuring the given Pauli operator on the `target` register.</span></span>