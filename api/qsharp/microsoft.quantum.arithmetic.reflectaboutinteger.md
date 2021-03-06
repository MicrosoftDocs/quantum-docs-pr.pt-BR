---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Operação ReflectAboutInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: 4d451c4e8e002f86c892b394f58ea2d7e9dd6a48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842988"
---
# <a name="reflectaboutinteger-operation"></a>Operação ReflectAboutInteger

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Reflete um registro quântico sobre um determinado inteiro clássico.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
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