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
# <a name="singlequbitprocesstomographymeasurement-operation"></a>Operação SingleQubitProcessTomographyMeasurement

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Executa uma medida de tomography de processo de qubit único na base Pauli, dado um canal específico de interesse.

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a>Entrada

### <a name="preparation--pauli"></a>preparação: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

O elemento de base Pauli $P $ em que um qubit deve ser preparado.


### <a name="measurement--pauli"></a>medida: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

O elemento de base Pauli $Q $ no qual um qubit deve ser medido.


### <a name="channel--qubit--unit"></a>canal: [](xref:microsoft.quantum.lang-ref.qubit) => [unidade](xref:microsoft.quantum.lang-ref.unit) qubit 

Um único qubit Channel $ \Lambda $ cujo comportamento está sendo estimado com o Process tomography.



## <a name="output--__invalidresult__"></a>Saída: __inválida <Result>__

O resultado `Zero` com probabilidade $ $ \Begin{align} \Pr (\texttt{zero} | \Lambda; P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).
\end{align} $ $

## <a name="remarks"></a>Comentários

A distribuição sobre os resultados retornados por essa operação é um caso especial de tomography de estado de duas qubit. Deixe que $ \rho = J (\Lambda)/$2 seja o estado Choi – Jamiłkowski para $ \Lambda $. Em seguida, a distribuição acima é idêntica a $ $ \begin{align} \Pr (\texttt{Zero} | \rho; M) = \operatorname{Tr} (M \rho), \end{Align} $ $, em que $M = 2 (\boldone + P) ^ \mathrm{T}/2 \cdot (\boldone + Q)/$2 é a medida efetiva correspondente a $P $ e $Q $.