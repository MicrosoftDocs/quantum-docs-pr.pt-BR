---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: Operação AssertPhaseLessThan
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: 8a943ff937593801bd308ab4224c7051ff8a10cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223741"
---
# <a name="assertphaselessthan-operation"></a>Operação AssertPhaseLessThan

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que o `number` codificado em PhaseLittleEndian é menor que `value` .

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="value--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

`number` deve ser menor que isso.


### <a name="number--phaselittleendian"></a>número: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Inteiro não assinado que é comparado a `value` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

A versão controlada dessa operação ignora os controles.