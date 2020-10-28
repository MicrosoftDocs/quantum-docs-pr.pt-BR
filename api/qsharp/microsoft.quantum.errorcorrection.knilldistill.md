---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Operação KnillDistill
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 1135db83cf750918347df10c6f1301b636aaee0c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693452"
---
# <a name="knilldistill-operation"></a>Operação KnillDistill

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Agrupa [](https://nuget.org/packages/)


Implementa o algoritmo detalhamento de estado mágico Knill.

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a>Descrição

Dadas 15 cópias aproximadas de um estado mágico $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} {8} \ket {1} \end{Align}, $ $ produz uma cópia de qualidade superior.

## <a name="input"></a>Entrada

### <a name="roughmagic--qubit"></a>roughMagic: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro de quinze qubits que contém cópias aproximadas de um estado mágico. O aplicativo a seguir deste procedimento detalhamento conterá `roughMagic[0]` uma cópia de qualidade superior e o restante do registro será redefinido para o estado $ \ket{00\cdots 0} $.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)

Se `true` , o procedimento foi bem-sucedido e a cópia de qualidade superior deve ser aceita. Se `false` , o procedimento falhou e o estado do registro deve ser considerado indefinido.

## <a name="remarks"></a>Comentários

Seguimos o algoritmo de Knill.
No entanto, a implementação atual está longe de ser a ideal, pois ela usa muitas qubits.
Os Estados mágicos são injetados nessa rotina; nesse caso, há protocolos melhores.

## <a name="references"></a>Referências

- [Knill](https://arxiv.org/abs/quant-ph/0402171)