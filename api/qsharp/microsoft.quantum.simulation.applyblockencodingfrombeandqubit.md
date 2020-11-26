---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingFromBEandQubit
title: Operação ApplyBlockEncodingFromBEandQubit
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingFromBEandQubit
qsharp.summary: Conversion of ((LittleEndian, Qubit[]) => () is Adj + Ctl) to BlockEncoding
ms.openlocfilehash: 16d54a982b020f4d4ded5901ec07de44a2d09726
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229606"
---
# <a name="applyblockencodingfrombeandqubit-operation"></a>Operação ApplyBlockEncodingFromBEandQubit

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Conversão de ((LittleEndian, qubit []) => () é adj + CTL) para BlockEncoding

```qsharp
operation ApplyBlockEncodingFromBEandQubit (op : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl), auxiliary : Qubit[], system : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="op--littleendianqubit--unit--is-adj--ctl"></a>op: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL




### <a name="auxiliary--qubit"></a>auxiliar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="system--qubit"></a>sistema: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

