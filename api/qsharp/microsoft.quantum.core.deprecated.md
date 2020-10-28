---
uid: Microsoft.Quantum.Core.Deprecated
title: Tipo definido pelo usuário preterido
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: b1fcae9647b2a655d25773386ecffa826515516e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693594"
---
# <a name="deprecated-user-defined-type"></a>Tipo definido pelo usuário preterido

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Agrupa [](https://nuget.org/packages/)


Atributo reconhecido pelo compilador usado para marcar um tipo ou chamável como preterido.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>Itens nomeados

### <a name="newname--string"></a>NewName: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

O nome completo do tipo ou que poderia ser usado em vez disso.
É definido como a cadeia de caracteres vazia se um tipo ou callable foi preterido sem substituição.