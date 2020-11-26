---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLEA
title: Operação ApplyLEOperationOnPhaseLEA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLEA
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 408bd4e5d7146a74d7aec233765a63b2086b8ede
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190846"
---
# <a name="applyleoperationonphaselea-operation"></a>Operação ApplyLEOperationOnPhaseLEA

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação que usa um <xref:microsoft.quantum.arithmetic.phaselittleendian> registro como entrada em um registro de destino do tipo <xref:microsoft.quantum.arithmetic.littleendian> .

```qsharp
operation ApplyLEOperationOnPhaseLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj
```


## <a name="input"></a>Entrada

### <a name="op--littleendian--unit--is-adj"></a>op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) a => [unidade](xref:microsoft.quantum.lang-ref.unit) LittleEndian é adj

A operação a ser aplicada.


### <a name="target--phaselittleendian"></a>destino: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

O registro ao qual a operação é aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

O registro é transformado `LittleEndian` pelo uso de <xref:microsoft.quantum.canon.qftle> e, em seguida, retornado para sua representação original após a aplicação do `op` .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyLEOperationonPhaseLE](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [Microsoft. Quantum. Canon. ApplyLEOperationonPhaseLEC](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)
- [Microsoft. Quantum. Canon. ApplyLEOperationonPhaseLECA](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)