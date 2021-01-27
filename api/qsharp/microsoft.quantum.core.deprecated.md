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
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="3dd4d-102">Tipo definido pelo usuário preterido</span><span class="sxs-lookup"><span data-stu-id="3dd4d-102">Deprecated user defined type</span></span>

<span data-ttu-id="3dd4d-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="3dd4d-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="3dd4d-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3dd4d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3dd4d-105">Atributo reconhecido pelo compilador usado para marcar um tipo ou chamável como preterido.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="3dd4d-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="3dd4d-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="3dd4d-107">NewName: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="3dd4d-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="3dd4d-108">O nome completo do tipo ou que poderia ser usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="3dd4d-109">É definido como a cadeia de caracteres vazia se um tipo ou callable foi preterido sem substituição.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>