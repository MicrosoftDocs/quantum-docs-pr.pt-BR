---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Tipo definido pelo usuário ComplexPolar
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: a4f3a7b6ffa73271d7ac9674d8c718f6f09c0291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210974"
---
# <a name="complexpolar-user-defined-type"></a>Tipo definido pelo usuário ComplexPolar

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa um número complexo na forma polar.

A representação polar de um número complexo é $c = r e ^ {i t} $.

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a>Itens nomeados

### <a name="magnitude--double"></a>Magnitude: [dupla](xref:microsoft.quantum.lang-ref.double)

O valor absoluto $r \ge $0 de $c $.
### <a name="argument--double"></a>Argumento: [Double](xref:microsoft.quantum.lang-ref.double)

A fase $t na \mathbb R $ de $c $.