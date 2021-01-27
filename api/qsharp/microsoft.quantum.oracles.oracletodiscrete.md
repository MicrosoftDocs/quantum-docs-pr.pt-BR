---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Função OracleToDiscrete
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842532"
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

## <a name="example"></a>Exemplo

`OracleToDiscrete(U)(3, target)` é equivalente a `U(target)` repetir três vezes.