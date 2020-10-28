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
# <a name="singlequbitprocesstomographymeasurement-operation"></a>Operação SingleQubitProcessTomographyMeasurement

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Agrupa [](https://nuget.org/packages/)


Executa uma medida de tomography de processo de qubit único na base Pauli, dado um canal específico de interesse.

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a>Entrada

### <a name="preparation--pauli"></a>preparação: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

O elemento de base Pauli $P $ em que um qubit deve ser preparado.


### <a name="measurement--pauli"></a>medida: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

O elemento de base Pauli $Q $ no qual um qubit deve ser medido.


### <a name="channel--qubit--unit"></a>canal: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit 

Um único qubit Channel $ \Lambda $ cujo comportamento está sendo estimado com o Process tomography.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

O resultado `Zero` com probabilidade $ $ \Begin{align} \Pr (\texttt{zero} | \Lambda; P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).
\end{align} $ $

## <a name="remarks"></a>Comentários

A distribuição sobre os resultados retornados por essa operação é um caso especial de tomography de estado de duas qubit. Deixe que $ \rho = J (\Lambda)/$2 seja o estado Choi – Jamiłkowski para $ \Lambda $. Em seguida, a distribuição acima é idêntica a $ $ \begin{align} \Pr (\texttt{Zero} | \rho; M) = \operatorname{Tr} (M \rho), \end{Align} $ $, em que $M = 2 (\boldone + P) ^ \mathrm{T}/2 \cdot (\boldone + Q)/$2 é a medida efetiva correspondente a $P $ e $Q $.