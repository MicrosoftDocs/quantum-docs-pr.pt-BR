---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: Operação ApplyLowDepthAnd
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 7fa9d9bf2f1905bf1b59e783d7bceb8cb2e09fa4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841699"
---
# <a name="applylowdepthand-operation"></a>Operação ApplyLowDepthAnd

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Inverte um determinado qubit de destino se e somente se ambos os controles qubits estiverem no estado 1, com T-depth 1, usando a medida para executar a operação de estado adjacente.

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Inverte `target` se e somente se ambos os controles forem 1, mas pressupõe que `target` está no estado 0.  A operação tem T-Count 4, T-depth 1 e requer um qubit auxiliar e, portanto, pode ser preferível a uma operação CCNOT, se `target` for conhecido como 0.  O adjoin dessa operação é baseado em medição e não requer nenhuma Gates e nenhum qubit auxiliar.

## <a name="input"></a>Entrada

### <a name="control1--qubit"></a>Control1: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit de controle primeiro


### <a name="control2--qubit"></a>Control2: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit de controle secundário


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit auxiliar de destino; deve estar no estado 0



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referências

- Cody Jones: "construções de romance para a porta Toffoli tolerante a falhas", Phys. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/PhysRevA. 87.022328
- Peter Selinger: "circuitos Quantum de T-Depth One", Phys. Rev. A 87, 042302, 2013 [arXiv: 1210.0974](https://arxiv.org/abs/1210.0974) doi: 10.1103/PhysRevA. 87.042302