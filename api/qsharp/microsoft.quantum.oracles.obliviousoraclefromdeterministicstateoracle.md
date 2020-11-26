---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: Função ObliviousOracleFromDeterministicStateOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 8f1fe34e38edefba228fb9d01e1712e4c0916970
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226682"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a>Função ObliviousOracleFromDeterministicStateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Combina os Oracle `DeterministicStateOracle` e o `ObliviousOracle` .

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a>Entrada

### <a name="ancillaoracle--deterministicstateoracle"></a>ancillaOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Uma preparação de estado Oracle $A $ do tipo que `DeterministicStateOracle` atua no registro $a $.


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Um Oracle $U $ do tipo que `ObliviousOracle` atua em conjunto no registro $a, s $.



## <a name="output--obliviousoracle"></a>Saída: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Um Oracle $O = UA $ do tipo `ObliviousOracle` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. Quantum. oracles. ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)