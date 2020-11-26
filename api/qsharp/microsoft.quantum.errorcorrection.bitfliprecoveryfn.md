---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: Função BitFlipRecoveryFn
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: f8d102cd54222f61058c655e72c63e86d2f5af03
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201199"
---
# <a name="bitfliprecoveryfn-function"></a><span data-ttu-id="c9503-102">Função BitFlipRecoveryFn</span><span class="sxs-lookup"><span data-stu-id="c9503-102">BitFlipRecoveryFn function</span></span>

<span data-ttu-id="c9503-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="c9503-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="c9503-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c9503-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c9503-105">Função para operações de Pauli de recuperação para determinada medição de síndrome pela pesquisa de tabela para o código de flip ⟦ 3, 1, 1 ⟧ bit.</span><span class="sxs-lookup"><span data-stu-id="c9503-105">Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.</span></span>

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="c9503-106">Saída: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="c9503-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="c9503-107">Função do tipo `RecoveryFn` que usa uma medida de síndrome `Result[]` e retorna as `Pauli[]` operações que corrigem o erro detectado.</span><span class="sxs-lookup"><span data-stu-id="c9503-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9503-108">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c9503-108">See Also</span></span>

- [<span data-ttu-id="c9503-109">Microsoft. Quantum. ErrorCorrection. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="c9503-109">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)