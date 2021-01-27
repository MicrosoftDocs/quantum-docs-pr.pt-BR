---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Operação SingleQubitProcessTomographyMeasurement
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 883b98ad4f2d0ac4a02e55e444c04e8e7cf37af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839649"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a><span data-ttu-id="44f03-102">Operação SingleQubitProcessTomographyMeasurement</span><span class="sxs-lookup"><span data-stu-id="44f03-102">SingleQubitProcessTomographyMeasurement operation</span></span>

<span data-ttu-id="44f03-103">Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="44f03-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="44f03-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="44f03-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="44f03-105">Executa uma medida de tomography de processo de qubit único na base Pauli, dado um canal específico de interesse.</span><span class="sxs-lookup"><span data-stu-id="44f03-105">Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.</span></span>

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a><span data-ttu-id="44f03-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="44f03-106">Input</span></span>

### <a name="preparation--pauli"></a><span data-ttu-id="44f03-107">preparação: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="44f03-107">preparation : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="44f03-108">O elemento de base Pauli $P $ em que um qubit deve ser preparado.</span><span class="sxs-lookup"><span data-stu-id="44f03-108">The Pauli basis element $P$ in which a qubit is to be prepared.</span></span>


### <a name="measurement--pauli"></a><span data-ttu-id="44f03-109">medida: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="44f03-109">measurement : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="44f03-110">O elemento de base Pauli $Q $ no qual um qubit deve ser medido.</span><span class="sxs-lookup"><span data-stu-id="44f03-110">The Pauli basis element $Q$ in which a qubit is to be measured.</span></span>


### <a name="channel--qubit--unit"></a><span data-ttu-id="44f03-111">canal: [](xref:microsoft.quantum.lang-ref.qubit) => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit</span><span class="sxs-lookup"><span data-stu-id="44f03-111">channel : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="44f03-112">Um único qubit Channel $ \Lambda $ cujo comportamento está sendo estimado com o Process tomography.</span><span class="sxs-lookup"><span data-stu-id="44f03-112">A single qubit channel $\Lambda$ whose behavior is being estimated with process tomography.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="44f03-113">Saída: __inválida <Result>__</span><span class="sxs-lookup"><span data-stu-id="44f03-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="44f03-114">O resultado `Zero` com probabilidade $ $ \Begin{align} \Pr (\texttt{zero} | \Lambda; P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).</span><span class="sxs-lookup"><span data-stu-id="44f03-114">The Result `Zero` with probability $$ \begin{align} \Pr(\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left( \frac{\boldone + Q}{2} \Lambda\left[ \frac{\boldone + P}{2} \right] \right).</span></span>
<span data-ttu-id="44f03-115">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="44f03-115">\end{align} $$</span></span>

## <a name="remarks"></a><span data-ttu-id="44f03-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="44f03-116">Remarks</span></span>

<span data-ttu-id="44f03-117">A distribuição sobre os resultados retornados por essa operação é um caso especial de tomography de estado de duas qubit.</span><span class="sxs-lookup"><span data-stu-id="44f03-117">The distribution over results returned by this operation is a special case of two-qubit state tomography.</span></span> <span data-ttu-id="44f03-118">Deixe que $ \rho = J (\Lambda)/$2 seja o estado Choi – Jamiłkowski para $ \Lambda $.</span><span class="sxs-lookup"><span data-stu-id="44f03-118">Let $\rho = J(\Lambda) / 2$ be the Choi–Jamiłkowski state for $\Lambda$.</span></span> <span data-ttu-id="44f03-119">Em seguida, a distribuição acima é idêntica a $ $ \begin{align} \Pr (\texttt{Zero} | \rho; M) = \operatorname{Tr} (M \rho), \end{Align} $ $, em que $M = 2 (\boldone + P) ^ \mathrm{T}/2 \cdot (\boldone + Q)/$2 é a medida efetiva correspondente a $P $ e $Q $.</span><span class="sxs-lookup"><span data-stu-id="44f03-119">Then, the distribution above is identical to $$ \begin{align} \Pr(\texttt{Zero} | \rho; M) = \operatorname{Tr}(M \rho), \end{align} $$ where $M = 2 (\boldone + P)^\mathrm{T} / 2 \cdot (\boldone + Q) / 2$ is the effective measurement corresponding to $P$ and $Q$.</span></span>