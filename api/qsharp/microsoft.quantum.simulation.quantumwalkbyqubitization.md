---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: Função QuantumWalkByQubitization
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: ccef1bbf400e01800053777d0010acb7addaef53
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192478"
---
# <a name="quantumwalkbyqubitization-function"></a>Função QuantumWalkByQubitization

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converte uma reflexão de codificação de bloco em uma Walk de Quantum.

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a>Descrição

Dado um `BlockEncodingReflection` representado por um unitário $U $ que codifica algum operador $H $ de interesse, converte-o em uma passagem quantum $W $ contendo o espectro de $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.

## <a name="input"></a>Entrada

### <a name="blockencoding--blockencodingreflection"></a>blockEncoding: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Um `BlockEncodingReflection` unitário $U $ a ser convertido em uma Walk de Quantum.



## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL

Uma Walk do Quantum $W $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e contém o espectro de $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.

## <a name="references"></a>Referências

- Simulação de Hamiltonian por Qubitization Guang Hao Low, Julio L. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Simulation. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)