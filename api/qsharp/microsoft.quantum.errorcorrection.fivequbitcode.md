---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: Função FiveQubitCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 540dcf1eafa7449f386676a9a3c9562a4d4bf29c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853150"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="85727-102">Função FiveQubitCode</span><span class="sxs-lookup"><span data-stu-id="85727-102">FiveQubitCode function</span></span>

<span data-ttu-id="85727-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="85727-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="85727-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85727-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85727-105">Retorna um valor QECC que representa o codificador de código ⟦ 5, 1, 3 ⟧ e o decodificador com medição de síndrome in-loco.</span><span class="sxs-lookup"><span data-stu-id="85727-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="85727-106">Saída: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="85727-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="85727-107">Retorna uma implementação de um código de correção de erro Quantum especificando um `QECC` tipo.</span><span class="sxs-lookup"><span data-stu-id="85727-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="85727-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="85727-108">Remarks</span></span>

<span data-ttu-id="85727-109">Esse código foi encontrado de forma independente nos dois documentos a seguir:</span><span class="sxs-lookup"><span data-stu-id="85727-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="85727-110">C.</span><span class="sxs-lookup"><span data-stu-id="85727-110">C.</span></span> <span data-ttu-id="85727-111">H.</span><span class="sxs-lookup"><span data-stu-id="85727-111">H.</span></span> <span data-ttu-id="85727-112">Bennett, D. DiVincenzo, J. A.</span><span class="sxs-lookup"><span data-stu-id="85727-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="85727-113">Smolin e W. K.</span><span class="sxs-lookup"><span data-stu-id="85727-113">Smolin and W. K.</span></span> <span data-ttu-id="85727-114">Wootters, "Entanglement de estado misto e correção de erro Quantum," Phys. Rev. A, 54 (1996) PP. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 e</span><span class="sxs-lookup"><span data-stu-id="85727-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="85727-115">R.</span><span class="sxs-lookup"><span data-stu-id="85727-115">R.</span></span> <span data-ttu-id="85727-116">LaFlamme, C. Miquel, J. P.</span><span class="sxs-lookup"><span data-stu-id="85727-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="85727-117">Paz e W. H.</span><span class="sxs-lookup"><span data-stu-id="85727-117">Paz and W. H.</span></span> <span data-ttu-id="85727-118">Zurek, "código de correção de erro do Quantum perfeito", Phys. Rev. Lett.</span><span class="sxs-lookup"><span data-stu-id="85727-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="85727-119">77 (1996) PP. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="85727-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>