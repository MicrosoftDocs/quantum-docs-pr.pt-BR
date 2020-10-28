---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: Operação LogicalANDMeasAndFix
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693973"
---
# <a name="logicalandmeasandfix-operation"></a>Operação LogicalANDMeasAndFix

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Computa o e lógico de vários qubits.

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a>Entrada

### <a name="ctrlregister--qubit"></a>ctrlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Entrada qubits para a porta múltipla e entrada.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit na qual a saída de e é gravada. Isso é presumido para sempre iniciar no estado $ \ket {0} $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Quando `ctrlRegister` tem exatamente $2 $ qubits, isso é equivalente à `CCNOT` operação, mas a fase com uma fase $e ^ {i \ pi/2} $ em $ \ket {001} $ e $-e ^ {i \ pi/2} $ em $ \ket {101} $ e $ \ket {011} $.
O adjoin também é uma abordagem de medida e correção que é o inverso da operação original somente em casos especiais (consulte referências), mas usa menos T-Gates.

## <a name="references"></a>Referências

- [*Craig Gidney* , 1709, 6648](https://arxiv.org/abs/1709.06648)