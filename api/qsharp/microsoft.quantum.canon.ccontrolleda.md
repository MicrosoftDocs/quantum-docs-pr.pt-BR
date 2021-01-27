---
uid: Microsoft.Quantum.Canon.CControlledA
title: Função CControlledA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 823d80182621691f4fa6f42246b3d671f3adfc3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840986"
---
# <a name="ccontrolleda-function"></a><span data-ttu-id="bed6d-102">Função CControlledA</span><span class="sxs-lookup"><span data-stu-id="bed6d-102">CControlledA function</span></span>

<span data-ttu-id="bed6d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bed6d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bed6d-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bed6d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bed6d-105">Dada uma operação op, retorna uma nova operação que aplica a op se um bit de controle clássico for true.</span><span class="sxs-lookup"><span data-stu-id="bed6d-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="bed6d-106">Se `false` nada acontecer.</span><span class="sxs-lookup"><span data-stu-id="bed6d-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="bed6d-107">O modificador `A` indica que a operação é de adjointable.</span><span class="sxs-lookup"><span data-stu-id="bed6d-107">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="bed6d-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="bed6d-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="bed6d-109">op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj</span><span class="sxs-lookup"><span data-stu-id="bed6d-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="bed6d-110">Uma operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="bed6d-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj"></a><span data-ttu-id="bed6d-111">Saída: ([bool](xref:microsoft.quantum.lang-ref.bool), não) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj</span><span class="sxs-lookup"><span data-stu-id="bed6d-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="bed6d-112">Uma nova operação que será op se o bit de controle clássico for true.</span><span class="sxs-lookup"><span data-stu-id="bed6d-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bed6d-113">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="bed6d-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bed6d-114">T'</span><span class="sxs-lookup"><span data-stu-id="bed6d-114">'T</span></span>

<span data-ttu-id="bed6d-115">O tipo de entrada da operação a ser aplicada condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="bed6d-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="bed6d-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bed6d-116">See Also</span></span>

- [<span data-ttu-id="bed6d-117">Microsoft. Quantum. Canon. CControlled</span><span class="sxs-lookup"><span data-stu-id="bed6d-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)