---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Tipo definido pelo usuário BigEndian
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 2f6ec9f83ac124ce9b06c278f8fda820c35c23aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843387"
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