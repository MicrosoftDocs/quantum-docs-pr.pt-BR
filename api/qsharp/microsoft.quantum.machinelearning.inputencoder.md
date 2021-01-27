---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: Função InputEncoder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: ed70d9f24af06f8918083307c98a5f6c4671f1c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852933"
---
# <a name="inputencoder-function"></a><span data-ttu-id="3150a-102">Função InputEncoder</span><span class="sxs-lookup"><span data-stu-id="3150a-102">InputEncoder function</span></span>

<span data-ttu-id="3150a-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3150a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="3150a-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3150a-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="3150a-105">Dado um conjunto de coeficientes e uma tolerância, retorna uma operação de preparação de estado que prepara cada coeficiente como a amplitude correspondente de um estado de base computacional.</span><span class="sxs-lookup"><span data-stu-id="3150a-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="3150a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="3150a-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="3150a-107">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="3150a-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="3150a-108">Os coeficientes a serem codificados em um estado de entrada.</span><span class="sxs-lookup"><span data-stu-id="3150a-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="3150a-109">Saída: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="3150a-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="3150a-110">Uma operação de preparação de estado que prepara os coeficientes fornecidos como um estado de entrada em um determinado registro.</span><span class="sxs-lookup"><span data-stu-id="3150a-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>