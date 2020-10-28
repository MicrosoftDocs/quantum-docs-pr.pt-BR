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
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="74624-102">Tipo definido pelo usuário preterido</span><span class="sxs-lookup"><span data-stu-id="74624-102">Deprecated user defined type</span></span>

<span data-ttu-id="74624-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="74624-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="74624-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="74624-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="74624-105">Atributo reconhecido pelo compilador usado para marcar um tipo ou chamável como preterido.</span><span class="sxs-lookup"><span data-stu-id="74624-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="74624-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="74624-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="74624-107">NewName: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="74624-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="74624-108">O nome completo do tipo ou que poderia ser usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="74624-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="74624-109">É definido como a cadeia de caracteres vazia se um tipo ou callable foi preterido sem substituição.</span><span class="sxs-lookup"><span data-stu-id="74624-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>