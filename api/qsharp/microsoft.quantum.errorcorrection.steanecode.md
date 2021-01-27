---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Função SteaneCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: af3f3ef5088b898bd827ebca00fdc7fcb992f2a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853065"
---
# <a name="steanecode-function"></a><span data-ttu-id="060fe-102">Função SteaneCode</span><span class="sxs-lookup"><span data-stu-id="060fe-102">SteaneCode function</span></span>

<span data-ttu-id="060fe-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="060fe-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="060fe-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="060fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="060fe-105">Retorna um valor CSS que representa o codificador de código ⟦ 7, 1, 3 ⟧ Steane e o decodificador com uma medida de síndrome in-loco.</span><span class="sxs-lookup"><span data-stu-id="060fe-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="060fe-106">Saída: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="060fe-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="060fe-107">Um objeto do tipo CSS que coleta todos os dados relevantes para executar a codificação e a correção de erros para o código ⟦ 7, 1, 3 ⟧ Steane.</span><span class="sxs-lookup"><span data-stu-id="060fe-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="060fe-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="060fe-108">Remarks</span></span>

<span data-ttu-id="060fe-109">Esse código foi encontrado no seguinte documento:</span><span class="sxs-lookup"><span data-stu-id="060fe-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="060fe-110">a.</span><span class="sxs-lookup"><span data-stu-id="060fe-110">A.</span></span> <span data-ttu-id="060fe-111">Steane, "interferência de várias partículas e correção de erro Quantum", proc.</span><span class="sxs-lookup"><span data-stu-id="060fe-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="060fe-112">Roy.</span><span class="sxs-lookup"><span data-stu-id="060fe-112">Roy.</span></span> <span data-ttu-id="060fe-113">SOC. Lond.</span><span class="sxs-lookup"><span data-stu-id="060fe-113">Soc. Lond.</span></span> <span data-ttu-id="060fe-114">A452 (1996) PP. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="060fe-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>