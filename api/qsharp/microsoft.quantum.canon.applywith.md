---
uid: Microsoft.Quantum.Canon.ApplyWith
title: Operação ApplyWith
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWith
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: 7127df047a260b18d75efb092e8e090e2d0b207a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850400"
---
# <a name="applywith-operation"></a>Operação ApplyWith

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dadas duas operações, o aplica-se uma como conjugado com a outra.

```qsharp
operation ApplyWith<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit), target : 'T) : Unit
```


## <a name="description"></a>Descrição

Dadas duas operações, respectivamente descritas por operadores unitários $U $ e $V $, aplica-as na sequência $U ^ {\dagger} V U $. Ou seja, essa operação implementa o operador unitário fornecido por $V $ conjugado com $U $.

## <a name="input"></a>Entrada

### <a name="outeroperation--t--unit--is-adj"></a>outerOperation: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

A operação $U $ que deve ser usada para conjugar $V $. Observe que a operação externa $U $ precisa ser adjointable, mas não precisa ser controlável.


### <a name="inneroperation--t--unit"></a>innerOperation: t = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

A operação $V $ sendo conjugada.


### <a name="target--t"></a>destino: ' t

A entrada a ser fornecida para as operações externas e internas.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O destino no qual cada uma das operações internas e externas atuam.

## <a name="remarks"></a>Comentários

A operação externa sempre é presumida como adjointable, mas não precisa ser controlável para que a operação combinada seja controlável.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyWithA](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [Microsoft. Quantum. Canon. ApplyWithC](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [Microsoft. Quantum. Canon. ApplyWithCA](xref:Microsoft.Quantum.Canon.ApplyWithCA)