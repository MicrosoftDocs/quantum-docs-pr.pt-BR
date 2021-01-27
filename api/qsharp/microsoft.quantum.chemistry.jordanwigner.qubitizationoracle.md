---
uid: Microsoft.Quantum.Chemistry.JordanWigner.QubitizationOracle
title: Função QubitizationOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: QubitizationOracle
qsharp.summary: Returns Qubitization operation and the parameters necessary to run it.
ms.openlocfilehash: cf6fe04b3f629c4ca4a7c27d8519a4cb42d07630
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835846"
---
# <a name="qubitizationoracle-function"></a><span data-ttu-id="1c623-102">Função QubitizationOracle</span><span class="sxs-lookup"><span data-stu-id="1c623-102">QubitizationOracle function</span></span>

<span data-ttu-id="1c623-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="1c623-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="1c623-104">Pacote: [Microsoft. Quantum. química](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="1c623-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="1c623-105">Retorna a operação Qubitization e os parâmetros necessários para executá-la.</span><span class="sxs-lookup"><span data-stu-id="1c623-105">Returns Qubitization operation and the parameters necessary to run it.</span></span>

```qsharp
function QubitizationOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="1c623-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="1c623-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="1c623-107">qSharpData: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="1c623-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="1c623-108">Hamiltonian descrito por `JordanWignerEncodingData` formato.</span><span class="sxs-lookup"><span data-stu-id="1c623-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a><span data-ttu-id="1c623-109">Saída: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL))</span><span class="sxs-lookup"><span data-stu-id="1c623-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl))</span></span>

<span data-ttu-id="1c623-110">Uma tupla em que: `Int` é o número de qubits alocados, `Double` é a norma de Hamiltonian coeficientes, e a operação é a Walk do Quantum criada pelo Qubitization.</span><span class="sxs-lookup"><span data-stu-id="1c623-110">A tuple where: `Int` is the number of qubits allocated, `Double` is the one-norm of Hamiltonian coefficients, and the operation is the Quantum walk created by Qubitization.</span></span>