---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Função SteaneCodeRecoveryX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 0f6b987ca23bd9ff2076080d60f1ca756b36848e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693431"
---
# <a name="steanecoderecoveryx-function"></a><span data-ttu-id="e67f1-102">Função SteaneCodeRecoveryX</span><span class="sxs-lookup"><span data-stu-id="e67f1-102">SteaneCodeRecoveryX function</span></span>

<span data-ttu-id="e67f1-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="e67f1-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="e67f1-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e67f1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e67f1-105">Decodificador para a parte X do grupo de estabilizador do ⟦ 7, 1, 3 ⟧ Steane código do Quantum.</span><span class="sxs-lookup"><span data-stu-id="e67f1-105">Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="e67f1-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="e67f1-106">Input</span></span>

### <a name="syndrome--syndrome"></a><span data-ttu-id="e67f1-107">Síndrome: [síndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="e67f1-107">syndrome : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="e67f1-108">Uma matriz de síndrome obtida na medição da parte X do estabilizador.</span><span class="sxs-lookup"><span data-stu-id="e67f1-108">A syndrome array obtained from measuring the X-part of the stabilizer.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="e67f1-109">Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="e67f1-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="e67f1-110">Uma matriz de operações Pauli que, quando aplicada ao sistema Quantum codificado, corrige o erro correspondente a `syndrome` .</span><span class="sxs-lookup"><span data-stu-id="e67f1-110">An array of Pauli operations which, when applied to the encoded quantum system corrects the error corresponding to `syndrome`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e67f1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e67f1-111">Remarks</span></span>

<span data-ttu-id="e67f1-112">O decodificador escolhido usa a propriedade de código CSS do ⟦ 7, 1, 3 ⟧ Steane Code, ou seja, corrige erros X e Z erros separadamente.</span><span class="sxs-lookup"><span data-stu-id="e67f1-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="e67f1-113">Uma propriedade do código é que o local da correção X, respectivamente, Z a ser aplicada é a codificação de 3 bits da síndrome X, respectivamente, Z, quando considerada um inteiro.</span><span class="sxs-lookup"><span data-stu-id="e67f1-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="e67f1-114">Referências</span><span class="sxs-lookup"><span data-stu-id="e67f1-114">References</span></span>

- <span data-ttu-id="e67f1-115">D.</span><span class="sxs-lookup"><span data-stu-id="e67f1-115">D.</span></span> <span data-ttu-id="e67f1-116">Gottesman, "códigos de estabilizador e correção de erro Quantum", Ph.D. tese, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="e67f1-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="e67f1-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e67f1-117">See Also</span></span>

- [<span data-ttu-id="e67f1-118">Microsoft. Quantum. ErrorCorrection. SteaneCodeRecoveryX</span><span class="sxs-lookup"><span data-stu-id="e67f1-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="e67f1-119">Microsoft. Quantum. ErrorCorrection. SteaneCodeRecoveryFns</span><span class="sxs-lookup"><span data-stu-id="e67f1-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)