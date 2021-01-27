---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Função DeterministicStateOracleFromStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: af545a7d6e82e654ee36ab3ba77c8f8be3384b96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854549"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a>Função DeterministicStateOracleFromStateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converte um Oracle do tipo `StateOracle` em `DeterministicStateOracle` .

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a>Entrada

### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

O índice para o sinalizador qubit do `stateOracle` $A $, que age explicitamente em dois registros: o sinalizador $f $ e o sistema $s $, por exemplo $A \ket {0} \_ f\ket {\ psi} \_ s $.


### <a name="stateoracle--stateoracle"></a>stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Uma preparação de estado Oracle $A $ do tipo `StateOracle` .



## <a name="output--deterministicstateoracle"></a>Saída: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

A mesma preparação de estado Oracle $A $, mas agora do tipo `DeterministicStateOracle` , por isso atua em um registro em que $a, s $ não é mais explicitamente separado, por exemplo,  $A \ket{0\psi} \_ {as} $.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. oracles. StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)
- [Microsoft. Quantum. oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)