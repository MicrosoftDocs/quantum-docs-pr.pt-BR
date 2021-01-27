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
# <a name="steanecode-function"></a>Função SteaneCode

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna um valor CSS que representa o codificador de código ⟦ 7, 1, 3 ⟧ Steane e o decodificador com uma medida de síndrome in-loco.

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a>Saída: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

Um objeto do tipo CSS que coleta todos os dados relevantes para executar a codificação e a correção de erros para o código ⟦ 7, 1, 3 ⟧ Steane.

## <a name="remarks"></a>Comentários

Esse código foi encontrado no seguinte documento:

- a. Steane, "interferência de várias partículas e correção de erro Quantum", proc. Roy. SOC. Lond. A452 (1996) PP. 2551; https://arxiv.org/abs/quant-ph/9601029.