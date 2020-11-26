---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: Função FormattedFailure
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: da809c04059d4fd0f0ec92412a3094f5b582fd91
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201692"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="f9aee-102">Função FormattedFailure</span><span class="sxs-lookup"><span data-stu-id="f9aee-102">FormattedFailure function</span></span>

<span data-ttu-id="f9aee-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f9aee-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f9aee-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f9aee-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f9aee-105">Função interna usada para falhar com mensagens de erro significativas.</span><span class="sxs-lookup"><span data-stu-id="f9aee-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="f9aee-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9aee-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="f9aee-107">real: ' t</span><span class="sxs-lookup"><span data-stu-id="f9aee-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="f9aee-108">esperado: ' t</span><span class="sxs-lookup"><span data-stu-id="f9aee-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="f9aee-109">mensagem: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="f9aee-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="f9aee-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f9aee-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f9aee-111">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="f9aee-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f9aee-112">T'</span><span class="sxs-lookup"><span data-stu-id="f9aee-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="f9aee-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9aee-113">Remarks</span></span>

<span data-ttu-id="f9aee-114">Essa função deve ser emulada por tempos de execução de simulação, para permitir o encaminhamento de contradição formatadas.</span><span class="sxs-lookup"><span data-stu-id="f9aee-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>