---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Operação ReflectAboutInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694550"
---
# <a name="reflectaboutinteger-operation"></a>Operação ReflectAboutInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Agrupa [](https://nuget.org/packages/)


Reflete um registro quântico sobre um determinado inteiro clássico.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Descrição

Considerando um registro Quantum inicialmente no estado $ \ sum_i \ alpha_i \ket{i} $, em que cada $ \ket{i} $ é um estado base que representa um inteiro $i $, reflete o estado do registro sobre o estado base de um determinado inteiro $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $

## <a name="input"></a>Entrada

### <a name="index--int"></a>índice: [int](xref:microsoft.quantum.lang-ref.int)

O inteiro clássico que indexa o estado base sobre o qual refletir.


### <a name="reg--littleendian"></a>Reg: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Esta operação é implementada in-loco, sem a alocação explícita de qubits auxiliares adicionais.