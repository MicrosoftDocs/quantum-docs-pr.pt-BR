---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: Função FiveQubitCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 7509de880b1e3ea8964b61e4b3f034ce20b2f202
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693461"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="1c51e-102">Função FiveQubitCode</span><span class="sxs-lookup"><span data-stu-id="1c51e-102">FiveQubitCode function</span></span>

<span data-ttu-id="1c51e-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="1c51e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="1c51e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1c51e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1c51e-105">Retorna um valor QECC que representa o codificador de código ⟦ 5, 1, 3 ⟧ e o decodificador com medição de síndrome in-loco.</span><span class="sxs-lookup"><span data-stu-id="1c51e-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="1c51e-106">Saída: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="1c51e-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="1c51e-107">Retorna uma implementação de um código de correção de erro Quantum especificando um `QECC` tipo.</span><span class="sxs-lookup"><span data-stu-id="1c51e-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c51e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c51e-108">Remarks</span></span>

<span data-ttu-id="1c51e-109">Esse código foi encontrado de forma independente nos dois documentos a seguir:</span><span class="sxs-lookup"><span data-stu-id="1c51e-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="1c51e-110">C.</span><span class="sxs-lookup"><span data-stu-id="1c51e-110">C.</span></span> <span data-ttu-id="1c51e-111">H.</span><span class="sxs-lookup"><span data-stu-id="1c51e-111">H.</span></span> <span data-ttu-id="1c51e-112">Bennett, D. DiVincenzo, J. A.</span><span class="sxs-lookup"><span data-stu-id="1c51e-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="1c51e-113">Smolin e W. K.</span><span class="sxs-lookup"><span data-stu-id="1c51e-113">Smolin and W. K.</span></span> <span data-ttu-id="1c51e-114">Wootters, "Entanglement de estado misto e correção de erro Quantum," Phys. Rev. A, 54 (1996) PP. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 e</span><span class="sxs-lookup"><span data-stu-id="1c51e-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="1c51e-115">R.</span><span class="sxs-lookup"><span data-stu-id="1c51e-115">R.</span></span> <span data-ttu-id="1c51e-116">LaFlamme, C. Miquel, J. P.</span><span class="sxs-lookup"><span data-stu-id="1c51e-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="1c51e-117">Paz e W. H.</span><span class="sxs-lookup"><span data-stu-id="1c51e-117">Paz and W. H.</span></span> <span data-ttu-id="1c51e-118">Zurek, "código de correção de erro do Quantum perfeito", Phys. Rev. Lett.</span><span class="sxs-lookup"><span data-stu-id="1c51e-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="1c51e-119">77 (1996) PP. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="1c51e-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>