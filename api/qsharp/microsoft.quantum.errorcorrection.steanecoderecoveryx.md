---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Função SteaneCodeRecoveryX
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: c90eac291ebe718d10377399184ad705bb51673e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824686"
---
# <a name="steanecoderecoveryx-function"></a>Função SteaneCodeRecoveryX

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Decodificador para a parte X do grupo de estabilizador do ⟦ 7, 1, 3 ⟧ Steane código do Quantum.

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a>Entrada

### <a name="syndrome--syndrome"></a>Síndrome: [síndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Uma matriz de síndrome obtida na medição da parte X do estabilizador.



## <a name="output--pauli"></a>Saída: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Uma matriz de operações Pauli que, quando aplicada ao sistema Quantum codificado, corrige o erro correspondente a `syndrome` .

## <a name="remarks"></a>Comentários

O decodificador escolhido usa a propriedade de código CSS do ⟦ 7, 1, 3 ⟧ Steane Code, ou seja, corrige erros X e Z erros separadamente. Uma propriedade do código é que o local da correção X, respectivamente, Z a ser aplicada é a codificação de 3 bits da síndrome X, respectivamente, Z, quando considerada um inteiro.

## <a name="references"></a>Referências

- D. Gottesman, "códigos de estabilizador e correção de erro Quantum", Ph.D. tese, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. SteaneCodeRecoveryX](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. Quantum. ErrorCorrection. SteaneCodeRecoveryFns](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)