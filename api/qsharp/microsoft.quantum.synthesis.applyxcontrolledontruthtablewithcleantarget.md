---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Operação ApplyXControlledOnTruthTableWithCleanTarget
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: b43a5351985339bcf7c1f2bbe03ae6dc6dfdd165
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697056"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a>Operação ApplyXControlledOnTruthTableWithCleanTarget

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Agrupa [](https://nuget.org/packages/)


Aplica a @"microsoft.quantum.intrinsic.x" operação em `target` , se a função booliana `func` for avaliada como true para a atribuição clássica no `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="description"></a>Descrição

Essa operação implementa um caso especial do @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" , no qual o qubit de destino é conhecido como no estado $ \ket {0} $.

A implementação usa @"microsoft.quantum.intrinsic.cnot" e @"microsoft.quantum.intrinsic.r1" Gates.  A implementação da operação de adjoin é otimizada e usa o descálculo baseado em medida.

## <a name="input"></a>Entrada

### <a name="func--bigint"></a>Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Tabela booliana da verdade representada como um inteiro grande


### <a name="controlregister--qubit"></a>controlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registro de qubits de controle


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit de destino (deve estar no estado $ \ket {0} $)



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. síntese. ApplyXControlledOnTruthTable](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)