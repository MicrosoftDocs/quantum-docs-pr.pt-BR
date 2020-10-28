---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Função FixedPointReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 6ab2a8c6cb0b390f96aa13ece5d5b89c196a6107
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694904"
---
# <a name="fixedpointreflectionphases-function"></a>Função FixedPointReflectionPhases

Namespace: [Microsoft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Agrupa [](https://nuget.org/packages/)


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