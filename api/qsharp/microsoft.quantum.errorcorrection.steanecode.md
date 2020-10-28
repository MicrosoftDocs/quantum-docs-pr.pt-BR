---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Função SteaneCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: ea36320fff1f0c24426e2fcead976ef051d6699f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693438"
---
# <a name="steanecode-function"></a><span data-ttu-id="b2e99-102">Função SteaneCode</span><span class="sxs-lookup"><span data-stu-id="b2e99-102">SteaneCode function</span></span>

<span data-ttu-id="b2e99-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="b2e99-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="b2e99-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b2e99-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b2e99-105">Retorna um valor CSS que representa o codificador de código ⟦ 7, 1, 3 ⟧ Steane e o decodificador com uma medida de síndrome in-loco.</span><span class="sxs-lookup"><span data-stu-id="b2e99-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="b2e99-106">Saída: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="b2e99-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="b2e99-107">Um objeto do tipo CSS que coleta todos os dados relevantes para executar a codificação e a correção de erros para o código ⟦ 7, 1, 3 ⟧ Steane.</span><span class="sxs-lookup"><span data-stu-id="b2e99-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e99-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2e99-108">Remarks</span></span>

<span data-ttu-id="b2e99-109">Esse código foi encontrado no seguinte documento:</span><span class="sxs-lookup"><span data-stu-id="b2e99-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="b2e99-110">A.</span><span class="sxs-lookup"><span data-stu-id="b2e99-110">A.</span></span> <span data-ttu-id="b2e99-111">Steane, "interferência de várias partículas e correção de erro Quantum", proc.</span><span class="sxs-lookup"><span data-stu-id="b2e99-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="b2e99-112">Roy.</span><span class="sxs-lookup"><span data-stu-id="b2e99-112">Roy.</span></span> <span data-ttu-id="b2e99-113">SOC. Lond.</span><span class="sxs-lookup"><span data-stu-id="b2e99-113">Soc. Lond.</span></span> <span data-ttu-id="b2e99-114">A452 (1996) PP. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="b2e99-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>