---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Operação SteaneCodeEncoderImpl
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 3a9a1b11ed9255f18135e3717de7e9e1ec891298
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200417"
---
# <a name="steanecodeencoderimpl-operation"></a>Operação SteaneCodeEncoderImpl

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Operação privada usada para implementar o codificador de código Steane e o decodificador.

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Entrada

### <a name="data--qubit"></a>dados: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

uma matriz que mantém 1 qubit que é a qubit de entrada.


### <a name="scratch--qubit"></a>Scratch: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

uma matriz que contém 6 qubits que adicionam redundância.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

