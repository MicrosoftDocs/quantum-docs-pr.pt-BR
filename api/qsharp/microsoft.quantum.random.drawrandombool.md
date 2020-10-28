---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Operação DrawRandomBool
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694644"
---
# <a name="drawrandombool-operation"></a>Operação DrawRandomBool

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Agrupa [](https://nuget.org/packages/)


Devido a uma probabilidade de êxito, retorna uma única avaliação de Bernoulli que é verdadeira com a probabilidade especificada.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>Entrada

### <a name="successprobability--double"></a>successProbability: [Double](xref:microsoft.quantum.lang-ref.double)

A probabilidade com a qual `true` deve ser retornada.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` com probabilidade `successProbability` e `false` com probabilidade `1.0 - successProbability` .