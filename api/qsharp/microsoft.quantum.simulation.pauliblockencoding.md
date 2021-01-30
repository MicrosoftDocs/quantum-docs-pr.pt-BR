---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Função PauliBlockEncoding
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 2e37b40c60d19aa747114de988dddc19f0d7c50b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848015"
---
# <a name="pauliblockencoding-function"></a>Função PauliBlockEncoding

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Cria um unitário de codificação de bloco para um Hamiltonian.

O Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ é descrito por uma soma dos termos de Pauli $P _j $, cada um com o coeficiente real $ \ alpha_j $.

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>Entrada

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Um `GeneratorSystem` que descreve $H $ como uma soma dos termos do Pauli



## <a name="output--doubleblockencodingreflection"></a>Saída: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>Primeiro parâmetro

A uma norma de coeficientes $ \alpha = \ sum_ {j} | \ alpha_j | $.

## <a name="second-parameter"></a>Segundo parâmetro

Um `BlockEncodingReflection` unitário $U $ do Hamiltonian $H $. Como esse unitário satisfaz $U ^ 2 = I $, também é uma reflexão.

## <a name="remarks"></a>Comentários

Isso é obtido preparando e despreparando o estado $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ e construindo um unitário controlado por multiplicação <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> e <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .