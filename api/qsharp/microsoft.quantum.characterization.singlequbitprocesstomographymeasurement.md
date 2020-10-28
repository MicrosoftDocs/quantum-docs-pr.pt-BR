---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Operação SingleQubitProcessTomographyMeasurement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 34e5143d5be316ee42a63124d35475949db0a692
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693830"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a><span data-ttu-id="74307-102">Operação SingleQubitProcessTomographyMeasurement</span><span class="sxs-lookup"><span data-stu-id="74307-102">SingleQubitProcessTomographyMeasurement operation</span></span>

<span data-ttu-id="74307-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="74307-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="74307-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="74307-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="74307-105">Executa uma medida de tomography de processo de qubit único na base Pauli, dado um canal específico de interesse.</span><span class="sxs-lookup"><span data-stu-id="74307-105">Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.</span></span>

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a><span data-ttu-id="74307-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="74307-106">Input</span></span>

### <a name="preparation--pauli"></a><span data-ttu-id="74307-107">preparação: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="74307-107">preparation : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="74307-108">O elemento de base Pauli $P $ em que um qubit deve ser preparado.</span><span class="sxs-lookup"><span data-stu-id="74307-108">The Pauli basis element $P$ in which a qubit is to be prepared.</span></span>


### <a name="measurement--pauli"></a><span data-ttu-id="74307-109">medida: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="74307-109">measurement : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="74307-110">O elemento de base Pauli $Q $ no qual um qubit deve ser medido.</span><span class="sxs-lookup"><span data-stu-id="74307-110">The Pauli basis element $Q$ in which a qubit is to be measured.</span></span>


### <a name="channel--qubit--unit"></a><span data-ttu-id="74307-111">canal: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit</span><span class="sxs-lookup"><span data-stu-id="74307-111">channel : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="74307-112">Um único qubit Channel $ \Lambda $ cujo comportamento está sendo estimado com o Process tomography.</span><span class="sxs-lookup"><span data-stu-id="74307-112">A single qubit channel $\Lambda$ whose behavior is being estimated with process tomography.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="74307-113">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="74307-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="74307-114">O resultado `Zero` com probabilidade $ $ \Begin{align} \Pr (\texttt{zero} | \Lambda; P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).</span><span class="sxs-lookup"><span data-stu-id="74307-114">The Result `Zero` with probability $$ \begin{align} \Pr(\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left( \frac{\boldone + Q}{2} \Lambda\left[ \frac{\boldone + P}{2} \right] \right).</span></span>
<span data-ttu-id="74307-115">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="74307-115">\end{align} $$</span></span>

## <a name="remarks"></a><span data-ttu-id="74307-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="74307-116">Remarks</span></span>

<span data-ttu-id="74307-117">A distribuição sobre os resultados retornados por essa operação é um caso especial de tomography de estado de duas qubit.</span><span class="sxs-lookup"><span data-stu-id="74307-117">The distribution over results returned by this operation is a special case of two-qubit state tomography.</span></span> <span data-ttu-id="74307-118">Deixe que $ \rho = J (\Lambda)/$2 seja o estado Choi – Jamiłkowski para $ \Lambda $.</span><span class="sxs-lookup"><span data-stu-id="74307-118">Let $\rho = J(\Lambda) / 2$ be the Choi–Jamiłkowski state for $\Lambda$.</span></span> <span data-ttu-id="74307-119">Em seguida, a distribuição acima é idêntica a $ $ \begin{align} \Pr (\texttt{Zero} | \rho; M) = \operatorname{Tr} (M \rho), \end{Align} $ $, em que $M = 2 (\boldone + P) ^ \mathrm{T}/2 \cdot (\boldone + Q)/$2 é a medida efetiva correspondente a $P $ e $Q $.</span><span class="sxs-lookup"><span data-stu-id="74307-119">Then, the distribution above is identical to $$ \begin{align} \Pr(\texttt{Zero} | \rho; M) = \operatorname{Tr}(M \rho), \end{align} $$ where $M = 2 (\boldone + P)^\mathrm{T} / 2 \cdot (\boldone + Q) / 2$ is the effective measurement corresponding to $P$ and $Q$.</span></span>