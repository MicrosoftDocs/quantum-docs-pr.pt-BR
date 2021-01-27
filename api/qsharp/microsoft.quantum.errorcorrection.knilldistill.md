---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Operação KnillDistill
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 4eff99eebb1e271d240513f827c6e93973ef79a6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853111"
---
# <a name="knilldistill-operation"></a>Operação KnillDistill

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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