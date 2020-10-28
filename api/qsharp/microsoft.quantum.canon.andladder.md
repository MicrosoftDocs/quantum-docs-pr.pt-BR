---
uid: Microsoft.Quantum.Canon.AndLadder
title: Operação AndLadder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: 05a0e8110539742501883fea75ac368d9946164d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694345"
---
# <a name="andladder-operation"></a>Operação AndLadder

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Executa uma "e uma escada" controlada em um registro de qubits de destino.

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit
```


## <a name="description"></a>Descrição

Esta operação aplica uma transformação descrita pelo seguinte mapeamento da base computacional, $ $ \begin{align} \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1, \dots, y \_ {n-1}} \mapsto \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1 \oplus (x \_ 1 \land x \_ 2), \dots, y \_ {n-1} \oplus (x \_ 1 \land x \_ 2 \land \cdots \land x \_ {n-1}}, \end{Align} $ $, em que $ \ket{x \_ 1, \dots, x \_ n} $ refere-se aos Estados de base computacional de `controls` e onde $ \ket{y \_ 1, \dots, y \_ {n-1}} $ refere-se aos Estados de base computacional de `targets` .

## <a name="input"></a>Entrada

### <a name="ccnot--ccnotop"></a>ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)

O portão CCNOT a ser usado para a construção.


### <a name="controls--qubit"></a>controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro de qubits a ser usado como controles para a escada e.
Essa operação deixa os Estados de base de `controls` variável de constante.
O comprimento de `controls` deve ser pelo menos 2 e deve ser igual a um mais o comprimento de `targets` .


### <a name="targets--qubit"></a>destinos: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

O comprimento de `targets` deve ser pelo menos 1 e igual ao comprimento de `controls` menos um.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

- Usado como parte de <xref:microsoft.quantum.canon.applymulticontrolledc> e <xref:microsoft.quantum.canon.applymulticontrolledca> .
- Para obter a explicação e o diagrama de circuito, consulte a Figura 4,10, seção 4,3 em Nielsen & Chuang.

## <a name="references"></a>Referências

- [*Michael A. Nielsen, Julio L. Chuang* , computação Quantum e informações de Quantum](http://doi.org/10.1017/CBO9780511976667)