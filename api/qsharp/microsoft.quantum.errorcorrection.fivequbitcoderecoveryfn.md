---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: Função FiveQubitCodeRecoveryFn
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 47e8a74d3631be2209537679ec9786a8dab63c58
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200774"
---
# <a name="fivequbitcoderecoveryfn-function"></a><span data-ttu-id="a5aed-102">Função FiveQubitCodeRecoveryFn</span><span class="sxs-lookup"><span data-stu-id="a5aed-102">FiveQubitCodeRecoveryFn function</span></span>

<span data-ttu-id="a5aed-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a5aed-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a5aed-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5aed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5aed-105">Retorna a função que mapeia as medições de erro de síndrome para os operadores de Pauli de correção de erros apropriados por pesquisa de tabela para o código Quantum ⟦ 5, 1, 3 ⟧.</span><span class="sxs-lookup"><span data-stu-id="a5aed-105">Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="a5aed-106">Saída: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="a5aed-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="a5aed-107">Função do tipo `RecoveryFn` que usa uma medida de síndrome `Result[]` e retorna os `Pauli[]` operadores que corrigem o erro detectado.</span><span class="sxs-lookup"><span data-stu-id="a5aed-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operators that corrects the detected error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5aed-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5aed-108">Remarks</span></span>

<span data-ttu-id="a5aed-109">Ao iterar em todos os erros de peso de $1 $, obtemos um total de US $3 \ vezes 5 = 15 $ possíveis síndromes não triviais.</span><span class="sxs-lookup"><span data-stu-id="a5aed-109">By iterating over all errors of weight $1$, we obtain a total of $3\times 5=15$ possible non-trivial syndromes.</span></span>
<span data-ttu-id="a5aed-110">Junto com a identidade, uma tabela de erros e a síndrome correspondente são criadas.</span><span class="sxs-lookup"><span data-stu-id="a5aed-110">Together with the identity, a table of error and corresponding syndrome is built up.</span></span> <span data-ttu-id="a5aed-111">Para o código de 5 qubit, essa tabela é fornecida por: $X \_ 1: (0, 0, 0, 1); X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0, 0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0, 0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ com $Y _i $ obtido adicionando as per$Xs _i $ e $Z _i $.</span><span class="sxs-lookup"><span data-stu-id="a5aed-111">For the 5 qubit code this table is given by: $X\_1: (0,0,0,1); X\_2: (1,0,0,0); X\_3: (1,1,0,0); X\_4: (0,1,1,0); X\_5: (0,0,1,1)$, $Z\_1: (1,0,1,0); Z\_2: (0,1,0,1); Z\_3: (0,0,1,0); Z\_4: (1,0,0,1); Z\_5: (0,1,0,0)$ with $Y_i$ obtained by adding the $X_i$ and $Z_i$ syndromes.</span></span> <span data-ttu-id="a5aed-112">Observe que a ordem na recuperação de pesquisa de tabela é fornecida pela conversão de bitvectors em inteiros (usando little endian).</span><span class="sxs-lookup"><span data-stu-id="a5aed-112">Note that the ordering in the table lookup recovery is given by converting the bitvectors to integers (using little endian).</span></span>

## <a name="see-also"></a><span data-ttu-id="a5aed-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a5aed-113">See Also</span></span>

- [<span data-ttu-id="a5aed-114">Microsoft. Quantum. ErrorCorrection. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="a5aed-114">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)