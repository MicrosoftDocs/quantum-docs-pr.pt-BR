---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Função SteaneCodeRecoveryFns
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 7395996e75c5a1c0c5d13f76d9ec76acae5683c7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200400"
---
# <a name="steanecoderecoveryfns-function"></a><span data-ttu-id="20654-102">Função SteaneCodeRecoveryFns</span><span class="sxs-lookup"><span data-stu-id="20654-102">SteaneCodeRecoveryFns function</span></span>

<span data-ttu-id="20654-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="20654-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="20654-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="20654-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="20654-105">Decodificador para partes X-e Z combinadas do grupo de estabilizador do ⟦ 7, 1, 3 ⟧ Steane de código Quantum.</span><span class="sxs-lookup"><span data-stu-id="20654-105">Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a><span data-ttu-id="20654-106">Saída: ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span><span class="sxs-lookup"><span data-stu-id="20654-106">Output : ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span></span>

<span data-ttu-id="20654-107">Tupla de funções do tipo `RecoveryFn` que usa uma medida de síndrome `Result[]` e retorna as `Pauli[]` operações que corrigem o erro detectado.</span><span class="sxs-lookup"><span data-stu-id="20654-107">Tuple of functions of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="20654-108">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="20654-108">See Also</span></span>

- [<span data-ttu-id="20654-109">Microsoft. Quantum. ErrorCorrection. SteaneCodeRecoveryX</span><span class="sxs-lookup"><span data-stu-id="20654-109">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="20654-110">Microsoft. Quantum. ErrorCorrection. SteaneCodeRecoveryZ</span><span class="sxs-lookup"><span data-stu-id="20654-110">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)