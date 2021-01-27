---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Operação ApplyXControlledOnTruthTableWithCleanTarget
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: a54544cd026f26784bb0c41cb12187a8885ed9db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855544"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a>Operação ApplyXControlledOnTruthTableWithCleanTarget

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica a @"microsoft.quantum.intrinsic.x" operação em `target` , se a função booliana `func` for avaliada como true para a atribuição clássica no `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
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