---
uid: Microsoft.Quantum.Core.Deprecated
title: Tipo definido pelo usuário preterido
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 1a32d98f5d034c2673d42301b45379da1302ca7f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832078"
---
# <a name="deprecated-user-defined-type"></a>Tipo definido pelo usuário preterido

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Atributo reconhecido pelo compilador usado para marcar um tipo ou chamável como preterido.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>Itens nomeados

### <a name="newname--string"></a>NewName: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

O nome completo do tipo ou que poderia ser usado em vez disso.
É definido como a cadeia de caracteres vazia se um tipo ou callable foi preterido sem substituição.