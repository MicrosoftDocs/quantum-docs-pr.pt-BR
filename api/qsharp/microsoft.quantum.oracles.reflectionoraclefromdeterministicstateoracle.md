---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Função ReflectionOracleFromDeterministicStateOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: 09de63d615a4d80e2b59deeddc07567aefe7660e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193821"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a>Função ReflectionOracleFromDeterministicStateOracle

Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Constrói a reflexão sobre um determinado estado de um Oracle.

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a>Descrição

Considerando uma preparação de estado determinística Oracle representada por uma matriz unitário $O $, o resultado dessa função é um Oracle que aplica uma reflexão sobre o estado $ \ket{\psi} $ preparado pelo Oracle $O $; ou seja, o estado $ \ket{\psi} $, que $O \ket {0} = \ket{\psi} $.

## <a name="input"></a>Entrada

### <a name="oracle--deterministicstateoracle"></a>Oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Um Oracle que prepara cópias do estado $ \ket{\psi} $.



## <a name="output--reflectionoracle"></a>Saída: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Um Oracle que reflete o estado $ \ket{\psi} $.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Microsoft. Quantum. oracles. ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)