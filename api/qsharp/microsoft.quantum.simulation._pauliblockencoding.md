---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: Função _PauliBlockEncoding
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: c27ef1a6b7cd7c84defe2a783e9fb1610e52d1e7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851073"
---
# <a name="_pauliblockencoding-function"></a>Função _PauliBlockEncoding

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Cria um unitário de codificação de bloco para um Hamiltonian.

O Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ é descrito por uma soma dos termos de Pauli $P _j $, cada um com o coeficiente real $ \ alpha_j $.

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>Entrada

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Um `GeneratorSystem` que descreve $H $ como uma soma dos termos do Pauli


### <a name="stateprepunitary--double---littleendian--unit--is-adj--ctl"></a>statePrepUnitary: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj + CTL

Uma operação unitário $V $ que aplica o $V unitário _j $ controlado no índice $ \ket{j} $, dada uma função $f: j\rightarrow V_j $.


### <a name="multiplexer--intint---qubit--unit--is-adj--ctl---littleendianqubit--unit--is-adj--ctl"></a>Multiplexador: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL)->[(LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL





## <a name="output--doubleblockencodingreflection"></a>Saída: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>Primeiro parâmetro

A uma norma de coeficientes $ \alpha = \ sum_ {j} | \ alpha_j | $.

## <a name="second-parameter"></a>Segundo parâmetro

Um `BlockEncodingReflection` unitário $U $ do Hamiltonian $U $. Como esse unitário satisfaz $U ^ 2 = I $, também é uma reflexão.

## <a name="remarks"></a>Comentários

Operações de exemplo a preparação e despreparação do estado $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ e a construção de um unitário controlado por multiplicação são <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> e <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .