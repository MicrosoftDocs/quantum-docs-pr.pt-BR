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
# <a name="decodefromsteanecode-operation"></a>Operação DecodeFromSteaneCode

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Uma operação de codificação inversa que mapeia um registro Quantum não codificado para um registro Quantum codificado no código Quantum ⟦ 7, 1, 3 ⟧ Steane.

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Entrada

### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Uma matriz de qubits que representa o estado lógico de código de 5 qubit codificado.



## <a name="output--qubitqubit"></a>Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[],[qubit](xref:microsoft.quantum.lang-ref.qubit)[])

Uma matriz qubit de comprimento 1 que representa o estado não codificado no primeiro parâmetro, junto com qubits auxiliar no segundo parâmetro.

## <a name="remarks"></a>Comentários

O decodificador escolhido usa a propriedade de código CSS do ⟦ 7, 1, 3 ⟧ Steane Code, ou seja, corrige erros X e Z erros separadamente. Uma propriedade do código é que o local da correção X, respectivamente, Z a ser aplicada é a codificação de 3 bits da síndrome X, respectivamente, Z, quando considerada um inteiro.

## <a name="references"></a>Referências

- D. Gottesman, "códigos de estabilizador e correção de erro Quantum", Ph.D. tese, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. SteaneCodeEncoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [Microsoft. Quantum. ErrorCorrection. SteaneCodeDecoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [Microsoft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)