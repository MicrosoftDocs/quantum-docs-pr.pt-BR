---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Função ApproximateInputEncoder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 67ef7a47a2e036f0953d946b4ace0e6673b173bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694687"
---
# <a name="approximateinputencoder-function"></a><span data-ttu-id="646a4-102">Função ApproximateInputEncoder</span><span class="sxs-lookup"><span data-stu-id="646a4-102">ApproximateInputEncoder function</span></span>

<span data-ttu-id="646a4-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="646a4-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="646a4-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="646a4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="646a4-105">Dado um conjunto de coeficientes e uma tolerância, retorna uma operação de preparação de estado que prepara cada coeficiente como a amplitude correspondente de um estado de base computacional, até a tolerância determinada.</span><span class="sxs-lookup"><span data-stu-id="646a4-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.</span></span>

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="646a4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="646a4-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="646a4-107">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="646a4-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="646a4-108">A tolerância de aproximação a ser usada na codificação dos coeficientes fornecidos em um estado de entrada.</span><span class="sxs-lookup"><span data-stu-id="646a4-108">The approximation tolerance to be used in encoding the given coefficients into an input state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="646a4-109">coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="646a4-109">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="646a4-110">Os coeficientes a serem codificados em um estado de entrada.</span><span class="sxs-lookup"><span data-stu-id="646a4-110">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="646a4-111">Saída: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="646a4-111">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="646a4-112">Uma operação de preparação de estado que prepara os coeficientes fornecidos como um estado de entrada em um determinado registro.</span><span class="sxs-lookup"><span data-stu-id="646a4-112">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>