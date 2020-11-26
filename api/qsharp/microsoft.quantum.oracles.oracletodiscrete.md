---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Função OracleToDiscrete
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: 158a90bbd0c68406e0a8507ae99fc08fad3b6d19
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193838"
---
# <a name="oracletodiscrete-function"></a>Função OracleToDiscrete

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação que representa uma "caixa preta" da Oracle, retorna um Oracle de tempo discreto que representa a "caixa preta" da Oracle repetida várias vezes.

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a>Entrada

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a>blackBoxOracle: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

A operação a ser exponenciaçãoda.



## <a name="output--discreteoracle"></a>Saída: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Uma operação parcialmente aplicada sobre a "caixa preta" da Oracle que representa o tempo discreto da Oracle