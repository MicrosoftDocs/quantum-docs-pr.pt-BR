---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Função FixedPointReflectionPhases
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 8cc1073447f5fae87ece38db64dcc312f6208899
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191441"
---
# <a name="fixedpointreflectionphases-function"></a>Função FixedPointReflectionPhases

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Computa fases de reflexo parcial para amplificação de amplitude de ponto fixo.

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Entrada

### <a name="nqueries--int"></a>nQueries: [int](xref:microsoft.quantum.lang-ref.int)

Número de consultas à preparação do estado Oracle. Deve ser um inteiro ímpar.


### <a name="successmin--double"></a>successMin: [Double](xref:microsoft.quantum.lang-ref.double)

Probabilidade de êxito mínima de destino.



## <a name="output--reflectionphases"></a>Saída: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Matriz de fases que pode ser usada na implementação do algoritmo Quantum da amplitude de ponto fixo.

## <a name="references"></a>Referências

Usamos as fases em "amplificação de amplitude de ponto fixo com um número ideal de consultas"

- [YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Consulte também "metodologia de Gates de Quantum de composição"
- [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) para fases no `RotationPhases` formato.