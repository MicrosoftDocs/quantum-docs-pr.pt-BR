---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: Operação EstimateFrequency
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 83589637a7bfa328812207271844411f57d42097
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693853"
---
# <a name="estimatefrequency-operation"></a><span data-ttu-id="6160e-102">Operação EstimateFrequency</span><span class="sxs-lookup"><span data-stu-id="6160e-102">EstimateFrequency operation</span></span>

<span data-ttu-id="6160e-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="6160e-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="6160e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6160e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6160e-105">Dada uma preparação e medida, o estima a frequência com a qual essa medida é realizada com sucesso (retorna `Zero` ) executando um determinado número de avaliações.</span><span class="sxs-lookup"><span data-stu-id="6160e-105">Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="6160e-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="6160e-106">Input</span></span>

### <a name="preparation--qubit--unit"></a><span data-ttu-id="6160e-107">preparação: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="6160e-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="6160e-108">Uma operação $P $ que prepara um determinado estado $ \rho $ em seu registro de entrada.</span><span class="sxs-lookup"><span data-stu-id="6160e-108">An operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="6160e-109">medida: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="6160e-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="6160e-110">Uma operação $M $ representa a medida de interesse.</span><span class="sxs-lookup"><span data-stu-id="6160e-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="6160e-111">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6160e-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6160e-112">O número de qubits em que cada ação de preparação e medição atua.</span><span class="sxs-lookup"><span data-stu-id="6160e-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="6160e-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6160e-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6160e-114">O número de vezes que a medida deve ser executada para estimar a frequência de interesse.</span><span class="sxs-lookup"><span data-stu-id="6160e-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="6160e-115">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6160e-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6160e-116">Uma estimativa de $ \hat{p} $ da frequência com a qual $M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ retorna `Zero` , obtida usando o estimador binomial não polarizado $ \hat{p} = n \_ {\uparrow}/n \_ {\Text{Measurements}} $, em que $n \_ {\uparrow} $ é o número de `Zero` resultados observados.</span><span class="sxs-lookup"><span data-stu-id="6160e-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

<span data-ttu-id="6160e-117">Isso é particularmente importante em computadores de destino que respeitam as limitações físicas, de modo que as probabilidades não podem ser medidas.</span><span class="sxs-lookup"><span data-stu-id="6160e-117">This is particularly important on target machines which respect physical limitations, such that probabilities cannot be measured.</span></span>