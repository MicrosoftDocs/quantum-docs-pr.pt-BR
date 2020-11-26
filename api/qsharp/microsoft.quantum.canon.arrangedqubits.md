---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Função ArrangedQubits
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f3bc4dff73d5ad6393294fc3770b8d36e6094fb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217060"
---
# <a name="arrangedqubits-function"></a>Função ArrangedQubits

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Organizar qubits de controle, destino e auxiliar de acordo com um índice

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a>Descrição

Retorna uma matriz qubit com destino no índice 0 e Control i no índice 2 ^ i.  Os qubits auxiliares são inseridos em todas as outras posições na matriz.

## <a name="input"></a>Entrada

### <a name="controls--qubit"></a>controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)




### <a name="helper--qubit"></a>auxiliar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--qubit"></a>Saída: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

