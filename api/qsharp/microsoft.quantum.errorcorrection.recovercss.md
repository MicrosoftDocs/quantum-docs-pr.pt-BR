---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Operação RecoverCSS
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: eb01b1b9fccc19f0e3f1fd5ee596b95d0d61563f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200536"
---
# <a name="recovercss-operation"></a><span data-ttu-id="562f6-102">Operação RecoverCSS</span><span class="sxs-lookup"><span data-stu-id="562f6-102">RecoverCSS operation</span></span>

<span data-ttu-id="562f6-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="562f6-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="562f6-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="562f6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="562f6-105">Executa uma única rodada de correção de erro por um código Quantum descrito por um `CSS` tipo.</span><span class="sxs-lookup"><span data-stu-id="562f6-105">Performs a single round of error correction by a quantum code described by a `CSS` type.</span></span>

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="562f6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="562f6-106">Input</span></span>

### <a name="code--css"></a><span data-ttu-id="562f6-107">código: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="562f6-107">code : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="562f6-108">Um código baseado em CSS de Quantum-corrigindo o pacote de códigos como um `CSS` tipo descreve a codificação e decodificação de dados Quantum e como os síndromes de erro devem ser medidos.</span><span class="sxs-lookup"><span data-stu-id="562f6-108">A quantum CSS error-correcting code packaged as a `CSS` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fnx--recoveryfn"></a><span data-ttu-id="562f6-109">fnX: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="562f6-109">fnX : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="562f6-110">Um `RecoveryFn` que mapeia cada síndrome $X $ Error para as `Pauli[]` operações que corrigem o erro detectado.</span><span class="sxs-lookup"><span data-stu-id="562f6-110">A `RecoveryFn` that maps each $X$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="fnz--recoveryfn"></a><span data-ttu-id="562f6-111">fnZ: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="562f6-111">fnZ : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="562f6-112">Um `RecoveryFn` que mapeia cada síndrome $Z $ Error para as `Pauli[]` operações que corrigem o erro detectado.</span><span class="sxs-lookup"><span data-stu-id="562f6-112">A `RecoveryFn` that maps each $Z$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="562f6-113">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="562f6-113">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="562f6-114">Uma matriz de qubits onde o código de estabilizador é definido.</span><span class="sxs-lookup"><span data-stu-id="562f6-114">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="562f6-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="562f6-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="562f6-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="562f6-116">See Also</span></span>

- [<span data-ttu-id="562f6-117">Microsoft. Quantum. ErrorCorrection. CSS</span><span class="sxs-lookup"><span data-stu-id="562f6-117">Microsoft.Quantum.ErrorCorrection.CSS</span></span>](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [<span data-ttu-id="562f6-118">Microsoft. Quantum. ErrorCorrection. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="562f6-118">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="562f6-119">Microsoft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="562f6-119">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)