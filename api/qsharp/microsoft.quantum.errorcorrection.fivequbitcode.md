---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: Função FiveQubitCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 3b45af29897735905f7fe52340e2a8e425bd8cbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200876"
---
# <a name="fivequbitcode-function"></a>Função FiveQubitCode

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna um valor QECC que representa o codificador de código ⟦ 5, 1, 3 ⟧ e o decodificador com medição de síndrome in-loco.

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a>Saída: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)

Retorna uma implementação de um código de correção de erro Quantum especificando um `QECC` tipo.

## <a name="remarks"></a>Comentários

Esse código foi encontrado de forma independente nos dois documentos a seguir:

- C. H. Bennett, D. DiVincenzo, J. A. Smolin e W. K. Wootters, "Entanglement de estado misto e correção de erro Quantum," Phys. Rev. A, 54 (1996) PP. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 e
- R. LaFlamme, C. Miquel, J. P. Paz e W. H. Zurek, "código de correção de erro do Quantum perfeito", Phys. Rev. Lett. 77 (1996) PP. 198-201; https://arxiv.org/abs/quant-ph/9602019