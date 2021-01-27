---
uid: Microsoft.Quantum.AmplitudeAmplification
title: Namespace Microsoft. Quantum. AmplitudeAmplification
ms.date: 1/23/2021 12:00:00 AM
ms.topic: managed-reference
qsharp.kind: namespace
qsharp.name: Microsoft.Quantum.AmplitudeAmplification
qsharp.summary: This namespace contains functions and operations for performing amplitude amplification.
ms.openlocfilehash: a014f923de62c5e660c1c0fc839fbe60e80f8ba9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845841"
---
# <a name="microsoftquantumamplitudeamplification-namespace"></a>Namespace Microsoft. Quantum. AmplitudeAmplification

Este namespace contém funções e operações para executar amplificação de amplitude.



## <a name="description"></a>Descrição

A amplificação de amplitude alheios com reflexos parciais é a forma mais geral de amplificação de amplitude implementada aqui.

Isso é chamado por meio da operação AmpAmpObliviousByReflectionPhases.

Isso tem dois registros: `ancillaRegister` e `systemRegister` .

Isso aceita dois Oracle para esses reflexos do tipo `ReflectionOracle` que atuam apenas no `ancillaRegister` registro.

Isso aceita um Oracle Special para amplificação de amplitude de alheios do tipo `ObliviousOracle` que atua em conjunto em ambos os registros.

O estado de entrada para `ancillaRegister` é considerado o único $-$1 eigenstate do primeiro operador de reflexão $I-2 \ ket {s} \ Bra {s} $.

Os reflexos sobre um estado de Quantum de destino geralmente são implementados supondo-se o acesso a um Oracle que prepare esse estado da base computacional $ \ket{0\cdots 0} $.

Nossa Convenção para esses Oracle requer dois registros: um registro de qubit único `flagQubit` e um registro para todo o restante no registro de ancillaRegister.

O Oracle do tipo `StateOracle` atua em conjunto em ambos os registros para criar o estado de destino sinalizado por $ \ket {1} $ no `flagQubit` registro com alguma amplitude real.

A reflexão `ReflectionOracle` sobre o estado desse sinalizador é gerada pela operação `TargetStateReflectionOracle` .

A reflexão `ReflectionOracle` sobre o estado de entrada para `ancillaRegister` é gerada pelo inverso de StateOracle e, em seguida, pela reflexão de $ \ket{0\cdots 0} $ com ReflectionStart ().

O Oracle do tipo `DeterministicStateOracle` atua nos `qubitState` registros para criar o estado de destino exatamente sem sinalizador.

`AmpAmpObliviousByOraclePhases` é uma versão da amplificação de amplitude alheios que aceita ORACLES `StateOracle` e `ObliviousOracle` em vez de reflexos.

Observe que a amplificação de amplitude é um caso especial de amplificação de amplitude alheios em que `ObliviousOracle` é o operador Identity, e não há nenhum qubits de sistema, ou seja, `systemRegister` está vazio.

Isso é chamado por meio da operação `AmpAmByReflectionPhases` e `AmpAmpByOraclePhases` .

As fases para reflexões parciais no caso padrão da pesquisa Grover são fornecidas pela função AmpAmpPhasesStandard.

Por exemplo, temos as seguintes dependências: AmpAmpByOracle-> AmpAmpByOraclePhases-> AmpAmpObliviousByOraclePhases-> AmpAmpObliviousByReflectionPhases.