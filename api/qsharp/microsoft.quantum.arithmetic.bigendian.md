---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Tipo definido pelo usuário BigEndian
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 8ea1aefa46a7224ef199baf68f2d6ab2d563e3a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223656"
---
# <a name="bigendian-user-defined-type"></a>Tipo definido pelo usuário BigEndian

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Registre-se que codifica um inteiro não assinado na ordem big-endian. O qubit com o índice `0` codifica o bit mais alto de um inteiro sem sinal.

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a>Comentários

Abreviamos `BigEndian` como `BE` na documentação.