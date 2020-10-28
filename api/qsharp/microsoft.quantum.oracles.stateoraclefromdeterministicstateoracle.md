---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Função StateOracleFromDeterministicStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: ccb083dbaaec2f306ba0740ef364ebb22408ed98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92696911"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a>Função StateOracleFromDeterministicStateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Agrupa [](https://nuget.org/packages/)


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