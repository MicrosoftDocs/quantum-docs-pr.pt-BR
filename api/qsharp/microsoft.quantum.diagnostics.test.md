---
uid: Microsoft.Quantum.Diagnostics.Test
title: Tipo de teste definido pelo usuário
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Test
qsharp.summary: Compiler-recognized attribute used to mark a unit test.
ms.openlocfilehash: 80821cb46d773d84085838d9ee539a8a45c43e61
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201488"
---
# <a name="test-user-defined-type"></a>Tipo de teste definido pelo usuário

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Atributo reconhecido pelo compilador usado para marcar um teste de unidade.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Test = (ExecutionTarget : String);
```



## <a name="named-items"></a>Itens nomeados

### <a name="executiontarget--string"></a>ExecutionTarget: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

