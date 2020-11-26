---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Função PauliBlockEncoding
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: b1df6d239e6ef061cf0a4784c652e9dd126991d5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230422"
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