---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Função FormattedFailure
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 0d7fb01ddf23cd6d79f722c8f6b691afa74a8885
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693509"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="10b9d-102">Função FormattedFailure</span><span class="sxs-lookup"><span data-stu-id="10b9d-102">FormattedFailure function</span></span>

<span data-ttu-id="10b9d-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="10b9d-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="10b9d-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="10b9d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="10b9d-105">Função interna usada para falhar com mensagens de erro significativas.</span><span class="sxs-lookup"><span data-stu-id="10b9d-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="10b9d-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="10b9d-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="10b9d-107">real: ' t</span><span class="sxs-lookup"><span data-stu-id="10b9d-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="10b9d-108">esperado: ' t</span><span class="sxs-lookup"><span data-stu-id="10b9d-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="10b9d-109">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="10b9d-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="10b9d-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="10b9d-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="10b9d-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="10b9d-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="10b9d-112">T'</span><span class="sxs-lookup"><span data-stu-id="10b9d-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="10b9d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="10b9d-113">Remarks</span></span>

<span data-ttu-id="10b9d-114">Essa função deve ser emulada por tempos de execução de simulação, para permitir o encaminhamento de contradição formatadas.</span><span class="sxs-lookup"><span data-stu-id="10b9d-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>