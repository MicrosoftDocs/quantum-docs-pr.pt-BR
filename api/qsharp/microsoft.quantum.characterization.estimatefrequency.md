---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: Operação EstimateFrequency
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 30b21a8e86eb5a4dd8dd8207dbdc6a0970308319
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216244"
---
# <a name="estimatefrequency-operation"></a>Operação EstimateFrequency

Namespace: [Microsoft. Quantum. caracterization](xref:Microsoft.Quantum.Characterization)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma preparação e medida, o estima a frequência com a qual essa medida é realizada com sucesso (retorna `Zero` ) executando um determinado número de avaliações.

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Entrada

### <a name="preparation--qubit--unit"></a>preparação: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Uma operação $P $ que prepara um determinado estado $ \rho $ em seu registro de entrada.


### <a name="measurement--qubit--__invalidresult__"></a>medida: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __inválido <Result>__ 

Uma operação $M $ representa a medida de interesse.


### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits em que cada ação de preparação e medição atua.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

O número de vezes que a medida deve ser executada para estimar a frequência de interesse.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)

Uma estimativa de $ \hat{p} $ da frequência com a qual $M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ retorna `Zero` , obtida usando o estimador binomial não polarizado $ \hat{p} = n \_ {\uparrow}/n \_ {\Text{Measurements}} $, em que $n \_ {\uparrow} $ é o número de `Zero` resultados observados.

Isso é particularmente importante em computadores de destino que respeitam as limitações físicas, de modo que as probabilidades não podem ser medidas.