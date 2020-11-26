---
uid: Microsoft.Quantum.Core.Deprecated
title: Tipo definido pelo usuário preterido
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 122cbc113a68cec107558d68a6fb145cf6bbd9db
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224081"
---
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="4c740-102">Tipo definido pelo usuário preterido</span><span class="sxs-lookup"><span data-stu-id="4c740-102">Deprecated user defined type</span></span>

<span data-ttu-id="4c740-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="4c740-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="4c740-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4c740-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4c740-105">Atributo reconhecido pelo compilador usado para marcar um tipo ou chamável como preterido.</span><span class="sxs-lookup"><span data-stu-id="4c740-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="4c740-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="4c740-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="4c740-107">NewName: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="4c740-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="4c740-108">O nome completo do tipo ou que poderia ser usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4c740-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="4c740-109">É definido como a cadeia de caracteres vazia se um tipo ou callable foi preterido sem substituição.</span><span class="sxs-lookup"><span data-stu-id="4c740-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>