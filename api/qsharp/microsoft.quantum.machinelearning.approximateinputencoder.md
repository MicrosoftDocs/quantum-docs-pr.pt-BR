---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Função ApproximateInputEncoder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 035c353c34362aa3486a7df9e7bb1bc95a6f63be
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856171"
---
# <a name="approximateinputencoder-function"></a><span data-ttu-id="18390-102">Função ApproximateInputEncoder</span><span class="sxs-lookup"><span data-stu-id="18390-102">ApproximateInputEncoder function</span></span>

<span data-ttu-id="18390-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="18390-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="18390-104">Pacote: [Microsoft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="18390-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="18390-105">Dado um conjunto de coeficientes e uma tolerância, retorna uma operação de preparação de estado que prepara cada coeficiente como a amplitude correspondente de um estado de base computacional, até a tolerância determinada.</span><span class="sxs-lookup"><span data-stu-id="18390-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.</span></span>

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="18390-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="18390-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="18390-107">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="18390-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="18390-108">A tolerância de aproximação a ser usada na codificação dos coeficientes fornecidos em um estado de entrada.</span><span class="sxs-lookup"><span data-stu-id="18390-108">The approximation tolerance to be used in encoding the given coefficients into an input state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="18390-109">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="18390-109">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="18390-110">Os coeficientes a serem codificados em um estado de entrada.</span><span class="sxs-lookup"><span data-stu-id="18390-110">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="18390-111">Saída: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="18390-111">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="18390-112">Uma operação de preparação de estado que prepara os coeficientes fornecidos como um estado de entrada em um determinado registro.</span><span class="sxs-lookup"><span data-stu-id="18390-112">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>