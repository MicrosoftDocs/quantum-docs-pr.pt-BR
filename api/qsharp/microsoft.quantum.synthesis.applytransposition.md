---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Operação ApplyTransposition
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 46cf8c2c891aa02b0d8a1397e6c2b7a4b8618048
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855576"
---
# <a name="applytransposition-operation"></a>Operação ApplyTransposition

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Esta operação alterna a amplitude no índice `a` com a amplitude no índice `b` no determinado estado-vetor de `register` tamanho $n $.  Se for `a` igual `b` a, o vetor de estado não será alterado.

## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

Primeiro índice (deve ser um valor de 0 a $2 ^ n-$1)


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

O segundo índice (deve ser um valor de 0 a $2 ^ n-$1)


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Uma lista de $n $ qubits à qual o transposição é aplicado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Exemplo

Prepare uma superposição uniforme dos Estados de número $ | 1 \ rangle $, $ | 2 \ rangle $ e $ | 3 \ rangle $ em 2 qubits.

```qsharp
using (qubits = Qubit[2]) {
  let register = LittleEndian(qubits);
  PrepareUniformSuperposition(3, register);
  ApplyTransposition(0, 3, register);
}
```