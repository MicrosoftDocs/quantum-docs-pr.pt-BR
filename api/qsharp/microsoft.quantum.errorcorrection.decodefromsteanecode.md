---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: Operação DecodeFromSteaneCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 50fc6fb22e8b65ce10aba41e18362ad96236a907
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201131"
---
# <a name="decodefromsteanecode-operation"></a><span data-ttu-id="fd40b-102">Operação DecodeFromSteaneCode</span><span class="sxs-lookup"><span data-stu-id="fd40b-102">DecodeFromSteaneCode operation</span></span>

<span data-ttu-id="fd40b-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="fd40b-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="fd40b-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fd40b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fd40b-105">Uma operação de codificação inversa que mapeia um registro Quantum não codificado para um registro Quantum codificado no código Quantum ⟦ 7, 1, 3 ⟧ Steane.</span><span class="sxs-lookup"><span data-stu-id="fd40b-105">An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="fd40b-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd40b-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="fd40b-107">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="fd40b-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="fd40b-108">Uma matriz de qubits que representa o estado lógico de código de 5 qubit codificado.</span><span class="sxs-lookup"><span data-stu-id="fd40b-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="fd40b-109">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="fd40b-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="fd40b-110">Uma matriz qubit de comprimento 1 que representa o estado não codificado no primeiro parâmetro, junto com qubits auxiliar no segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fd40b-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd40b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd40b-111">Remarks</span></span>

<span data-ttu-id="fd40b-112">O decodificador escolhido usa a propriedade de código CSS do ⟦ 7, 1, 3 ⟧ Steane Code, ou seja, corrige erros X e Z erros separadamente.</span><span class="sxs-lookup"><span data-stu-id="fd40b-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="fd40b-113">Uma propriedade do código é que o local da correção X, respectivamente, Z a ser aplicada é a codificação de 3 bits da síndrome X, respectivamente, Z, quando considerada um inteiro.</span><span class="sxs-lookup"><span data-stu-id="fd40b-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="fd40b-114">Referências</span><span class="sxs-lookup"><span data-stu-id="fd40b-114">References</span></span>

- <span data-ttu-id="fd40b-115">D.</span><span class="sxs-lookup"><span data-stu-id="fd40b-115">D.</span></span> <span data-ttu-id="fd40b-116">Gottesman, "códigos de estabilizador e correção de erro Quantum", Ph.D. tese, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="fd40b-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="fd40b-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fd40b-117">See Also</span></span>

- [<span data-ttu-id="fd40b-118">Microsoft. Quantum. ErrorCorrection. SteaneCodeEncoder</span><span class="sxs-lookup"><span data-stu-id="fd40b-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [<span data-ttu-id="fd40b-119">Microsoft. Quantum. ErrorCorrection. SteaneCodeDecoder</span><span class="sxs-lookup"><span data-stu-id="fd40b-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [<span data-ttu-id="fd40b-120">Microsoft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="fd40b-120">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)