---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: Operação Clicarei
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: 5a4e18cb0361708e1fc00e8d62c0a6c2415d6bed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694341"
---
# <a name="applyand-operation"></a>Operação Clicarei

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Inverte um determinado qubit de destino se e somente se ambos os controles qubits estiverem no estado 1, usando a medida para executar a operação de adjoin.

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a>Descrição

Inverte `target` se e somente se ambos os controles forem 1, mas pressupõe que `target` está no estado 0.  A operação tem T-Count 4, T-Depth 2 e não requer nenhum qubit auxiliar e, portanto, pode ser preferível a uma operação CCNOT, se `target` for conhecido como 0.  O adjoin dessa operação é baseado em medição e não requer nenhuma Gates.

O aplicativo controlado desta operação não requer nenhum auxiliar qubit, `2^c` `Rz` Gates e não é otimizado para profundidade, em que `c` é o número de qubits de controle geral, incluindo os dois controles da `ApplyAnd` operação.  O aplicativo controlado por adjacente requer `2^c - 1` `Rz` Gates (com um ângulo duas vezes o tamanho da operação não-adjacente), nenhum auxiliar qubit e não é otimizado para profundidade.

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
- Craig Gidney: "metade do custo da adição da Quantum", Quantum 2, página 74, 2018 [arXiv: 1709.06648](https://arxiv.org/abs/1709.06648) doi: 10.1103/PhysRevA. 85.044302
- Mathias Soeken: "circuitos do Oracle Quantum e padrão de árvore de Natal", [artigo de blog de 19 de dezembro de 2019](https://msoeken.github.io/blog_qac.html) (Observação: explica a construção de vários controlados)