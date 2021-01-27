---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: Operação EstimateFrequencyA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 6cca8dff70283e0d69441db8a5b31fb5bfb3082a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839924"
---
# <a name="estimatefrequencya-operation"></a><span data-ttu-id="281be-102">Operação EstimateFrequencyA</span><span class="sxs-lookup"><span data-stu-id="281be-102">EstimateFrequencyA operation</span></span>

<span data-ttu-id="281be-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="281be-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="281be-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="281be-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="281be-105">Devido a uma preparação que é de adjointable e de medição, o estima a frequência com a qual essa medida é realizada com sucesso (retorna `Zero` ) executando um determinado número de avaliações.</span><span class="sxs-lookup"><span data-stu-id="281be-105">Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="281be-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="281be-106">Input</span></span>

### <a name="preparation--qubit--unit--is-adj"></a><span data-ttu-id="281be-107">preparação: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="281be-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="281be-108">Uma operação de adjointable $P $ que prepara um determinado estado $ \rho $ em seu registro de entrada.</span><span class="sxs-lookup"><span data-stu-id="281be-108">An adjointable operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="281be-109">medida: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __inválido <Result>__</span><span class="sxs-lookup"><span data-stu-id="281be-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="281be-110">Uma operação $M $ representa a medida de interesse.</span><span class="sxs-lookup"><span data-stu-id="281be-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="281be-111">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="281be-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="281be-112">O número de qubits em que cada ação de preparação e medição atua.</span><span class="sxs-lookup"><span data-stu-id="281be-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="281be-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="281be-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="281be-114">O número de vezes que a medida deve ser executada para estimar a frequência de interesse.</span><span class="sxs-lookup"><span data-stu-id="281be-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="281be-115">Saída: [duplo](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="281be-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="281be-116">Uma estimativa de $ \hat{p} $ da frequência com a qual $M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ retorna `Zero` , obtida usando o estimador binomial não polarizado $ \hat{p} = n \_ {\uparrow}/n \_ {\Text{Measurements}} $, em que $n \_ {\uparrow} $ é o número de `Zero` resultados observados.</span><span class="sxs-lookup"><span data-stu-id="281be-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="281be-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="281be-117">Remarks</span></span>

<span data-ttu-id="281be-118">Para operações de adjointable, algumas suposições podem ser feitas, como chamar a operação, preparará o qubits para exatamente o mesmo estado, que permite que os computadores de destino façam algumas otimizações de desempenho.</span><span class="sxs-lookup"><span data-stu-id="281be-118">For adjointable operations, certain assumptions can be made such like calling the operation will prepare the qubits to exactly the same state, which allow target machines to make some performance optimizations.</span></span>