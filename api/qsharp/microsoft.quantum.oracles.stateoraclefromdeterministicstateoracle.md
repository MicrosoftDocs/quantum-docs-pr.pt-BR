---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Função StateOracleFromDeterministicStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: 4eed29072cab9e8c106509a6a114c8a071441079
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842496"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a>Função StateOracleFromDeterministicStateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converte um Oracle do tipo `DeterministicStateOracle` em `StateOracle` .

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a>Entrada

### <a name="deterministicstateoracle--deterministicstateoracle"></a>deterministicStateOracle: [deterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Uma preparação de estado Oracle $A $ do tipo `DeterministicStateOracle` .



## <a name="output--stateoracle"></a>Saída: [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

A mesma preparação de estado Oracle $A $, mas agora do tipo `StateOracle` . Observe que o índice do sinalizador `StateOracle` é uma variável fictícia e não tem nenhum efeito.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. Quantum. oracles. StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)